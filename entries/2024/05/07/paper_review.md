# Paper Review

## Testing Android Third Party Libraries with LLMs to Detect Incompatible APIs

### Summary

The paper proposes LibCT which uses GPT-4 to automatically generate test cases in order to detect incompatible Android APIs invoked by Third-Party Libraries (TPLs). LibCT uncovers the incompatiblities via runtime exceptions that indicates the incompatible implementation (or the lack thereof) of the Android framework APIs. The incompatiblities are found to be caused by either the evolution of the Android framework, or by hardware/vendor/manufacturer differences. 


### Strengths

- The paper approaches the novel problem in solving compatiblity issues between the Android Framework and TPLs instead of Android Apps.

- The paper makes interesting discoveries on the category of applications (video-related) that is the most prone to breakages caused by API incompatibilities between different Android versions, and UI-related invocations causing breakages between different devices.

### Weaknesses

- Relation between the number of few-shot learnining training sessions (or the number of test cases per training session) and the failure rate of the test execution (or attempts until successful test generation) is not evaluated.

- In the few-shot training process, the effect of **[API usage]** field's presence in the pre-prompts on the failure rate of test generation and execution is not evaluated.  
