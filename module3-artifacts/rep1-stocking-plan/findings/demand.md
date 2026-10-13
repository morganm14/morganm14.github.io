# Demand: projected spring 2027 units by title

Analyst: `demand`. Inputs: `data/orders-fall.csv`, `data/enrollment-spring.csv` only.

## Method

`orders-fall.csv` has 403 line items. I summed `qty` by `course` x `sku_or_isbn` x `format`. No row's `notes` marks it cancelled, voided or duplicated (the only notes are "Rental due 2026-12-18" x65, "Code redeemed <date>" x63 and "Code issued, not yet redeemed" x11), and I also found no repeated `order_id`, no fully duplicated row and no row where qty x unit_price differs from total. So **0 rows were excluded as cancelled, voided or duplicate**. I did exclude 42 apparel rows (54 units; SKUs APP-TEE, APP-HOOD-L, APP-HOOD-M), which have no course and are out of scope. That leaves 361 course-tied rows (361 units, all qty 1). Each title was matched to `enrollment-spring.csv` on `sku_or_isbn` = `required_isbn_or_sku`. All 10 courses matched. MATH 151 lists two required items ("978-0-00-000866-0 + ELEC-TI84CE"), so each gets its own row, and both rows use the same course seats. Buy rate = fall units / `seats_fall_2026`. Projected spring units = buy rate x `projected_seats_spring`, rounded half-up to whole units, with the unrounded figure in brackets. Format mix = each format's share of fall units for that title, as observed and not adjusted. Format labels map as follows: New = new, Used = used, Used rental = rental, Digital access code = digital, Electronics = calculator. No safety stock is included and none of this is an order quantity. No customer names or emails were used or copied.

## Title by title

| course | title | fall units | fall seats | buy rate | spring seats | projected spring units | fall format mix |
|---|---|---|---|---|---|---|---|
| ACCT 220 | Financial Accounting 6th Ed. (978-0-00-000422-1) | 31 | 56 | 0.5536 (55.4%) | 62 | **34** (34.32) | new 26% / used 48% / rental 26% (8 / 15 / 8) |
| BIOL 110 | Introductory Biology 12th Ed. (978-0-00-000207-3) | 48 | 68 | 0.7059 (70.6%) | 72 | **51** (50.82) | new 25% / used 29% / rental 46% (12 / 14 / 22) |
| CHEM 115 | General Chemistry 8th Ed. (978-0-00-000315-9) | 22 | 30 | 0.7333 (73.3%) | 52 | **38** (38.13) | new 100% (22) |
| ECON 201 | Principles of Microeconomics 9th Ed. (978-0-00-000101-4) | 61 | 92 | 0.6630 (66.3%) | 104 | **69** (68.96) | new 49% / used 34% / rental 16% (30 / 21 / 10) |
| FINC 300 | Corporate Finance 5th Ed. (978-0-00-000644-4) | 15 | 36 | 0.4167 (41.7%) | 40 | **FLAG: text not confirmed. Left blank.** | fall: new 27% / used 27% / rental 47% (4 / 4 / 7) |
| MATH 151 | Calculus: Early Transcendentals 9th Ed. (978-0-00-000866-0) | 26 | 74 | 0.3514 (35.1%) | 78 | **27** (27.41) | new 23% / used 23% / rental 54% (6 / 6 / 14) |
| MATH 151 | TI-84 Plus CE Graphing Calculator (ELEC-TI84CE) | 18 | 74 | 0.2432 (24.3%) | 78 | **19** (18.97) | calculator 100% (18) |
| MGMT 342 | Managing AI and Emerging Technology, course packet (PKT-MGMT342) | 20 | 22 | 0.9091 (90.9%) | 24 | **22** (21.82) | new 100% (20) |
| MKTG 230 | Principles of Marketing 14th Ed. (978-0-00-000538-6) | 19 | 40 | 0.4750 (47.5%) | 44 | **21** (20.90) | new 32% / used 47% / rental 21% (6 / 9 / 4) |
| PHIL 100 | Ethics: A Reader (978-0-00-000751-9) | 27 | 100 | 0.2700 (27.0%) | 108 | **29** (29.16) | new 41% / used 59% (11 / 16) |
| STAT 210 | Statistics Online Homework Access Code (DIG-STAT-2041) | 74 | 88 | 0.8409 (84.1%) | 96 | **81** (80.73) | digital 100% (74) |

