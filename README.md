# ByteViper
Proof of concept of how AI could be used by malwares

**DISCLAIMER:** This is a proof of concept for researching how AI could potentially be used by threat actors/adversaries for criminal activities. This source code **_should not to be used_** for malicious purposes. Due to the nature of this code being an open source, if it is ever used, I should not be held liable/responsible for any harm/damages/loss caused by others in any way including using the code for nefarious/criminal purposes, harming/damaging of any nature and any kind.

$${\color{lightgreen}Introduction:}$$
Malwares comes in various kinds. A typical malware consists of two parts, a dropper and a payload. They would do the following:

1. A dropper gets deployed/installed on a target system during intial access like phishing, compromised accounts etc.
2. The dropper would also establish a communication channel with the adversary (attacker) for further instructions
3. The dropper would have a payload hidden in it (or received by the attacker in some cases) which gets executed by the dropper to perform some set of tasks like privilege escalation, lateral movement, exfiltration etc. depending on what they were programmed to do.

Malware developers use plenty of techniques to hide their precious payloads. The dropper without a payload is mostly benign which is why its precious. Its, the payload that performs most of the nefarious tasks. Hence, malware authors go through a lot of trouble to hide their payload from being detected by EDRs, AVs, threat hunters etc. Some of the common techniques used are obfuscating and encrypting the payload and unobfuscating/decrypting just-in-time when the payload has to be executed. This means the deobfucation logic or decryption secrets are also normally inside the dropper itself. There is a serious drawback though. Obfuscating/encrypting increases the entropy of the malware binary significantly. This increase in entropy becomes a red flag in the prying eyes of EDRs/AVs. That means, even if the EDR/AV cannot read the encrypted/obfucated payload, the binary gets flagged for further inspection because of its high entropy. However, malware authors do attempt to use variety of techniques to reduce the entropy as well. But there is no guarantee and the entropy may not go down significantly down as well.

Malware detections have evolved overtime and today's machine learning (AI) based detection tools like EDRs are extremely powerful in detecting malicous activities because they are not based on static rules but they are trained to detect malicous behaviors when a piece of code run. In fact, evading AI based EDRs are rare and malware authors are actively researching ways to bypass them.

**Motivation for ByteViper:**
Since AI is used by malware detection tools (defensive security), it should also possible to have a malware that uses AI to evade these intelligent EDRs. With AI in malwares, things change a lot for both offensive and defensive security. It levels the field. Its not easy anymore for EDRs/AVs to detect an AI based malware. It becomes a battle between intelligent systems.

**How does ByteViper work:**
This section is the most interesting piece that everyone would be interested in. ByteViper has 2 parts, a AI module and a dropper. The AI module is python based and uses Sentence Transformers to supply the payload to the dropper. The dropper is a simple C program that executes the payload. The dropper could use just about any techniques to run the payload including remote execution.
