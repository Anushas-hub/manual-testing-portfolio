# E-Commerce Test Documentation — Sauce Demo

Manual functional QA case study on [Sauce Demo](https://www.saucedemo.com) (the official Sauce Labs demo e-commerce application, built for QA practice).

## What's in this folder

| File | Description |
|---|---|
| `Test-Plan.pdf` | Objective, scope, approach, environment, entry/exit criteria, coverage summary |
| `Test-Cases-and-Bug-Reports.xlsx` | 28 test cases across 4 modules + 6 bug reports + auto-calculating summary dashboard |
| `screenshots/` | Execution & defect evidence |

## Scope

- **Login** — 8 test cases (positive, negative, empty-field, locked-account)
- **Product Listing / Sort** — 5 test cases (display, default order, all 4 sort options)
- **Cart** — 6 test cases (add, remove, persistence, empty-cart checkout)
- **Checkout** — 9 test cases (field validation, boundary input, order completion)

## Defects found

4 confirmed defects were logged using the application's `problem_user` test account, including one **Critical** severity bug that blocks the checkout flow entirely (Last Name field cannot be typed into). And 2 confirmed bugs from 'standard__user' Full repro steps, severity and priority are in the workbook's **Bug Reports** tab.

## Test design approach

Equivalence Partitioning and Boundary Value Analysis were used to design a mix of positive, negative and boundary test cases for every module, rather than covering the happy path alone.

## Tools used

Manual black-box testing · Google Sheets / Excel for documentation
---
*Part of my [manual testing portfolio](../).*

