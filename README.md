# Serhii Nikolaichuk

Remote attestation and confidential computing · verifiers written from the specifications, proven on real hardware · Austin, Texas

I work on what a signed statement from a machine actually proves — and what it does not — and on the code that checks it: attestation verifiers for AMD SEV-SNP, Intel TDX and NVIDIA H100 confidential GPUs (AWS Nitro Enclaves in review), the services that act on their results, and measurements that show where the specifications leave room.

## Selected work

**[Vault Genome](https://github.com/vault-genome/vaultgenome-core)** · Go · AGPL-3.0
Open-source continuity for fine-tuned AI models: the model is sealed as a compact genome, its key is released only to hardware that attests, and the restored model is gated EXACT or EQUIVALENT against its own sealed references. Measured on real chips: a failover from a Google Cloud SEV-SNP host to an Azure confidential H100 in 24.99 s; a 32B model restored and gated EXACT on the H100; byte-identical integer inference on an Intel Xeon and an NVIDIA L4; seven of eight adversarial policies refused on the record. Every number is one of [26 verifiable claims](https://github.com/vault-genome/vaultgenome-core/blob/main/VERIFIABLE-CLAIMS.md), each with its evidence files and the command that reproduces it. Releases are signed and reproducible, with SLSA provenance.

**[HATLS](https://github.com/nikolaichuk7/hatls)** · Python · Apache-2.0
Hybrid attested TLS with a continuity mandate: proof that the confidential machine answering you is the same enrolled instance it was at the first message, and detection within one message when it stops being. Measured on AMD SEV-SNP: 2.5 µs per link, about 1 ms per mandate check; no false reject, no accepted impersonation and no accepted relayed exporter in 500 trials each. [Hardware results](https://github.com/nikolaichuk7/hatls/blob/main/docs/HARDWARE-RESULTS.md).

**[geoar-verifier](https://github.com/nikolaichuk7/geoar-verifier)**
A verifier for geographic attestation results and a measured atlas of where a place enters an attestation artifact: AWS Nitro and SEV-SNP with VLEK, Google Cloud SEV-SNP and Intel TDX, Azure SEV-SNP through the paravisor. Every signature checked against the vendor root with independent code, every capture tied to a public nonce. Start with [ATLAS.md](https://github.com/nikolaichuk7/geoar-verifier/blob/main/ATLAS.md).

**[tacra-est](https://github.com/nikolaichuk7/tacra-est)**
Reference implementation, twenty-four ProVerif models and SEV-SNP measurements for the EST profile of TACRA (`draft-novak-lamps-tacra-est`): the attacks the first text admits, and the bindings that close them.

## Standards (IETF)

- Co-author of **[draft-richardson-rats-geographic-results](https://github.com/mcr/geographicresult)**, geographic attestation results in the RATS working group; author of the `basis` proposal — a location claim states which class of artifact it rests on ([pull requests](https://github.com/mcr/geographicresult/pulls?q=author%3Anikolaichuk7)).
- **[draft-nikolaichuk-rats-tap](https://datatracker.ietf.org/doc/draft-nikolaichuk-rats-tap/)**: attestation-gated release of sealed key material, recorded as an auditable object.
- **[draft-nikolaichuk-scitt-continuity-receipts](https://datatracker.ietf.org/doc/draft-nikolaichuk-scitt-continuity-receipts/)**: the recovery of a stateful asset registered as a signed statement in a transparency service.
- Measurements for the SEAT working group, filed in its trackers: the early-attestation binder after a HelloRetryRequest ([#74](https://github.com/yaronf/draft-fossati-seat-early-attestation/issues/74)) and what a "machine identifier" is on three platforms ([use-cases #8](https://github.com/ietf-wg-seat/draft-ietf-seat-use-cases/issues/8)).

## Also built

[GlossPlate](https://glossplate.com), a production menu platform for restaurants (web and Android; Square and Clover point-of-sale integrations end to end), and Entropy Protocol, provenance for AI-generated text. Named inventor on eight USPTO patent applications, drafted and prosecuted myself. Retrieval for AI agents with XERJ: [aiburnclock.org](https://aiburnclock.org), [xerj-plugins](https://github.com/nikolaichuk7/xerj-plugins), [xerj-offline](https://github.com/nikolaichuk7/xerj-offline).

[vaultgenome.com](https://vaultgenome.com) · [IETF datatracker](https://datatracker.ietf.org/person/Serhii%20Nikolaichuk) · [LinkedIn](https://www.linkedin.com/in/serhii-nikolaichuk-9959b2193/)
