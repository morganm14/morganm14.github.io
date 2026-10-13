# Risk memo: spring 2027 order

Sources: `data/supplier-prices.csv` (14 titles) and `data/returns-log.csv` (43 returns). No other file was read.

## 1. Method

**Unrecoverable money:** a title counts if `returnable_to_publisher` = No, or if `return_window_closes` is before late January 2027. For those titles the exposure is `our_cost` for each unsold copy. **Minimum order cost** = `min_order_qty` × `our_cost`. **Lead times:** I give three dates for each title. (a) When the December order arrives: 2026-12-12 + `lead_time_days`. (b) The last day a reorder can be placed and still arrive by the first day of class: 2027-01-12 − `lead_time_days`. (c) When a reorder arrives if we spot a shortfall on the first day of class: 2027-01-12 + `lead_time_days`. Where it matters I also give the date for a reorder placed when sales data comes in, which I take to be 2027-01-26. **Shelf-life** dates are copied word for word from `publisher_notes`. **Returns:** I grouped `returns-log.csv` by `item` and `reason`, counted the rows, added up `amount_refunded`, and counted the rows where `restocked` = No. `amount_refunded` leaves out costs the store pays to the publisher or replaces in kind. Where I priced those, I used `our_cost` per copy and say so in the row. No order quantities were available to me, so exposure from unsold copies is given per copy and at the minimum order.

## 2. Title by title

Totals across all 14 titles: the minimum orders add up to **$28,451.67**, which is $2,451.67 over the $26,000.00 budget. The minimums on non-returnable titles add up to **$13,276.70**, or 51.1% of the budget.

