# 🐞 Vikunja – Manual Testing & Bug Hunting Project

A manual QA project where I tested the open-source task management app **[Vikunja](https://vikunja.io)** through its public demo, documented the results in a structured test sheet, and logged the bugs I found with steps, evidence and severity.

> **Author:** Anusha Yadav · **Role:** QA Manual Testing

---

## 📌 Project Overview

| Item | Details |
|---|---|
| **Application under test** | Vikunja (open-source to-do / project management app) |
| **Test site** | [try.vikunja.io](https://try.vikunja.io) |
| **Testing type** | Manual, functional & exploratory |
| **Browser** | Google Chrome |
| **OS** | Windows |
| **Test cases executed** | 10 |
| **Passed / Failed** | 8 / 2 |
| **Bugs logged** | 2 |

---

## 📂 Repository Contents

```
.
├── Vikunja_Bug_Hunting_Project.xlsx   # Test cases, bug reports and summary
└── README.md
```

The Excel workbook has three sheets:

1. **Tests** – 10 test cases with steps, expected result, actual result and Pass/Fail status.
2. **Bug Report** – detailed report for each failed test (one column per bug).
3. **Summary** – auto-calculated totals (executed, passed, failed, blocked, not run).

---

## 🧪 Modules & Areas Covered

- **Login** – wrong password handling
- **Projects** – empty title, very long title (250 chars), special characters / HTML / emoji
- **Tasks** – empty title, long title (300 chars), mark as Done + refresh, past due date, double-click on Add
- **Search** – special characters (`% ' " & <`)

---

## ✅ Test Results

| Test ID | Module | Scenario | Result |
|---|---|---|---|
| TC-01 | Login | Correct username + wrong password | ✅ Pass |
| TC-02 | Projects | Create project with empty title | ❌ **Fail** |
| TC-03 | Projects | 250-character project title | ✅ Pass |
| TC-04 | Projects | Title with `<b>bold</b> & 'quotes' 😀` | ✅ Pass |
| TC-05 | Tasks | Task with empty title | ✅ Pass |
| TC-06 | Tasks | 300-character task title | ✅ Pass |
| TC-07 | Tasks | Mark task Done, then refresh (F5) | ❌ **Fail** |
| TC-08 | Tasks | Due date set in the past | ✅ Pass |
| TC-09 | Tasks | Double-click the Add button quickly | ✅ Pass |
| TC-10 | Search | Special characters in search | ✅ Pass |

---

## 🐛 Bugs Found

### BUG-01 – Project can be created with an empty title
- **Failed test:** TC-02
- **Severity / Priority:** Medium / Medium
- **Steps to reproduce:** Create a new project with an empty title.
- **Expected:** Creation is blocked with a message; no empty project is created.
- **Actual:** A project with an empty title was created. The app did not block it.
- **Evidence:** [Screenshot / video](https://drive.google.com/file/d/1y9lAKuGPL3x-HHO7OcCAFVJBGeSLOBV1/view?usp=sharing)
- **Status:** Logged only

### BUG-02 – Task marked as Done disappears after page refresh
- **Failed test:** TC-07
- **Severity / Priority:** High / High
- **Steps to reproduce:** Mark a task as Done, then refresh the page (F5).
- **Expected:** The task is still shown as Done after refresh.
- **Actual:** After refreshing, the task that was marked Done disappeared from the list instead of staying Done.
- **Evidence:** [Screenshot / video](https://drive.google.com/file/d/1BKVAII21vBvsaUGm-V0TeEr9eqQR9DDW/view?usp=sharing)
- **Status:** Logged only

---

## 📏 Severity Guide Used

| Severity | Meaning |
|---|---|
| **Critical** | App unusable / data lost |
| **High** | A main feature is broken |
| **Medium** | Wrong behaviour, but a workaround exists |
| **Low** | Cosmetic / spelling issues |

---

## 🛠️ Skills Demonstrated

- Writing clear manual test cases (steps, expected vs. actual result)
- Boundary and negative testing (empty input, very long input, special characters)
- Exploratory testing and quick edge-case checks (double-click, refresh persistence)
- Writing reproducible bug reports with severity, priority and evidence
- Summarising test execution results

---

## 🚀 How to Use This Project

1. Open `Vikunja_Bug_Hunting_Project.xlsx` in Excel or Google Sheets.
2. Go through the **Tests** sheet to see every test case and its result.
3. Open the **Bug Report** sheet for full details and evidence links of each bug.
4. Check the **Summary** sheet for overall numbers.

To re-run the tests, open [try.vikunja.io](https://try.vikunja.io) in Chrome and follow the steps listed in the sheet.

---

## 🔮 Future Improvements

- Report the bugs on the official Vikunja GitHub repository
- Add more test cases (registration, labels, filters, sharing, mobile view)
- Test on more browsers (Firefox, Edge, Safari) and operating systems
- Add API testing and basic automation

---

## 📬 Contact

**Anusha Yadav** – QA Manual Testing
- GitHub: [@your-username](https://github.com/your-username)
- LinkedIn: [your-profile](https://www.linkedin.com/in/your-profile)
- Email: your-email@example.com

---

*This is a learning project done on a public demo instance. Vikunja is an open-source project by its respective maintainers; this repository is not affiliated with them.*
