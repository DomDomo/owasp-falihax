
[comment]: # (Generated from JSON file by generate_feedback_md.py)
[comment]: # (Intended to be read in GitHub's markdown renderer. Apologies if the plaintext formatting is messy.)

# DomDomo's OWASP Falihax Hackathon Feedback
*Marked by [CyberSoc](https://cybersoc.org.uk/?r=falihax-marking-domdomo)*

This is DomDomo's specific feedback. See below for the full vunerability list, including ones you may have missed.

[General hackathon feedback with full vulnerability list and solutions](https://github.com/CyberSoc-Newcastle/owasp-falihax/blob/main/VULNS.md)
## Summary
**Total mark:** 30

A good attempt at securing the web app. While there are further ways to improve the security, your version is definitely a vast improvement on the original! Nice work!

## Marking Scheme Used
We used the following marking scheme to award marks for each vulnerability, where the mark awarded for the vulnerability is the highest row in the following table fulfilled by your solution. A tick means you had to have done this to get the mark, a cross means this mark does not apply if you did this, and a dash means this is ignored for this possible mark. This mark scheme was decided after the entries had been submitted and was not known to entrants during the competition, although hints were provided as to what to include for good marks.

For each vulnerability, this is how many marks we would award:
| State a valid vulnerability | Show where it is in code | Demo it | Describe how it could be mitigated | Attempt a reasonable fix | Fix works | Explain your fix | Marks |
|-----------------------------|--------------------------|---------|------------------------------------|--------------------------|-----------|------------------|-------|
| ✔                           | ❌                        | ❌       | ❌                                  | ❌                        | -         | -                | 1     |
| ✔                           | ✔                        | ❌       | ❌                                  | ❌                        | -         | -                | 2     |
| ✔                           | -                        | ✔       | ❌                                  | ❌                        | -         | -                | 3     |
| ✔                           | -                        | -       | ✔                                  | ❌                        | -         | -                | 4     |
| ✔                           | -                        | -       | -                                  | ✔                        | ❌         | -                | 4     |
| -                           | -                        | ❌       | -                                  | ✔                        | ✔         | ❌                | 5     |
| -                           | -                        | ✔       | -                                  | ✔                        | ✔         | ❌                | 6     |
| -                           | -                        | -       | -                                  | ✔                        | ✔         | ✔                | 7     |

## Vulnerabilites Found
### [A01-01: Unauthorised users are allowed to visit secure pages](https://github.com/CyberSoc-Newcastle/owasp-falihax/blob/main/VULNS.md#a01-01-unauthorised-users-are-allowed-to-visit-secure-pages)
| State | Show | Demo | Mitigate | Attempt fix | Fix works | Explain fix | Mark |
|-------|------|------|----------|-------------|-----------|-------------|------|
| ✔     | ❌    | ❌    | ❌        | ✔           | ✔         | ❌           | 5    |


### [A01-02: No access control/owner check on account page](https://github.com/CyberSoc-Newcastle/owasp-falihax/blob/main/VULNS.md#a01-02-no-access-control/owner-check-on-account-page)
| State | Show | Demo | Mitigate | Attempt fix | Fix works | Explain fix | Mark |
|-------|------|------|----------|-------------|-----------|-------------|------|
| ❌     | ❌    | ❌    | ❌        | ✔           | ✔         | ❌           | 5    |

This bug is successfully fixed [here](https://github.com/DomDomo/owasp-falihax/blob/c26c74decf3fed26c8cc6755e5a84bda4ab18903/app.py#L463-L476), however it would have been more efficient (and saved you some time) to use the [`get_accounts()`](https://github.com/DomDomo/owasp-falihax/blob/c26c74decf3fed26c8cc6755e5a84bda4ab18903/app.py#L389-L434) function to retrieve sort codes and account numbers for the user!


### [A01-03: No access control on the admin page](https://github.com/CyberSoc-Newcastle/owasp-falihax/blob/main/VULNS.md#a01-03-no-access-control-on-the-admin-page)
| State | Show | Demo | Mitigate | Attempt fix | Fix works | Explain fix | Mark |
|-------|------|------|----------|-------------|-----------|-------------|------|
| ❌     | ❌    | ❌    | ❌        | ✔           | ✔         | ❌           | 5    |


### [A02-01: Unsuitable use of ROT-13 "encryption"](https://github.com/CyberSoc-Newcastle/owasp-falihax/blob/main/VULNS.md#a02-01-unsuitable-use-of-rot-13-encryption)
| State | Show | Demo | Mitigate | Attempt fix | Fix works | Explain fix | Mark |
|-------|------|------|----------|-------------|-----------|-------------|------|
| ✔     | ❌    | ❌    | ❌        | ✔           | ✔         | ❌           | 5    |


### [A03-01: SQL Injection](https://github.com/CyberSoc-Newcastle/owasp-falihax/blob/main/VULNS.md#a03-01-sql-injection)
| State | Show | Demo | Mitigate | Attempt fix | Fix works | Explain fix | Mark |
|-------|------|------|----------|-------------|-----------|-------------|------|
| ✔     | ❌    | ❌    | ❌        | ✔           | ✔         | ❌           | 5    |


### [A04-02: No Password Strength Checks](https://github.com/CyberSoc-Newcastle/owasp-falihax/blob/main/VULNS.md#a04-02-no-password-strength-checks)
| State | Show | Demo | Mitigate | Attempt fix | Fix works | Explain fix | Mark |
|-------|------|------|----------|-------------|-----------|-------------|------|
| ✔     | ❌    | ❌    | ❌        | ✔           | ✔         | ❌           | 5    |

Related to this, you could also have implemented some kind of rate-limiting (A04-03) which would improve the resistance to brute force attacks.

## Total mark
5 + 5 + 5 + 5 + 5 + 5 = 30

**Your total mark is 30**