| title | what could go wrong | exposure in dollars | the date it becomes irreversible | can we undo it after that date |
|---|---|---|---|---|
| Principles of Microeconomics 9th Ed. | **Return window closes 2027-01-09**, three days before classes start and before we know sales. **New edition:** the 10th edition releases 2027-03-15, and the publisher stops restocking the 9th after 2027-02-01. After that, unsold 9th-edition copies cannot go back to the publisher and cannot be reordered, and their resale value as a current text is unknown (buyback cost on file is $57.00, set before the edition change). **Minimum:** 20. **Lead time:** 14 days. The December order arrives 2026-12-26. The last reorder date to arrive for class is 2026-12-29. A reorder placed 2027-01-12 arrives 2027-01-26. A reorder placed 2027-01-26 arrives 2027-02-09, which is after restocking ends on 2027-02-01, so it cannot be filled. **Fall returns:** 3 wrong edition ($522.36) and 2 course dropped ($265.93), all 5 restocked. | $142.46 per unsold copy. Meeting the minimum costs $2,849.20, all of which is unrecoverable after 2027-01-09. | 2027-01-09 (return window). Supply ends 2027-02-01. | No. After 2027-01-09 every unsold copy is ours. After 2027-02-01 we cannot get more copies. |
| Statistics Online Homework Access Code | **Non-returnable.** The column says No; the note says "Non-returnable once issued to a student." **Single use.** **Minimum:** 1. **Lead time:** 0 days, so a reorder arrives the same day. **Fall returns:** 6 "code already redeemed", all denied, $0 refunded, none restocked. 3 course dropped, refunded as $372.00 in store credit, none restocked, so the codes were spent. Pricing those 3 dead codes at our cost gives $260.40, on top of the $372.00 credit owed. | $86.80 per unsold code. The minimum costs $86.80. | 2026-12-12 (order committed) | No, according to the returnable column. The publisher note suggests codes not yet issued might be returnable. I could not confirm that. |
| Introductory Biology 12th Ed. | **Rental damage:** the publisher bills the store "at full cost" for damaged rentals. **Return window:** closes 2027-02-06, after we know sales. **Minimum:** 15. **Lead time:** 21 days. The December order arrives 2027-01-02. The last reorder date to arrive for class is 2026-12-22. A reorder placed 2027-01-12 arrives 2027-02-02. **Fall returns:** 7 "rental returned damaged", recorded as $0.00 refunded, 7 not restocked, all marked "Store billed by publisher." These are real losses that the refund column does not show. At $102.75 our cost they total **$719.25**. At $137.00 list they would total $959.00. | $102.75 per damaged rental. Fall loss: $719.25 at our cost. $102.75 per unsold copy after 2027-02-06. The minimum costs $1,541.25. | 2027-02-06 for unsold stock. Damage billing happens whenever a rental comes back, which runs through the semester. | Unsold copies can be returned until 2027-02-06. Damage bills cannot be undone. |
| General Chemistry 8th Ed. | **Non-returnable:** "Firm order, no returns." The book is bundled with a single-use lab code, and there is "no used or rental market," so an unsold copy recovers nothing. **Minimum:** 60, which costs $9,945.00, or 38.3% of the budget. **Lead time:** 45 days, which means the December order itself arrives **2027-01-26**, two weeks after classes start. To arrive by the first day of class, it would have had to be placed by 2026-11-28, before the 2026-12-12 commit date. A reorder placed 2027-01-12 arrives 2027-02-26. **Fall returns:** 3 damaged in shipping, recorded as $637.50 and handled by replacement, none restocked. At our cost, the replacement copies come to $497.25, unless a carrier or the publisher reimbursed us; the data does not say. 2 course dropped, denied ("lab code issued"), $0 refunded, none restocked. | $165.75 per unsold copy. The minimum costs $9,945.00, all unrecoverable. Fall shipping damage: $497.25 at our cost. | 2026-12-12 (order committed) | No |
| Financial Accounting 6th Ed. | **Return window:** closes 2027-02-06. **Minimum:** 20. **Lead time:** 14 days. The December order arrives 2026-12-26. The last reorder date to arrive for class is 2026-12-29. A reorder placed 2027-01-12 arrives 2027-01-26. **Fall returns:** 2 course dropped ($193.20), both restocked, nothing lost. | $126.00 per unsold copy after 2027-02-06. The minimum costs $2,520.00. | 2027-02-06 | Yes, until 2027-02-06. No after that. |
| Principles of Marketing 14th Ed. | **Return window:** closes 2027-02-20. **Minimum:** 12. **Lead time:** 18 days. The December order arrives 2026-12-30. The last reorder date to arrive for class is 2026-12-25. A reorder placed 2027-01-12 arrives 2027-01-30. **Fall returns:** 1 wrong edition ($154.75), exchanged and restocked. | $116.06 per unsold copy after 2027-02-20. The minimum costs $1,392.72. | 2027-02-20 | Yes, until 2027-02-20. No after that. |
| Corporate Finance 5th Ed. | **Return window:** closes 2027-02-20. **Minimum:** 10. **Lead time:** 18 days. The December order arrives 2026-12-30. The last reorder date to arrive for class is 2026-12-25. A reorder placed 2027-01-12 arrives 2027-01-30. **Fall returns:** none. | $172.38 per unsold copy after 2027-02-20. The minimum costs $1,723.80. | 2027-02-20 | Yes, until 2027-02-20. No after that. |
| Ethics: A Reader | **Competition:** "Widely available secondhand off campus." **Return window:** closes 2027-02-06. **Minimum:** 25. **Lead time:** 21 days. The December order arrives 2027-01-02. The last reorder date to arrive for class is 2026-12-22. A reorder placed 2027-01-12 arrives 2027-02-02. **Fall returns:** 3 "found cheaper elsewhere" ($180.00), all restocked. | $50.40 per unsold copy after 2027-02-06. The minimum costs $1,260.00. I cannot price lost sales to off-campus sellers. | 2027-02-06 | Yes, until 2027-02-06. No after that. |
| Calculus: Early Transcendentals 9th Ed. | **Return window closes 2027-01-09**, before classes start and before we know sales. **Minimum:** 20. **Lead time:** 14 days. The December order arrives 2026-12-26. The last reorder date to arrive for class is 2026-12-29. A reorder placed 2027-01-12 arrives 2027-01-26. Rentals last 3 semesters, where most titles here last 4. **Fall returns:** 4 "found cheaper elsewhere" ($619.65), all restocked; the latest was dated 2026-10-22. Any copy a student returns to us after 2027-01-09 stays on our shelf. | $194.40 per unsold copy. The minimum costs $3,888.00, unrecoverable after 2027-01-09. | 2027-01-09 | No |
| TI-84 Plus CE Graphing Calculator | **Non-returnable to the publisher.** The margin is fixed at $15.00 per unit ($149.99 − $134.99), so one unsold unit ($134.99) wipes out the margin on 9 sold units. **Minimum:** 10. **Lead time:** 30 days. The December order arrives 2027-01-11. The last reorder date to arrive for class is 2026-12-13. A reorder placed 2027-01-12 arrives 2027-02-11. **Fall returns:** 2 "changed mind" ($299.98), both restocked. We took those units back, but we cannot send them back to Texas Instruments. | $134.99 per unsold unit. The minimum costs $1,349.90. | 2026-12-12 (order committed) | No |
| Managing AI and Emerging Technology (course packet) | **Non-returnable,** but "Reorder any quantity, one week." **Minimum:** 5. **Lead time:** 7 days. The December order arrives 2026-12-19. The last reorder date to arrive for class is 2027-01-05. A reorder placed 2027-01-12 arrives 2027-01-19. **Fall returns:** none. | $19.00 per unsold copy. The minimum costs $95.00. | 2026-12-12 (order committed) | No. Reordering is quick, though, so a small first order limits the exposure. |
| Xavier Musketeers Hoodie (Size L) | **Non-returnable.** Seasonal: "Spring order closes 2026-12-15," so no spring reorder is possible. **Minimum:** 24. **Lead time:** 35 days, so a 2026-12-12 order arrives 2027-01-16, four days after classes start. **Fall returns:** 3 wrong size ($256.00), exchanged and restocked. | $28.00 per unsold unit. The minimum costs $672.00. | 2026-12-15 (supplier order closes) | No |
| Xavier Musketeers Hoodie (Size M) | **Non-returnable.** Seasonal: the spring order closes 2026-12-15. **Minimum:** 24. **Lead time:** 35 days, arriving 2027-01-16. **Fall returns:** none. | $28.00 per unsold unit. The minimum costs $672.00. | 2026-12-15 | No |
| Xavier Musketeers Tee | **Non-returnable.** Seasonal: the spring order closes 2026-12-15. **Minimum:** 48. **Lead time:** 35 days, arriving 2027-01-16. **Fall returns:** 2 wrong size ($78.00), exchanged and restocked. | $9.50 per unsold unit. The minimum costs $456.00. | 2026-12-15 | No |

