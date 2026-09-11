# Serhii Nikolaichuk

Remote attestation and confidential computing · standards and working code · Austin, Texas

I work on what a signed artifact from a machine actually proves, and on how a relying party should read it. I write the specifications and the code that checks them.

## Standards (IETF)

- Co-author of **[draft-richardson-rats-geographic-results](https://datatracker.ietf.org/doc/draft-richardson-rats-geographic-results/)**, the geographic attestation results draft in the RATS working group. Author of the `basis` proposal: a location claim states which class of artifact it rests on, measured by the attester, asserted by the operator, or concluded by another verifier ([PRs #6, #7, #9](https://github.com/mcr/geographicresult/pulls)).
- **[draft-nikolaichuk-rats-tap](https://datatracker.ietf.org/doc/draft-nikolaichuk-rats-tap/)**, Trusted Artifact Provenance: attestation-gated release of sealed key material, recorded as an auditable object.
- **[draft-nikolaichuk-scitt-continuity-receipts](https://datatracker.ietf.org/doc/draft-nikolaichuk-scitt-continuity-receipts/)**, registering the recovery of a stateful asset as a signed statement in a transparency service.

## Working code

- **[geoar-verifier](https://github.com/nikolaichuk7/geoar-verifier)**, a verifier for geographic attestation results and a measured atlas of where a place enters an attestation artifact: AWS Nitro and SEV-SNP with VLEK, Google Cloud SEV-SNP and Intel TDX, Azure SEV-SNP through the paravisor. Every signature checked against the vendor root with independent code, every capture tied to a public nonce. Start with [ATLAS.md](https://github.com/nikolaichuk7/geoar-verifier/blob/main/ATLAS.md).
- **[aiburnclock.org](https://aiburnclock.org)**, a daily index of what AI agents waste by reading whole files they never use, priced against published budgets: public sources, open formula, a dated release for every state. Source in [aiburnclock](https://github.com/nikolaichuk7/aiburnclock).
- **[xerj-offline](https://github.com/nikolaichuk7/xerj-offline)**, **[xerj-plugins](https://github.com/nikolaichuk7/xerj-plugins)**, **[arp-9200](https://github.com/nikolaichuk7/arp-9200)**: retrieval for AI agents over the Elasticsearch API on port 9200 (XERJ): an assistant that works offline, Claude Code plugins, protocol notes.

## Products and IP

Founder of [The Capital Index](https://thecapitalindex.com), a small studio in Austin. Shipped **[GlossPlate](https://glossplate.com)** (web, iOS and Android; Square and Clover POS integrations), **Entropy Protocol** (five-layer provenance for AI-generated text, built against EU AI Act Article 50) and **[ShelvesLab](https://shelveslab.com)** (privacy-preserving edge sensing on ESP32-S3). Named inventor on eight USPTO patent applications, sole inventor on four; I draft and prosecute the filings myself.

Product code lives in private repositories, as these are operating companies with pending patents. The attestation work above is public and reproducible.

[IETF datatracker](https://datatracker.ietf.org/person/nikolaichuk.s.f@gmail.com) · [thecapitalindex.com](https://thecapitalindex.com) · [LinkedIn](https://www.linkedin.com/in/serhii-nikolaichuk-9959b2193/)
