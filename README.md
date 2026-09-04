# 🛒 Rokomari.com Manual QA Testing Project

![Testing Type](https://img.shields.io/badge/Testing-Manual-blue)
![Platform](https://img.shields.io/badge/Platform-E--Commerce-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📖 About The Project
This repository contains comprehensive manual testing documentation for **Rokomari.com**, Bangladesh's largest e-commerce platform for books and electronics. The testing scope primarily focuses on the **E-Book Module**, **Search & Filter Algorithms**, **Sorting Logic**, and the **Cart & Checkout/Payment Gateway** processes. 

The goal of this project was to ensure a flawless user journey from product discovery to secure checkout, utilizing industry-standard QA methodologies.

---

## 🎯 Testing Scope & Features Covered
- **Filtering System:** Ratings, New Releases, Price Range (BVA), Language, Publisher, Author.
- **Sorting Mechanisms:** Price (High/Low), Discount Calculations (High/Low).
- **Core Book Features:** Live Chat Support Widget, "একটু পড়ে দেখুন" (Book Preview/Look Inside) access control.
- **Cart & Checkout Logic:** Mandatory field validation for physical (Hard Copy) deliveries vs. E-books.
- **Payment Gateways (Redirection):** bKash, Nagad, and MasterCard/Bank integrations.

---

## 🧪 Types of Testing Performed
- **Functional Testing:** Validating core features like sorting, filtering, and payment redirection.
- **UI & Usability Testing:** Analyzing page reload behavior and user experience during product filtering.
- **Boundary Value Analysis (BVA):** Testing minimum and maximum monetary thresholds on price filters.
- **Positive & Negative Testing:** Ensuring features like the Book Preview sticker grant or restrict access properly based on user authorization.

---

## 📂 QA Deliverables & Documentation

### 1. Mind Map 🧠
A complete visual breakdown of the testing structure. The mind map categorizes the E-book module, Cart functionality, and Checkout processes, marking out passing and failing modules for a quick high-level overview. *(File included in the repo).*

### 2. Test Scenarios 📋
Designed **13 High-level Test Scenarios** covering 19 distinct Test Cases. Documented in standard CSV/Excel format.
| Scenario ID | Tested Module | Priority |
| :--- | :--- | :--- |
| **TS_001** | Filter UI & Page Reload | P2 |
| **TS_002 - TS_007** | Filters (Ratings, Released, Price, Lang, Pub, Author) | P1 - P3 |
| **TS_008 - TS_009** | Sorting Calculations & Routing (Price, Discount) | P1 - P2 |
| **TS_010** | Live Chat Box User Interaction | P4 |
| **TS_011** | Book Preview Feature (Positive/Negative) | P1 |
| **TS_012** | Hard Copy Order Delivery Logic | P1 |
| **TS_013** | Payment Gateways (bKash, Nagad, Card) | P0 |

### 3. Test Cases 📝
Executed **19 Detailed Test Cases** featuring:
- Precise Reproducing Steps & Test Data.
- Expected vs. Actual Results.
- Pass/Fail Status & Dev Comments/Remarks.

### 4. Bug Reports 🐞
Identified and documented critical bugs. **Bugs were originally tracked and logged in Jira** (Internal tracking). For this repository, detailed Bug Reports following professional QA templates have been generated in `.docx` format, complete with reproducing steps, priority/severity scaling, and screenshots.

---

## 🚨 Key Defects & Bugs Discovered
During test execution, several critical business logic and UX defects were found:
1. **Critical Routing Defect (High Priority):** Sorting by "Discount - Low to High" breaks URL parameters. Clicking the top 3 sorted books redirects the user to the homepage instead of the product page, breaking the conversion funnel.
2. **Backend Indexing Failure (High Priority):** The 1-Star Rating filter incorrectly queries and displays books with 4.5-star ratings (e.g., *'না বলতে শিখুন'*), violating core sorting algorithms.
3. **Severe UX Flaw (Medium Priority):** Selecting multiple criteria in the sidebar filter triggers hard, full-page reloads for *every single click*, disrupting the user journey. Advocated for AJAX-based asynchronous loading.

---

## 🛠️ Tools & Technologies Used
* **Test Case Management:** Microsoft Excel / Google Sheets
* **Bug Tracking:** Jira, Microsoft Word (Docx Reports)
* **Visual Mapping:** Mind Mapping Software
* **Browsers Tested:** Google Chrome, Safari, Mozilla Firefox, Microsoft Edge

---

## 📁 Repository Structure
```text

├── Rokomari_Bug_01_UI_Reload.docx
├── Rokomari_Bug_04_Routing_Error.docx
├── Test_Cases/
│   └── Rokomari_Testing.xlsx
├── Test_Scenarios/
│   └── Rokomari_Testing.xlsx
├── Mind_Map/
│   └── Rokomari_Testing.xlsx
└── README.md


👤 Author

Muhammed Jabed Iqbal Sami
QA Analyst / Software Tester