### Returns log grouped by title and reason (fall 2026, 43 rows)

| title | reason | count | amount_refunded | not restocked |
|---|---|---|---|---|
| Calculus: Early Transcendentals 9th Ed. | Found cheaper elsewhere | 4 | $619.65 | 0 |
| Ethics: A Reader | Found cheaper elsewhere | 3 | $180.00 | 0 |
| Financial Accounting 6th Ed. | Course dropped | 2 | $193.20 | 0 |
| General Chemistry 8th Ed. | Course dropped | 2 | $0.00 | 2 |
| General Chemistry 8th Ed. | Damaged in shipping | 3 | $637.50 | 3 |
| Introductory Biology 12th Ed. | Rental returned damaged | 7 | $0.00 | 7 |
| Principles of Marketing 14th Ed. | Wrong edition | 1 | $154.75 | 0 |
| Principles of Microeconomics 9th Ed. | Course dropped | 2 | $265.93 | 0 |
| Principles of Microeconomics 9th Ed. | Wrong edition | 3 | $522.36 | 0 |
| Statistics Online Homework Access Code | Code already redeemed | 6 | $0.00 | 6 |
| Statistics Online Homework Access Code | Course dropped | 3 | $372.00 | 3 |
| TI-84 Plus CE Graphing Calculator | Changed mind | 2 | $299.98 | 0 |
| Xavier Musketeers Hoodie (Size L) | Wrong size | 3 | $256.00 | 0 |
| Xavier Musketeers Tee | Wrong size | 2 | $78.00 | 0 |

