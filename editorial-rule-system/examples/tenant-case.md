# Case: the tenant

Voiced story: a landlord in an Istanbul district says a tenant did not pay rent and covered the walls, doors and kitchen cupboards of the flat with love poems. The landlord's lawyer speaks on camera. Names and places are removed.

Rules involved: do not trim a quote, and keep the cause the source gives.

## 1. Trimming the quote

The lawyer's statement had eight sentences. One output split it into three soundbites and dropped the first two sentences, a middle sentence and the last sentence. That is trimming, not splitting.

The last four sentences of the statement in the source:

> "Kiracıyı tahliye etti fakat yasal yollarımız sürüyor. Hem tahsil edemediğimiz kira açısından takipteyiz hem de her yere yazdığı yazılar sebebiyle 'eve zarar verme' ve 'güveni kötüye kullanma' suçlarından dava ve takip sürecimiz devam ediyor. Zararlarımızı tazmin edeceğiz. Hukuki süreç bu şekilde sürüyor"
> [The tenant has moved out, but our legal action continues. We are pursuing the unpaid rent, and because of the writing everywhere, our case for 'damage to the property' and 'breach of trust' continues. We will recover our losses. The legal process continues this way.]

The same part in a model draft, with the middle and last sentences cut:

> "Hem tahsil edemediğimiz kira açısından takipteyiz hem de her yere yazdığı yazılar sebebiyle 'eve zarar verme' ve 'güveni kötüye kullanma' suçlarından dava ve takip sürecimiz devam ediyor. Zararlarımızı tazmin edeceğiz."

The right way: split the statement at sentence boundaries so that the parts together cover all of it, word for word. If it is too long, the model writes a note under the story; only the editor shortens a quote.

## 2. Keeping the cause

The source gave the reason for the writing: "Kız arkadaşım cezaevindeydi" [My girlfriend was in prison].

- Wrong: "Şiirleri kız arkadaşı için yazdı." [He wrote the poems for his girlfriend.] This changes the cause into the addressee and drops the prison detail that makes the story.
- Right: "Kız arkadaşı cezaevinde olduğu için yazdığını söyledi." [He said he wrote them because his girlfriend was in prison.]

## 3. Unnecessary attribution

<!-- TODO: Niyazi fills in: the real before/after sentence for the unnecessary attribution ("gereksiz atıf") in this case. -->

## Evaluation note

The same test was used to check the evaluators. One evaluator ranked its own text first and missed its own errors; another called its own text "legally the strongest" while it broke red line 34. See [testing.md](../testing.md).
