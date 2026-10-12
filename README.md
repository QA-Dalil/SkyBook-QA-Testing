<div align="center">

# SkyBook QA Testing

**Manual testing for a flight-booking application**

7 epics · 20 user stories · 37 test cases · 24 reported bugs

![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)
<a href="https://smartbear.com/product/zephyr/"><img src="https://dka575ofm4ao0.cloudfront.net/pages-transactional_logos/retina/807039/ZephyrEssential_Full-CLRRGB-6e8f6f45-0c04-4a06-953e-c5910c39262c.png" alt="Zephyr Essential by SmartBear" height="28"></a>
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)

I tested the [SkyBook practice booking app](https://claude.ai/code/artifact/5028f8a7-4747-4b7e-b07f-a4dddf65807c) from flight search through checkout, then documented the results and linked defects to the affected stories and test cases.

**[View results](#test-results)** · **[Browse project files](#project-files)** · **[See evidence](#test-evidence)**

</div>

## Test results

**37 cases:** 16 PASS · 20 FAIL · 1 BLOCKED. Executed on **7 September 2026** using positive, negative, boundary, and end-to-end scenarios across search, passenger details, seats, extras, payment, and confirmation.

`TC-6.3-01` was BLOCKED: the displayed arithmetic could be checked, but the UI did not show the individual child fare or tax calculation needed to verify the full pricing rule.

## Testing highlights

- **Booking validation:** Found accepted past dates, zero adults, duplicate seats, negative baggage, repeated promo discounts, and incomplete payment details. The [test case CSV](test-cases/SkyBook_Test_Cases.csv) records steps, expected and actual results, and status.
- **Seat boundary:** In BUG-14, **Continue to extras** was enabled while only one of two passengers had a seat. The [bug CSV](bugs/SkyBook_Bug_Reports.csv) contains reproduction steps and expected versus actual behavior; the [Jira record](screenshots/BUG-14-details-and-results.png) shows links to `US-4.2` and `TC-4.2-01`.
- **Traceability:** Connected Epic → Story → Test Case → Bug so a failed result can be followed back to its requirement in the [traceability matrix](traceability/SkyBook_Traceability_Matrix.csv).

## Tools used

- **Jira** — requirements, stories, defect tracking, and links between work items.
- **Zephyr Essential** — test case management and execution evidence.
- **Excel** — the QA workbook and detailed traceability matrix.

## Project files

- [QA workbook](SkyBook_QA_Project.xlsx) — test cases, execution results, defects, and summary.
- [Test cases CSV](test-cases/SkyBook_Test_Cases.csv) · [Bugs CSV](bugs/SkyBook_Bug_Reports.csv) · [Traceability CSV](traceability/SkyBook_Traceability_Matrix.csv) · [Detailed traceability workbook](traceability/SkyBook_Traceability_Matrix_Detailed.xlsx)
- [Screenshot evidence gallery](screenshots/README.md) — Jira, Zephyr, application, and workbook images.

## Test evidence

Zephyr shows the test library organized by Epic. The Jira summary shows the project work items. The application screenshot captures BUG-14 with the Continue button enabled before all passengers have seats.

![Zephyr test case library](screenshots/zephyr-test-library.png)

![Jira project summary](screenshots/jira-project-summary.png)

![BUG-14: Continue enabled with one of two passengers seated](screenshots/BUG-14-skybook-enabled-continue-button.png)
