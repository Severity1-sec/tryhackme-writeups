# BankGPT – TryHackMe Write-Up

## Room Overview
BankGPT is a TryHackMe room focused on prompt injection attacks against an AI-powered banking assistant.  
The chatbot is designed to follow strict security policies and avoid revealing sensitive information.

---

## Objective
The goal of this room is to bypass the chatbot’s security controls and retrieve protected information.

---

## Initial Observations
During initial interaction, the chatbot:
- Clearly follows a defined security policy
- Refuses direct requests for sensitive data
- Explains why certain requests are not allowed

This behaviour is important, as explaining restrictions can unintentionally reveal how a system reasons.

---

## Attack Approach
Direct attempts to request sensitive information were unsuccessful.

Instead, the approach shifted to:
- Asking questions about the security policy itself
- Reframing prompts to focus on explanation rather than extraction
- Leveraging the chatbot’s own responses to infer how restrictions were enforced

By carefully adjusting the wording of prompts, it was possible to bypass the intended restriction.

---

## Flag Retrieval
Using the refined prompt approach, the chatbot revealed the protected information, completing the challenge.

*(The flag itself is intentionally not included.)*

---

## Lessons Learned
- AI systems can leak sensitive information when explaining their own restrictions
- Prompt injection does not require traditional exploits — language alone can be enough
- AI security must consider how policies are communicated to users

This room highlights AI systems as an emerging attack surface.