Total projected across the 10 projected rows: 391 units (unrounded sum 391.17). FINC 300 is not included in that total. Percentages in the mix column are rounded to whole numbers, so some rows sum to 99% or 101%. The unit counts in brackets are exact.

`text_status` and `notes` in `enrollment-spring.csv`, read in full:
- FINC 300 is "Not confirmed" ("Instructor has not confirmed the text for spring."). It is flagged above.
- Every other title is "Confirmed".
- CHEM 115: "Second section added for spring."
- MATH 151: "Graphing calculator required."
- STAT 210: "Access code required for the online homework system."

No spring title is marked new, changed edition or dropped. Every spring SKU/ISBN appears in fall sales.

## What matters most

1. **CHEM 115 nearly doubles.** Seats go from 30 to 52 (+22, +73%) because a second section was added. At the fall buy rate of 73.3%, projected units go from 22 to 38 (38.13). Fall sold only new copies (22 of 22), so the observed mix puts all 38 in new. That is the largest absolute and relative change of any title.
2. **Buy rates vary more than threefold, so seats are not demand.** The rate is 27.0% for PHIL 100 (27 units on 100 seats), 35.1% for the MATH 151 text and 24.3% for the calculator, compared with 84.1% for STAT 210 and 90.9% for MGMT 342. Ordering one copy per seat for PHIL 100 would mean 108 units against a projection of 29. For the MATH 151 text it would mean 78 against 27.
3. **FINC 300 has no projection.** The text is not confirmed for 40 spring seats. In fall the same ISBN sold 15 units on 36 seats (41.7%), but that history only applies if the instructor confirms 978-0-00-000644-4 again. I have not projected it.

## What you could not determine

- **FINC 300 spring demand.** The text is not confirmed, so the projection is blank. I did not borrow another title's rate.
- **Whether fall sales are complete or final.** 36 of the 403 rows (31 of them course-tied) have `order_date` after today, 2026-10-13. The latest is 2026-11-07, and 3 code-redemption dates also fall after today. I cannot tell from these two files whether those rows are scheduled, pre-recorded or mis-dated. I counted them as sales because nothing marks them cancelled. If they should not count, buy rates fall for BIOL 110 (7 rows), MKTG 230 (5), STAT 210 (5), CHEM 115 (3), PHIL 100 (3), ECON 201 (3), MATH 151 (2), ACCT 220 (2) and MGMT 342 (1). Late-term buyers who have not purchased yet are also not visible.
- **STAT 210 codes not redeemed.** 11 of the 74 access codes are noted "Code issued, not yet redeemed". I counted them as sold because they are not marked voided. If they are later voided or refunded, fall units would be 63 and the buy rate 71.6%.
- **Whether the format mix reflects preference or availability.** CHEM 115 and MGMT 342 sold 100% new, and STAT 210 and the calculator each sold in only one format. The orders file does not show whether used or rental copies were offered for those titles, so I cannot tell what students would have chosen.
- **Edition continuity.** `enrollment-spring.csv` gives course titles and ISBNs but no editions. I matched on ISBN, which suggests the same edition. Nothing in my two files confirms that publishers will not move to a new edition before January.
- **Whether spring behaves like fall.** Every rate here is a single-term fall rate. Spring may differ, for example because students already own the book from fall or the course mix is different, and I have no prior spring data to test that.
- **Rental returns.** 65 rental units are due back 2026-12-18. These files do not show how many will come back in rentable condition. That is a supply question, not a demand one, and it is outside my data.
