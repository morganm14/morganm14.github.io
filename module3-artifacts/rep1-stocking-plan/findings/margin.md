# Margin memo: spring 2027

Sources: `data/supplier-prices.csv` and `data/orders-fall.csv` (fall 2026, 2026-08-10 to 2026-11-07, 403 line items). No other file was read.

## 1. Method

**What we pay:** new = `our_cost`. Used = `used_buyback_cost`. Rental = `our_cost` (we buy the rental copy new). Digital and non-book items = `our_cost`. **What we charge:** new = `list_price`. Used, rental, digital and non-book items = the fall `unit_price` for that SKU and `format`. Fall records rentals under the format "Used rental". Every SKU and format sold at a single price in fall except Introductory Biology rental: 21 lines at $54.80 and 1 line at $68.50. I used the most common price, $54.80, and noted the range. Every fall line was qty 1 except 12 apparel lines at qty 2, so line counts and unit counts give the same modal price. **Margin per copy** = charge − pay. **Margin %** = margin per copy ÷ charge. **Rental (per semester)**: margin = one-term rental price − (`our_cost` ÷ `rental_copy_semesters`). **Semesters to pay back** = ceil(`our_cost` ÷ rental price). Example, Microeconomics rental: 142.46 ÷ 4 = 35.615, and 75.98 − 35.615 = $40.37 (53.1%). Payback is ceil(142.46 ÷ 75.98 = 1.87) = 2 semesters. Figures are rounded to the cent and to 0.1%.

## 2. Title by title

| title | format | what we pay | what we charge | margin per copy | margin % | notes |
|---|---|---|---|---|---|---|
| Principles of Microeconomics 9th Ed. | New | $142.46 | $189.95 | $47.49 | 25.0% | 10th ed. releases 2027-03-15. 9th ed. not restocked after 2027-02-01. Return window closes 2027-01-09, before classes begin. |
| Principles of Microeconomics 9th Ed. | Used | $57.00 | $142.46 | $85.46 | 60.0% | Same edition change. A used 9th ed. copy bought back after spring may have no resale price. |
| Principles of Microeconomics 9th Ed. | Rental (per semester) | $35.62 / semester ($142.46 ÷ 4) | $75.98 | $40.37 | 53.1% | Pays for itself after 2 semesters (142.46 ÷ 75.98 = 1.87). That is fewer than the 4 `rental_copy_semesters`. **However, the edition change means the copy may get only 1 spring term. If it rents just once, it earns 75.98 − 142.46 = −$66.48.** |
| Statistics Online Homework Access Code | Digital access code | $86.80 | $124.00 | $37.20 | 30.0% | Single-use. Non-returnable once issued. Fall: 74 sold, 11 noted "issued, not yet redeemed". No new, used or rental format exists. |
| Introductory Biology 12th Ed. | New | $102.75 | $137.00 | $34.25 | 25.0% | |
| Introductory Biology 12th Ed. | Used | $41.00 | $102.75 | $61.75 | 60.1% | |
| Introductory Biology 12th Ed. | Rental (per semester) | $25.69 / semester ($102.75 ÷ 4) | $54.80 (range $54.80–$68.50) | $29.11 | 53.1% | Pays for itself after 2 semesters (1.88). That is fewer than 4. At $68.50 (1 fall line), the margin is $42.81 (62.5%). Publisher bills damaged rentals to the store at full cost ($102.75). |
| General Chemistry 8th Ed. | New | $165.75 | $212.50 | $46.75 | 22.0% | Bundled single-use lab code. Firm order, no returns. Minimum order 60. |
| General Chemistry 8th Ed. | Used | not offered | not offered | not offered | not offered | Buyback cost blank. Publisher: "No used or rental market." No fall used sales. |
| General Chemistry 8th Ed. | Rental | not offered | not offered | not offered | not offered | Rental semesters blank. No fall rental sales. |
| Financial Accounting 6th Ed. | New | $126.00 | $168.00 | $42.00 | 25.0% | |
| Financial Accounting 6th Ed. | Used | $50.00 | $126.00 | $76.00 | 60.3% | |
| Financial Accounting 6th Ed. | Rental (per semester) | $31.50 / semester ($126.00 ÷ 4) | $67.20 | $35.70 | 53.1% | Pays for itself after 2 semesters (1.88). That is fewer than 4. |
| Principles of Marketing 14th Ed. | New | $116.06 | $154.75 | $38.69 | 25.0% | |
| Principles of Marketing 14th Ed. | Used | $46.00 | $116.06 | $70.06 | 60.4% | |
| Principles of Marketing 14th Ed. | Rental (per semester) | $29.02 / semester ($116.06 ÷ 4) | $61.90 | $32.89 | 53.1% | Pays for itself after 2 semesters (1.87). That is fewer than 4. |
| Corporate Finance 5th Ed. | New | $172.38 | $221.00 | $48.62 | 22.0% | |
| Corporate Finance 5th Ed. | Used | $66.00 | $165.75 | $99.75 | 60.2% | |
| Corporate Finance 5th Ed. | Rental (per semester) | $43.10 / semester ($172.38 ÷ 4) | $88.40 | $45.31 | 51.3% | Pays for itself after 2 semesters (1.95). That is fewer than 4. |
| Ethics: A Reader | New | $50.40 | $72.00 | $21.60 | 30.0% | Publisher: "Widely available secondhand off campus." |
| Ethics: A Reader | Used | $21.00 | $54.00 | $33.00 | 61.1% | Same off-campus competition. |
| Ethics: A Reader | Rental | not offered | not offered | not offered | not offered | Rental semesters blank. No fall rental sales. |
| Calculus: Early Transcendentals 9th Ed. | New | $194.40 | $243.00 | $48.60 | 20.0% | Return window closes 2027-01-09, before classes begin. |
| Calculus: Early Transcendentals 9th Ed. | Used | $73.00 | $182.25 | $109.25 | 59.9% | |
| Calculus: Early Transcendentals 9th Ed. | Rental (per semester) | $64.80 / semester ($194.40 ÷ 3) | $97.20 | $32.40 | 33.3% | Pays for itself after exactly 2 semesters (194.40 ÷ 97.20 = 2.00). That is fewer than the 3 `rental_copy_semesters`. This is the lowest rental margin, and the copy is assumed to last only 3 terms. |
| TI-84 Plus CE Graphing Calculator | Electronics (new) | $134.99 | $149.99 | $15.00 | 10.0% | Authorized-reseller pricing. Margin is fixed. Non-returnable. |
| Managing AI and Emerging Technology (course packet) | New (printed) | $19.00 | $38.00 | $19.00 | 50.0% | Printed on campus. Any quantity can be reordered in one week. Non-returnable. |
| Xavier Musketeers Hoodie (Size L) | Apparel | $28.00 | $64.00 | $36.00 | 56.3% | Seasonal. Spring order closes 2026-12-15. Non-returnable. |
| Xavier Musketeers Hoodie (Size M) | Apparel | $28.00 | $64.00 | $36.00 | 56.3% | Seasonal. Spring order closes 2026-12-15. Non-returnable. |
| Xavier Musketeers Tee | Apparel | $9.50 | $26.00 | $16.50 | 63.5% | Seasonal. Spring order closes 2026-12-15. Non-returnable. |

