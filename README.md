
Quick update on the investigation:
The issue appears to be specific to a particular scenario and does not seem recent. Based on available data (TTL in Flight DB limits visibility to 7 days), it looks like this may have been occurring for some time.
To confirm historical impact, it would help if we can check whether CheckoutAir plugin DB retains older records of FSS responses (especially cases where checkoutTotal size = 4).
Regarding the fix — the change is non-trivial and will require design discussion, multi-team review, and release cycle alignment.
Current ETA: ~2 weeks (subject to refinement after design discussions).
