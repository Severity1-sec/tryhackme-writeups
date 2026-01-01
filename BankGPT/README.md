# BankGPT – TryHackMe Write-Up

## Overview
BankGPT is a TryHackMe room that introduces prompt injection vulnerabilities through an AI-powered banking assistant.  
The chatbot is designed to follow strict security policies and prevent disclosure of sensitive information.

The challenge demonstrates how poorly handled policy enforcement and natural language explanations can become an attack vector.

---

## Objective
The goal of this room is to bypass BankGPT’s security controls and cause it to disclose protected information without directly requesting it.

---

## Initial Observations
Upon interacting with BankGPT, several behaviours stood out immediately:

- The chatbot clearly states that it follows a strict security policy
- Direct requests for sensitive data are denied
- The bot explains *why* certain requests are not allowed

While this may appear secure at first glance, explaining restrictions often reveals internal logic — which can be exploited.

---

## Attack Strategy
Initial direct attempts to obtain sensitive information were unsuccessful, as expected.

Instead of continuing with direct requests, the approach shifted to understanding *how* the chatbot enforces its rules. This involved:

- Asking the chatbot to explain its security policy
- Reframing questions to focus on clarification and summarisation
- Paying attention to how restricted information was referenced, even when not disclosed

By carefully adjusting prompt wording and leveraging the chatbot’s own explanations, it became possible to influence its behaviour and bypass the intended restrictions.

---

## Flag Retrieval
Using the refined prompt approach, the chatbot eventually disclosed the protected information, completing the challenge.

*(The flag itself is intentionally omitted.)*

---

## Key Takeaways
- Prompt injection attacks can succeed without technical exploits
- AI systems may leak sensitive information when explaining their own restrictions
- Defensive AI design must carefully consider how policies are communicated to users

This room highlights why AI-powered systems should be treated as a serious security concern rather than a novelty.