## 3. What matters most

1. **The Microeconomics 9th Ed. rental margin depends on the copy renting 4 times, and the edition changes after spring.** The 10th edition releases 2027-03-15, and the 9th is not restocked after 2027-02-01. Spread over 4 semesters, a rental copy earns $40.37 per semester (53.1%). If it rents only in spring 2027, it earns 75.98 − 142.46 = **−$66.48**. Payback takes 2 rentals. The used margin of $85.46 (60.0%) also assumes a buyback copy that may not resell after spring. The new-copy return window closes 2027-01-09, before classes begin on 2027-01-12.
2. **Per copy, used earns about 60% and new earns 20–30% on every textbook that has both.** Examples: Calculus $109.25 used vs $48.60 new; Corporate Finance $99.75 vs $48.62; Microeconomics $85.46 vs $47.49. Rentals earn 51–53% per semester, except Calculus at $32.40 (33.3%). Calculus is the only title spread over 3 semesters instead of 4. These are per-copy figures only. They say nothing about how many copies will sell or what unsold copies cost.
3. **Several products carry fixed or one-way costs that the margin alone does not show.** General Chemistry earns $46.75 (22.0%) per copy, with a 60-copy minimum, a firm order and no returns. The Statistics code earns $37.20 (30.0%) and cannot be returned once issued. The TI-84 earns $15.00 (10.0%), the lowest of any item, and is non-returnable. A damaged Biology rental is billed at $102.75, which wipes out 3.5 semesters of rental margin ($29.11 each).

## 4. What you could not determine

- **Not offered / no price data:** General Chemistry used and rental (supplier fields blank, publisher says no used or rental market, no fall sales). Ethics rental (`rental_copy_semesters` blank, no fall rental sales). Statistics access code in any print format, and TI-84, course packet and apparel in used or rental (not sold that way). No figures were estimated for these.
- **Spring 2027 sell prices.** Every charge figure except new list price is a fall 2026 price. I have nothing that confirms spring prices will be the same.
- **Why one Biology rental sold at $68.50** instead of $54.80. The fall data does not say.
- **How many semesters rental copies actually last, and how many come back damaged.** The rental margins assume each copy rents for the full `rental_copy_semesters` and returns undamaged. My two files do not record return or damage rates.
- **What a Microeconomics 9th Ed. copy (used or rental) is worth after the 10th edition ships.** Neither file gives a post-edition-change price.
- **What a used copy costs once used inventory runs out.** `used_buyback_cost` is a per-copy cost. My files do not say how many used copies we can get at that price.
- **Returns and leftover costs.** This memo gives earnings per copy sold only. It does not cover unsold or returned copies.
