
Hi team,

Recently while reviewing our environments, I noticed that our service was still using the Alpha environment, which we are no longer using since everything has moved to the main branch with the beta environment. I cleaned it up on our side as it seemed unnecessary.

While checking further, I observed that a few other services still have 4–6 pods running in Alpine/Alpha, with resource usage <1% and the deployments appearing quite old. This made me wonder if these might be leftover deployments.

I understand Alpine/Alpha might still be used in some cases (e.g., automation pipelines or isolated testing), so this may very well be intentional. Just wanted to flag the observation in case it helps with environment cleanup or cost/resource optimization. Sharing a screenshot for reference.
