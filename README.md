# ByteViper
Proof of concept of how AI could be used by malwares

**DISCLAIMER:** _This is a proof of concept and not to be used for malicious purposes. I should not be held responsible for any damages caused by others in any way including changing the code for nefarious/criminal purposes, harmful of any nature and any kind._

Introduction:
Malwares comens in various kinds. A typical malware consists of two parts, a dropper and a payload. They would do the following:

1. A dropper gets deployed/installed on a target system during intial access like phishing, compromised accounts etc.
2. The dropper would also establish a communication channel with the adversary (attacker) for further instructions
3. The dropper would have a payload hidden in it (or received by the attacker in some cases) which gets executed by the dropper to perform some set of tasks like privilege escalation, lateral movement, exfiltration etc. depending on what they were programmed to do.

Motivation for ByteViper:
