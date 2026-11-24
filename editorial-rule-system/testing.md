# Testing

Every rule change passes the same tests before it is used.

## 1. Example test

All 47 gold-standard examples (*altın numune*) are run through the script. The result must be zero FAIL.

## 2. Counter test

Every new check must miss the error with the old script and catch it with the new one. This proves the check measures what it claims. Current result: 134/134.

## 3. Crash test

The script is run on 900 broken inputs. It must not crash.

## 4. Clean-copy test

The package is unzipped into a clean folder and the whole chain is run from the start.

## 5. Multi-model evaluation rules

When several models write the same story and models also grade the results:

- **The evaluator declares its own text.** If one of the texts is its own output, it says so at the top of the report and counts its own violations first, with the same rule list.
- **Every criticism carries a rule number.** A finding that lowers the score cites a red line or a check code ("red line 22", "M24").
- **Editorial preference does not lower the score.** An observation without a rule number goes under "editorial preference" and does not count. What the rules leave free (for example 4 text-band pairs instead of 3) is not a fault.
- **Known evaluator errors** seen again and again in real tests:
  - asking for the incident date in a crime story, where the exact date is not written
  - counting the city-name police form ("İstanbul Polisi" [Istanbul Police]) as an error
  - putting two statements side by side that the source does not link, and calling it a contradiction
  - merging three different findings into one ("missing", "only in the soundbite", "may be misheard")
  - applying the same criterion with different weight to different texts, including its own
  - inventing a grammar rule
  - counting as a fault what a rule requires
  - calling a line "too long" without counting the characters