**Patterns:**
- **Wrong edition:** 4 returns ($676.11), 3 of them on Microeconomics 9th Ed. That title changes edition on 2027-03-15.
- **Course dropped:** 9 returns. They cost us nothing on Accounting and Microeconomics, where copies were restocked. On the Statistics code and Chemistry they were absorbed, either through store credit or by denying the student.
- **Found cheaper elsewhere:** 7 returns ($799.65), all on Calculus and Ethics.
- **Defective access code:** none were logged under that reason. The 6 "code already redeemed" denials are the closest match.
- **Duplicate purchase:** none logged.

**Losses the refund column hides:** 21 returns were not restocked. Pricing them at our cost:

| item | cost |
|---|---|
| Biology damaged rentals | $719.25 |
| Chemistry shipping-damage replacements | $497.25 |
| Statistics codes spent on dropped students | $260.40 |
| **Total** | **$1,476.90** |

## 3. What matters most

1. **General Chemistry 8th Ed.** has three problems at once:
   - **Size:** the minimum is $9,945.00 (60 × $165.75), 38.3% of the budget.
   - **No way back:** the order is firm and non-returnable, with no used or rental market.
   - **Timing:** the 45-day lead time means even the 2026-12-12 order arrives 2027-01-26, two weeks after classes start. A shortfall reorder arrives 2027-02-26.

   Every unsold copy is a $165.75 loss, and a shortage cannot be fixed before late February.
2. **Microeconomics 9th Ed. and Calculus 9th Ed. have return windows that close 2027-01-09,** before classes start and before we know sales.
   - **Money at stake:** the minimums alone come to $6,737.20 ($2,849.20 + $3,888.00), unrecoverable from that date.
   - **Microeconomics after 2027-02-01:** the publisher stops restocking the 9th edition, so a shortfall found in late January cannot be filled.
   - **Microeconomics after 2027-03-15:** the 10th edition is released, which puts the value of leftover 9th-edition stock in doubt. This is the title that already had 3 wrong-edition returns in fall.
3. **Meeting every publisher minimum costs $28,451.67, which is $2,451.67 over the $26,000.00 budget.** Non-returnable minimums make up $13,276.70 of that. Separately, the fall log hides $1,476.90 in losses that `amount_refunded` records as $0 or as replacements, chiefly 7 Biology rentals the publisher billed at full cost ($719.25). The same exposure applies to every spring Biology rental.

## 4. What you could not determine

- **Order quantities.** I did not have them, so I could not total the spring exposure. Every unsold-copy figure above is per copy or at the minimum. I also cannot say whether any minimum is more than a section needs, because enrollment is not in my data.
- **What "full cost" means on Biology rental damage.** I assumed our cost ($102.75). At list price ($137.00), the fall loss would be $959.00 instead of $719.25.
- **Whether shipping-damaged Chemistry copies were reimbursed** by a carrier or the publisher. If they were, the $497.25 fall loss is lower.
- **Whether unissued Statistics codes can be returned.** The returnable column says No; the note says non-returnable "once issued."
- **What a 9th-edition Microeconomics copy is worth after 2027-03-15,** for buyback, rental, or resale. The data gives only the current $57.00 buyback cost.
- **What students actually paid at the register.** `amount_refunded` sometimes differs from list price; for example, a used Microeconomics return was refunded $142.46, which equals our cost. I reported the refunds as recorded.
- **Format labels on Biology returns.** All 7 are logged as "rental returned damaged," but 1 is labelled New, 2 Used, and 4 Used rental. I cannot tell which format they really were.
- **Return dates.** The log runs to 2026-12-01, which is later than today's date (2026-10-13). I used the rows as given.
- **Whether unsold apparel can be carried into a later season** at its $28.00 / $9.50 cost. If it can, apparel exposure is lower than shown.
- **Lost sales to off-campus sellers** on Ethics and Calculus.
