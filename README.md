Hi all —
I’ve started the initial investigation on this issue.
From the checkout response analysis, the unexpected airline credit deduction appears to be coming from the priced product breakdown returned by FSS (Flight Service). Specifically, the breakdown section includes an airline credit component that is being propagated into the checkout total object, even when no airline credit option is explicitly selected on the UI.
I was able to reproduce this once in lab, but subsequent attempts were inconsistent. I’m currently working on a deeper trace (local + lab) to identify:
In which flow the airline credit brick is being added to the breakdown list
Whether this originates directly from Flight Service or is being transformed/augmented downstream (FNG/SUS)
If this is configuration-driven or tied to a recent change
At this point, it appears Flight Service may be behaving as designed, but I’m validating that assumption before concluding.
Investigation is ongoing. I’ll share a confirmed root cause along with a precise ETA once we determine:
Where the incorrect breakdown entry is introduced
The scope of impact across services
The remediation approach (service fix vs. transformation guard)
Please allow some time for a thorough root cause analysis. I’ll provide a structured update shortly.
