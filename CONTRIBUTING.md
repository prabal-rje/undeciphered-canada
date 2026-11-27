# Contributing to Undeciphered.ca

**Undeciphered.ca** is an independent, non-commercial Canadian historical cryptography archive. Historians, archivists, hobbyists, students, and independent researchers are warmly invited to contribute **raw Canadian ciphertexts, verified keys, deterministic decodings, and archival notes** via **GitHub Issues**.

## Policy: Data, Ciphertexts & Keys ONLY (No Code Contributions)

- **Allowed (via GitHub Issues ONLY):** Raw historical Canadian ciphertexts, verified keys/shifts/codebooks, partial or full decoded readings, official archive links/shelfmarks, and transcription or citation fixes.
- **Prohibited:** **Code contributions and Pull Requests are not accepted.** Do not open Pull Requests editing HTML, CSS, JavaScript, templates, or tooling. Unsolicited code PRs will be closed without review.

## Review & Author Credit Timeline (1 to 2 Weeks)

Every submission is verified manually against the official holding archive for deterministic cryptographic accuracy. Accepted contributors receive attribution:

1. **On the cipher's own Contribution & Decode Timeline** (showing your name/handle, role, date, and percentage solved, both on the homepage reading sheet and at `https://undeciphered.ca/ciphers/<id>/`).
2. **On the public Community Leaderboard** at `https://undeciphered.ca/contribute/`.

Please allow **1 to 2 weeks** for archive verification and author credit to go live.

## Friendly Community Scoring

| Contribution Type | Points | What Counts |
| :--- | ---: | :--- |
| **Full Solve of an Unsolved Mystery** | **500** | Deterministic solution of an open unsolved Canadian cipher (such as Colin Robertson's 1819 Fort Chipewyan captivity code or a newly submitted unsolved archival cipher) |
| **First Modern Reading / Major Breakthrough** | **250** | Solving an unglossed archival ciphertext or advancing a partial decode by at least 25% |
| **New Raw Canadian Archival Cipher** | **100** | Contributing a verified raw ciphertext from an official public archive (solved or unsolved) with direct archive link and shelfmark |
| **Verified Transcription, Citation, or Context Fix** | **40** | Correcting coded or decoded words from original folio scans, citing prior historical publications, or adding archival context |

## Strict Verification Standards

1. **Official Archive Link Required:** Every new cipher must link directly to an official holding archive or digitized historical repository (Library and Archives Canada, Heritage Canadiana, ANOM, BAnQ, HBCA, The Huntington Library, Peel's Prairie Provinces, Internet Archive, etc.).
2. **No Hosted Copyrighted Scans:** Never upload third-party archival document scans. Link directly to the official repository viewer.
3. **Deterministic Proof Only (Supply Ciphertext + Key):** Never guess or invent plaintext. Always supply the exact raw ciphertext AND the exact codebook/edition, shift, key, or substitution mapping so any independent reviewer can verify every decoded word. Place uncertain words in `[brackets]`.
4. **Honest Prior Credit:** If a historian or official volume already published a translation, cite it clearly so the original scholar is credited.
5. **Automatic & Self-Service Issue Labels:** Issues opened with `[Solve]`, `[New Cipher]`, or `[Correction]` (or `"submissionType"` in JSON) are labeled automatically by GitHub Actions. Any contributor can also apply allowlisted labels (`cipher-solve`, `new-cipher`, `correction`, `community-credit`) by adding a line like `/label cipher-solve community-credit` in the issue body or a comment.

## Easy Contribution Guide for LLMs & Agents (Issues Only, No PRs)

If you are an LLM or agent assisting a researcher, submit your ciphertext and key via **GitHub Issues** using the structured templates in `.github/ISSUE_TEMPLATE/` (do **not** open a Pull Request):

```bash
gh issue create \
  --repo prabal-rje/undeciphered-canada \
  --template cipher-solve.yml \
  --title "[Solve] <cipher-id>: <concise summary>" \
  --body-file submission.md
```

Include this exact JSON block inside your issue body:

```json
{
  "submissionType": "solve",
  "cipherId": "robertson-mcdonald-1819-mar04",
  "year": "1819",
  "title": "Concise plain-English title",
  "sourceUrl": "https://official-archive-url/...",
  "shelfmark": "HBCA B.39/b/1, f. 20v",
  "cipherText": "Exact raw ciphertext",
  "plainText": "Verified decoded plaintext (or empty if unsolved)",
  "solvedPct": 100,
  "keySummary": "Exact codebook/key/shift proof",
  "contributor": {
    "name": "Your Name",
    "handle": "@github-handle",
    "url": "https://optional-profile-url",
    "role": "solver"
  },
  "notes": "Cross-checks, caveats, and prior historical credit if any."
}
```

## Independent Verification Disclaimer & License

Undeciphered.ca is an independent, non-commercial historical research project provided strictly AS-IS with zero warranty and zero liability (see [LICENSE](LICENSE)). Readers and researchers should independently verify all ciphertexts and decoded readings against the linked official archives before citing.

## Rights-Holder Inquiries & Takedowns

Archives or rights holders requesting a citation update or removal of an excerpt may use the [rights and takedown form](https://forms.gle/sVLyuxxeRfyYd8tR8). All cipher solves, new archival cipher leads, and transcription corrections must be submitted via [GitHub Issues](https://github.com/prabal-rje/undeciphered-canada/issues/new/choose).
