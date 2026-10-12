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

**37 cases:** 16 PASS · 20 FAIL · 1 BLOCKED. Testing covered functional flows, negative inputs, boundary values, and end-to-end booking. The blocked case could verify the displayed fare arithmetic, but the UI did not expose enough detail to verify the child fare and tax rules.

## Testing highlights

- **Booking validation:** Tested dates, passenger counts, sorting, filters, payment fields, seat assignment, baggage, and promo codes. The [execution report](docs/EXECUTION_REPORT.md) records expected and actual results for each case.
- **Seat boundary:** In BUG-14, **Continue to extras** was enabled while only one of two passengers had a seat. The [bug report](docs/BUG_REPORTS.md) and [Jira screenshot](screenshots/BUG-14-details-and-results.png) show the reproduction steps and links to `US-4.2` and `TC-4.2-01`.
- **Traceability:** Connected Epic → Story → Test Case → Bug so a failed result can be followed back to its requirement.

## Tools used

- **Jira** — requirements, stories, defect tracking, and links between work items.
- **Zephyr Essential** — test case management and execution evidence.
- **Excel** — the QA workbook and detailed traceability matrix.

## Project files

- [Test plan](docs/TEST_PLAN.md) · [Full execution report](docs/EXECUTION_REPORT.md) · [Bug reports](docs/BUG_REPORTS.md) · [Traceability](docs/TRACEABILITY.md)
- [QA workbook](SkyBook_QA_Project.xlsx) · [Test cases CSV](test-cases/SkyBook_Test_Cases.csv) · [Bugs CSV](bugs/SkyBook_Bug_Reports.csv) · [Traceability CSV](traceability/SkyBook_Traceability_Matrix.csv)
- [Screenshot evidence gallery](screenshots/README.md) — Jira, Zephyr, application, and workbook images.

## Test evidence

Zephyr shows the test library organized by Epic. The application screenshot captures BUG-14 with the Continue button enabled before all passengers have seats.

![Zephyr test case library](screenshots/zephyr-test-library.png)

![BUG-14: Continue enabled with one of two passengers seated](screenshots/BUG-14-skybook-enabled-continue-button.png)
