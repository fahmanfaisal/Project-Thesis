<img src="docs/images/cover-aiub-logo.jpeg" width="80" alt="AIUB logo" align="left">

# Sohoj Banking — Online Banking System

**Software Project-2** · Department of Computer Science, Faculty of Science and Technology
American International University – Bangladesh (AIUB) · 2019

<br clear="all">


![Sohoj Banking home page](docs/images/fig09-home-page.png)

---

## Table of Contents

1. [Overview](#overview)
2. [Highlights](#highlights)
3. [User Roles and Features](#user-roles-and-features)
4. [How It Works](#how-it-works)
5. [Requirements](#requirements)
6. [System Design](#system-design)
7. [Screenshots](#screenshots)
8. [Comparison with Existing Systems](#comparison-with-existing-systems)
9. [Development Process](#development-process)
10. [Project Economics](#project-economics)
11. [Scope, Environment and Challenges](#scope-environment-and-challenges)
12. [Outcomes, Limitations and Future Scope](#outcomes-limitations-and-future-scope)
13. [Full Report](#full-report)
14. [Team and Supervisors](#team-and-supervisors)
15. [References](#references)

---

## Overview

Online banking, also known as internet banking, is an electronic payment system that enables
customers of a bank or other financial institution to conduct a range of financial transactions
through the institution's website. Banking online allows you to transfer money, pay bills, check
your balance or set up a regular payment — 24/7, from any place with internet access, on a
computer, tablet or mobile phone.

**Sohoj Banking** is a dynamic, web-based online banking system built to make a customer's
transaction experience a little easier: register, get approved by bank staff, then deposit,
withdraw, transfer funds, request a cheque book or ATM card, and follow every account activity
online — all from one user-friendly portal.

### Motivation

- Going to the bank for any transaction is time consuming.
- Internet banking features are easy to use, private, secured and accessible.
- Society is becoming cashless, and people are very interested in using online banking systems.

### Objectives

- Perform transactions online and consume less time.
- A user-friendly system, up to date with the latest services of the bank.
- Make the banking transaction system simple, easy and reliable.

### Hypothesis

1. People are not happy with the existing banking system.
2. Advancement of technology demands a cashless society.

---

## Highlights

| Item | Detail |
|---|---|
| User roles | Admin, Staff, Customer |
| Core modules | Home page (index) · login panel (customer/admin/staff) + sign-up · Admin panel · Customer panel · Staff panel |
| Notifications | Email notification after each successful transaction |
| Methodology | Agile, using the XP (Extreme Programming) process model |
| Report figures | 31 (8 UML diagrams + 23 UI screenshots) |
| Estimated development cost | BDT 163,961 (grand total BDT 243,961 including launch and 1-year maintenance) |
| ROI plan | BDT 255,000 over 5 years — investment returns in 5 years |
| Status | All planned features implemented and working; mobile app planned for the future |

---

## User Roles and Features

There are three types of user: **Admin**, **Staff** and **Customer**.
Existing customers, admins and staff log in with a unique mail ID and password;
a new customer must register first.

### Customer

| Area | Features |
|---|---|
| Profile | Show profile · update profile · change password · logout |
| Money | Withdraw money · deposit money · transfer money to another account in the same bank or another bank · start a fixed deposit |
| Requests | Apply for credit/debit card · request a cheque book · request an ATM card · add / view / delete beneficiary |
| Records | Account statement · mini account statement |

### Staff

| Area | Features |
|---|---|
| Approvals | Approve new registration requests · approve credit/debit card · approve ATM requests · approve cheque book requests · approve beneficiaries |
| Information | Send notifications to customers · see the list of customers who did any transaction through the system |
| Account | Show profile · change password · logout |

### Admin

| Area | Features |
|---|---|
| Customer management | Add a new customer (after approval by staff) · search / show the list of all customers · update or delete a customer |
| Staff management | Add staff · edit staff · delete staff |
| Control | Block any account for a particular time period · access customer profiles · post article |
| Account | Show profile · change password · logout |

---

## How It Works

1. **Registration** — a new customer signs up with personal details (name, password, mobile
   number, address, branch, account type, nominee, etc.).
2. **Staff approval** — staff verifies the request from the request queue and approves the
   new customer.
3. **Login** — the customer logs in with a unique mail ID and password.
4. **Banking** — the customer deposits, withdraws, transfers funds, adds beneficiaries and
   requests a cheque book or ATM card; statements and mini statements are available online.
5. **Approvals** — staff approves customer, ATM, cheque book and beneficiary requests;
   admins add/edit/delete customers and staff and can block profiles.
6. **Notification** — an email notification is sent after each successful transaction.

---

## Requirements

### Functional (Customer Requirements)

- Show profile, update profile, change password, logout.
- Withdraw money, deposit money.
- Transfer money to another bank or within the same bank.
- Start a fixed deposit.
- Apply for a credit/debit card.

### Architectural Requirements

| Side | Specification |
|---|---|
| Server | OS: Linux / Windows Server · CPU: minimum Intel Xeon or higher · RAM: 4 GB or more · Hard drive: 1024 GB or more |
| Client (PC) | Any OS with web browsing · CPU: minimum Intel Pentium or higher |
| Client (Android) | Any OS with web browsing · CPU: Mali-400MP4 or higher · RAM: 512 MB or more |

### Performance Requirements

The system should be less time consuming in its operations; the majority of the work should be
done internally during the program's run-time and then set for network access.

---

## System Design

### Use Case Diagram

Shows the relationship between admin, customer and staff: how an admin approves a customer,
how staff verify a customer and send transaction notifications, and how a customer deposits,
withdraws and transfers money.

![Use Case Diagram for Online Banking](docs/images/fig01-use-case-diagram.jpeg)

### Activity Diagrams

**Admin** — approves a customer, can delete a customer, view the customer list, and update,
delete and block a customer.

![Activity Diagram for Admin](docs/images/fig02-activity-admin.jpeg)

**Customer** — logs in and transacts money, can apply for a debit/credit card, change password,
update the profile, and deposit, withdraw or transfer money.

![Activity Diagram for Customer](docs/images/fig03-activity-customer.jpeg)

**Staff** — approves new registration and sends transaction notifications to the customer.

![Activity Diagram for Staff](docs/images/fig04-activity-staff.jpeg)

### Statechart Diagrams

![Statechart Diagram for Admin](docs/images/fig05-statechart-admin.png)

![Statechart Diagram for Customer](docs/images/fig06-statechart-customer.png)

![Statechart Diagram for Staff](docs/images/fig07-statechart-staff.png)

### Entity Relationship Diagram

![ER Diagram for Online Banking System](docs/images/fig08-er-diagram.jpeg)

---

## Screenshots

### Home Page

The home page of Sohoj Banking with the secure login panel, sign-up link, features list and
safe-banking information.

![Home page](docs/images/fig09-home-page.png)

### Admin Panel

After login, an admin can change their password and add, delete or edit a customer or staff member.

![Admin options](docs/images/fig10-admin-options.png)

A new customer is added by filling in the name, password, mobile number, address and other
details, then confirming.

![Admin adding a customer](docs/images/fig11-admin-add-customer.png)

An admin can also add staff members to the system.

![Admin adding staff](docs/images/fig12-admin-add-staff.png)

<details>
<summary>Show the remaining admin screenshots (edit/delete customer, edit/delete staff)</summary>

![Admin editing a customer](docs/images/fig13-admin-edit-customer.png)

![Admin deleting a customer](docs/images/fig14-admin-delete-customer.png)

![Admin editing staff](docs/images/fig15-admin-edit-staff.png)

![Admin deleting staff](docs/images/fig16-admin-delete-staff.png)

</details>

### Customer Panel

After login, a customer sees these options for transactions: account balance, money transfer,
bill payment and more.

![Customer options](docs/images/fig17-customer-options.png)

From the account statement a customer can review full account activity online.

![Customer account statement](docs/images/fig21-customer-account-statement.png)

A customer transfers funds to another account after adding a beneficiary.

![Customer fund transfer](docs/images/fig24-customer-fund-transfer.png)

A customer can request a new cheque book or ATM card online instead of visiting the bank.

![Customer cheque book and ATM request](docs/images/fig20-customer-cheque-atm-request.png)

<details>
<summary>Show the remaining customer screenshots (personal details, password, mini statement, beneficiaries)</summary>

![Customer personal details](docs/images/fig18-customer-personal-details.png)

![Customer password change](docs/images/fig19-customer-change-password.png)

![Customer mini account statement](docs/images/fig22-customer-mini-statement.png)

![Customer add beneficiary](docs/images/fig23-customer-add-beneficiary.png)

![Customer view or delete beneficiary](docs/images/fig25-customer-view-delete-beneficiary.png)

</details>

### Staff Panel

The staff home page shows customer approval requests, ATM approval requests and cheque book
requests.

![Staff options](docs/images/fig26-staff-options.png)

A staff member approves a customer from the request queue.

![Staff approving a customer](docs/images/fig28-staff-approve-customer.png)

Cheque book requests are approved from the same panel.

![Staff approving a cheque book request](docs/images/fig31-staff-approve-chequebook.png)

<details>
<summary>Show the remaining staff screenshots (password change, ATM and beneficiary approval)</summary>

![Staff password change](docs/images/fig27-staff-change-password.png)

![Staff approving an ATM request](docs/images/fig29-staff-approve-atm.png)

![Staff approving a beneficiary](docs/images/fig30-staff-approve-beneficiary.png)

</details>

---

## Comparison with Existing Systems

Nine banking and banking-related systems were studied (Traderoot Technologies, Oracle
Flexcube, Altamira, IBS, ICS Bank, i-Mall, Kastle, Olympic Bank System, Omni Enterprise).
The chart below compares 12 features of two representative systems with Sohoj Banking.

| # | Feature | Oracle Flexcube | Olympic Bank | Sohoj Banking |
|---|---|:---:|:---:|:---:|
| 1 | Payment option through different sorts of cards (credit/master card, etc.) | ✓ | — | — |
| 2 | Payment / transaction cancellation | ✓ | — | — |
| 3 | Customer details | ✓ | — | ✓ |
| 4 | Monitoring operators | ✓ | ✓ | ✓ |
| 5 | Do transaction online | ✓ | ✓ | — |
| 6 | Send money from one account to another account | ✓ | — | ✓ |
| 7 | Pay any bills through their banking account | — | — | — |
| 8 | Refund request | — | — | — |
| 9 | Customer, admin and staff each have a unique mail ID and password | ✓ | — | ✓ |
| 10 | Record of all transactions | — | — | ✓ |
| 11 | Admin and staff can send notifications for updates or notices | — | ✓ | ✓ |
| 12 | Customer can change password and modify their profile | — | — | ✓ |
| | **Total** | **7** | **3** | **7** |

### Feature gaps we identified and filled

- **Customer's own panel** — see all account-related details and transaction history, which
  the existing systems above do not offer.
- **Account statement online** — not available in the existing systems.
- **Cheque book request online** — in existing systems a customer must go to the bank and
  apply in person.

No external human resources were required for the study; information about existing banking
systems was collected from the internet.

---

## Development Process

### Methodology

We used **agile methodology** to develop the system. Agile is an iteration-based software
development method in which errors can be fixed at any time and work can start and stop
wherever needed. The **XP (Extreme Programming) process model** was used within the project.

### Developed System Specification

| Module | Specification |
|---|---|
| Home page (index) | Login panel (customer, admin, staff), sign-up |
| Admin | Show profile, add customer/staff, delete customer/staff, change password, profile edit, logout |
| Customer | Show profile, account statement, mini statement, add beneficiary, apply for cheque/ATM, transfer funds, edit profile, change password, logout |
| Staff | Show profile, approve ATM/cheque, approve beneficiary, approve new customer request, change password, logout |

---

## Project Economics

Working hours: **8 hours per day**, **22 days per month**. Domain cost is Tk. 1,000/year;
the hosting package offers unlimited web space, bandwidth, databases, mailboxes and FTP
accounts with an SSL certificate (Tk. 10,000/year).

### Man-hour Cost

| Position | Monthly salary | Table / computer / other cost | Cost per hour |
|---|---:|---:|---:|
| Project Manager (PM) | 70,000 tk | 3,000 + 5,000 + 2,500 | **457.39 tk** |
| Business Analyst (BA) | 50,000 tk | 2,000 + 4,000 + 2,500 | **332.39 tk** |
| Developer (D) | 50,000 tk | 2,000 + 5,000 + 2,500 | **338.07 tk** |
| Quality Tester (QT) | 50,000 tk | 2,000 + 5,000 + 2,500 | **338.07 tk** |

### Cost Benefit Analysis

| Phase | Position | Man-hours | Rate/hr | Total |
|---|---|---:|---:|---:|
| Requirement specification and design | PM | 16 | 457.39 | 7,318.24 |
| | BA | 24 | 332.39 | 7,977.36 |
| | **Phase total** | | | **15,295.60** |
| Coding and testing | PM | 30 | 457.39 | 13,721.70 |
| | BA | 50 | 332.39 | 16,619.50 |
| | Developer | 200 | 338.07 | 67,614.00 |
| | QT | 150 | 338.07 | 50,710.50 |
| | **Phase total** | | | **148,665.70** |

**Estimated grand total cost**

| Description | Cost assumption |
|---|---:|
| Development | 163,961 BDT |
| Site launch (hosting) | 30,000 BDT |
| Maintenance (1 year) | 50,000 BDT |
| **Grand total** | **243,961 BDT** |

### Return of Investment

| Year | Medium | Amount |
|---|---|---:|
| 1st | Service charge + third party ad | 10,000.00 Tk |
| 2nd | Service charge + third party ad + merchant commission | 25,000.00 Tk |
| 3rd | Service charge + third party ad + merchant commission | 45,000.00 Tk |
| 4th | Service charge + third party ad + merchant commission | 75,000.00 Tk |
| 5th | Service charge + third party ad + merchant commission | 1,00,000.00 Tk |
| | **Total after 5 years** | **2,55,000.00 Tk** |

It will take **5 years** to return the investment.

---

## Scope, Environment and Challenges

**Scope** — The project is designed to run on desktop as well as mobile; users save time by
doing online banking from home.

**Environment** — The website must work on Android and iOS and be accessible from any web
browser: Google Chrome, Mozilla Firefox and Internet Explorer.

**Challenges**

1. The most impactful barrier of online banking is security.
2. The next challenge is the customer's privacy.
3. Broadband speed is another barrier.
4. Sophisticated IT infrastructure is required.
5. Lack of IT knowledge among users.
6. Requires a mobile phone or computer to use.
7. Customer satisfaction.

---

## Outcomes, Limitations and Future Scope

**Discussion on outcome** — Almost all the features we intended to implement are working
perfectly. An initial plan for a mobile application could not be completed; we plan to develop
an Android and iOS application in the near future.

**Performance** — In testing, the system fulfilled its performance requirements.

**Findings (limitations)**

- The security of the system is still very vulnerable.
- No OTP system was added for each transaction.
- Email notification is used for successful transactions; SMS notification would be more useful.

**Future aspects**

- Make the system more user friendly and collect appropriate requirements.
- Make services faster, with faster processing and updates.
- Allow transactions from any place.
- Make the system more reliable and secure than the current one.
- Include more functions, widgets and a more attractive, interactive interface.

**Conclusion** — "Sohoj Banking" is an online-based banking system that provides banking
services online. It is user friendly, secure and accurate, and much more efficient than a
manual banking transaction system.

---

## Full Report

The complete software project report — including declaration, approval, acknowledgement,
requirement analysis, cost benefit analysis, all diagrams, all screenshots and references —
is available in this repository:

**[Sohoj Banking(SP2).docx](Sohoj%20Banking%28SP2%29.docx)** (Microsoft Word, ~9 MB)

All 31 figures were extracted from the report into [`docs/images/`](docs/images/) for reuse.

---

## Team and Supervisors

**Submitted by**

| ID | Name |
|---|---|
| 15-30923-3 | Sandhi, Shihab Rizwan |
| 15-30854-3 | Parves, Rubel |
| 16-31557-1 | Saha, Saikat Chandra |
| 16-31429-1 | Chowdhury, Md Faisal |

**Board of examiners and supervisors**

| Role | Name |
|---|---|
| Supervisor (Assistant Professor) | Md. Ezazul Islam |
| External (Assistant Professor) | Sabbir Ahmed |
| Head, UG Program | Dr. M. M. Mahbubul Syeed |
| Dean, Faculty of Science and Information Technology | Prof. Dr. Tafazzal Hossain |
| Vice Chancellor | Dr. Carmen Z. Lamagna |

Submitted on 27 August 2019 and accepted on 28 September 2019 in partial fulfillment of the
requirements for the degree of Bachelor of Science in Computer Science and Software
Engineering, American International University – Bangladesh.

---

## References

1. https://www.globalbrandsmagazine.com/list-of-banking-software/
2. http://www.icsfs.com/en
3. http://www.icsfs.com/en/products/core-banking
4. https://legacy.imal.org/en/page/about-imal
5. http://www.imalpal.com/en/
6. http://security.kastle.com/
7. http://www.omni-enterprise.com/
8. http://www.infrasofttech.com/banking-products
9. http://www.oracle.com/us/industries/financial-services/046059.pdf
10. http://bankingsoftwareinfo.blogspot.com/
11. IEEE Software Engineering Standards Committee, "IEEE Std 830-1998, IEEE Recommended
    Practice for Software Requirements Specifications", October 20, 1998
12. https://www.roberthalf.com/blog/salaries-and-skills/6-basic-sdlc-methodologies-which-one-is-best
