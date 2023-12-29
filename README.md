# ByteViper
Proof of concept of how AI could be used by malwares

**DISCLAIMER:** This is a proof of concept for researching how AI could potentially be used by threat actors/adversaries for criminal activities. This source code **_should not to be used_** for malicious purposes. Due to the nature of this code being an open source, if it is ever used, I should not be held liable/responsible for any harm/damages/loss caused by others in any way including using the code for nefarious/criminal purposes, harming/damaging of any nature and any kind.

Introduction:
Malwares comens in various kinds. A typical malware consists of two parts, a dropper and a payload. They would do the following:

1. A dropper gets deployed/installed on a target system during intial access like phishing, compromised accounts etc.
2. The dropper would also establish a communication channel with the adversary (attacker) for further instructions
3. The dropper would have a payload hidden in it (or received by the attacker in some cases) which gets executed by the dropper to perform some set of tasks like privilege escalation, lateral movement, exfiltration etc. depending on what they were programmed to do.

Motivation for ByteViper:
