# Review Notes for the Historical Encryption Research

This report was written in 2025. It documents learning and research, not an implementation, current market survey, or a validated security assessment.

- “Perfect encryption system” and universal protection claims are overstatements. Security depends on configuration, identities, endpoints, operational controls, and the threat model.
- Customer Key adds customer control over root keys for service encryption at rest. It does not make ordinary Microsoft 365 processing inaccessible to Microsoft: customers authorize the service to use keys for functions including search and inspection. See the primary [Customer Key overview](https://learn.microsoft.com/en-us/purview/customer-key-overview).
- Customer Key and Double Key Encryption are distinct designs and must not be conflated.
- Opportunistic transport TLS does not justify “always delivered in ciphertext” for every email route. Requirements depend on the configured mail flow.
- TLS integrity is cipher-suite dependent; the source's blanket HMAC description does not cover all TLS modes.
- Message-encryption experiences differ across products, clients, configuration, and historical versions. An HTML-attachment portal is not a universal description of all current Purview encrypted mail.
- Encryption, signatures, and audit logs support confidentiality, authenticity, and accountability under assumptions. They do not automatically prove legal non-repudiation.
- Workforce forecasts, salary charts, adoption percentages, vendor claims, and national comparisons are historical source claims, not refreshed 2026 facts. A forecast is not a measured outcome.
- “No independent algorithms” and comparisons of national capability are broad claims requiring much more evidence. Adoption of international cryptographic standards is not itself a security weakness.
- Original third-party figures are omitted from this text edition; the remaining discussion references their historical role.
- Bibliography details, product branding, and policy claims were not comprehensively updated. Use current primary documentation for operational decisions.

- The separate security-analysis draft also overstates that all handshake/key-exchange keys are at least 2048 bits: bit lengths are not directly comparable across RSA and elliptic-curve systems. Hashing alone does not authenticate data. Do not infer plaintext confidentiality from storage encryption after an authorized session or endpoint is compromised.
- The analysis inconsistently presents Customer Key as excluding provider access, despite describing a service-mediated model elsewhere. The overview above is the correction; it applies to both historical reports.
