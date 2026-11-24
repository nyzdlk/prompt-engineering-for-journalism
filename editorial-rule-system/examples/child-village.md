# Case: children's village

Feature story about a children's village in Istanbul reopened to children and families. Names and places are removed.

Rules involved: the narrator is not at the scene ("geldi" / "gitti"), and no empty bridge sentence before a quote.

## 1. "Came" vs "went"

Before (reporter's draft and model output):

> çocuklar, aileleriyle birlikte [çocuk köyü]'ne geldi
> [the children came to [the children's village] with their families]

After (as broadcast): the body says "gitti" [went], the text band says "GİTTİ" [WENT], and the word "Burada" [Here] was deleted.

The reporter's own piece to camera keeps "geldi". That is correct: the reporter speaks from the scene. The narration is read from the studio.

## 2. Empty bridges

The raw text had street interviews, a reporter's piece to camera and more street interviews in a row. Before the deputy mayor's soundbite, one sentence already set the ground:

> "Bir süre aktif olarak kullanılmayan alan, yeniden düzenlenerek çocukların ve ailelerin hizmetine sunuldu."
> [The area, unused for some time, was redesigned and opened to children and families.]

Before: the model put an invented sentence in front of every quote.

> "Muhabir, çocuk köyündeki tatil gününü yerinden anlattı."
> [The reporter described the holiday at the children's village from the scene.]
>
> "Belediye Başkan Vekili, bir çocuk köyünde neler olması gerektiğini anlatıyor."
> [The deputy mayor explains what should be in a children's village.]
>
> "Ailelerden biri, çocuk köyüne ilk kez gelmiyor."
> [One of the families is not coming to the children's village for the first time.]

After: all three were deleted before broadcast.

- The first describes the reporter, who is already on screen and named in the caption.
- The second reports a general opinion, not this event, and leaves the topic hanging with "neler" [what].
- The third says the quote before the quote, and turns the single speaker into "a family".

The same output had also dropped four street interviews; the broadcast version has two street interviews in a row.

These findings became checks: M72 (sentence describing the reporter, FAIL), M63 (bridge with "neler" ending in "anlatıyor" / "anlattı", UYARI) and M73 ("geldi" / "burada", UYARI).
