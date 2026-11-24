# Checks (sample)

The script runs 77 checks on stories (M codes) and 11 on Wall graphics (W codes). These are 20 of them.

Principle: **FAIL is given only for an exact measurement; a heuristic measurement gives UYARI (warning).** ("FAIL yalnız kesin ölçümde verilir; sezgisel ölçüm UYARI verir.") A wrong FAIL stops a correct story, so an uncertain measurement is never raised to FAIL. A UYARI goes to the auditor, who decides.

A clean script result does not mean the story is correct. It only means the mechanical gates passed. Source fidelity, legal terms and sentence health are checked by the audit.

| Code | What it measures | Result |
|---|---|---|
| M2 | Text band (KUŞAK) top line: max 45 characters, spaces included | FAIL |
| M3 | Text band bottom line: max 75 characters, spaces included | FAIL |
| M11 | Em dash in the output | FAIL |
| M22 | Anchor intro with fewer sentences than required: 3 for voiced and feature stories, 2 for voice-over (DSF) stories | FAIL |
| M26 | Time and date in the story must exist in the source; a different year | FAIL; missing time anchor: UYARI |
| M34 | Anchor intro sentence length: 19–21 words | UYARI; 22 or more: FAIL |
| M48 | Health information next to a death sentence (may read as the cause of death) | UYARI |
| M53 | Question form in the text band | FAIL |
| M62 | A number in the headline that is not in the anchor intro | FAIL; number written in words or low word overlap: UYARI |
| M63 | Speaker's full name in the sentence just before their soundbite | FAIL; surname only, or an empty bridge sentence: UYARI |
| M64 | Clock time in the text band ("11.30") | FAIL; time written in words: UYARI |
| M68 | Quote not found word for word in the raw source (only when the source is given) | UYARI |
| M69 | "suçundan" / "suçlarından" [for the crime] in a detention or court-referral sentence | FAIL |
| M70 | Past record of a suspect ("23 suç kaydı bulunan" [with 23 criminal records]) | UYARI |
| M73 | "geldi" [came] or "burada" [here] outside quotes | UYARI |
| M75 | Singular "Uzman" [expert] or "uzmana göre" [according to the expert] | FAIL; expert's name in the narration: UYARI |
| M76 | "We" in the narration ("görüştüğümüz", "ekibimiz") | FAIL |
| M77 | Sentence before a street interview ends in "anlattı" [described] | FAIL |
| W4 | Wall content: heading and content under each sub-heading; 4 or 5 bullets in a mid-wall | FAIL |
| W9 | Full stop at the end of a Wall bullet | FAIL |
