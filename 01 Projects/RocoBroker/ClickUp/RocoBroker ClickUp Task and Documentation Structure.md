---
aliases:
  - ClickUp structure guide
tags:
  - roco
  - clickup
  - task-management
  - documentation
type: guide
status: proposed
area:
  - operations
created: 2026-09-16
updated: 2026-09-18
source: "https://chatgpt.com/share/6aaa44dd-86f0-83ed-95a5-21ed06196448"
---

# RocoBroker ClickUp Task and Documentation Structure

> [!summary]
> Fewer Lists, clearer Tasks, simple Custom Fields, and linked permanent documentation. ClickUp manages action; documentation preserves reusable knowledge; official files retain one canonical storage location.

## Provenance and decision status

This guide consolidates the conversation text pasted by the user on 2026-09-16. [Shared conversation](https://chatgpt.com/share/6aaa44dd-86f0-83ed-95a5-21ed06196448). The pasted text, not the inaccessible shared page, was the content actually read.

These are recommendations, not evidence that the workspace has been changed or the team has approved them. The referenced screenshot was not supplied, so screenshot-specific observations remain source recommendations rather than independently verified findings.

The source assumes a 40-List constraint for this setup. Verify the actual workspace/plan limit before implementation; this note does not assert a universal ClickUp limit.

## Hierarchy and placement rules

| Item | Purpose | Examples |
| --- | --- | --- |
| Space | Major company area | Operations, Finance, Brokerage |
| Folder | Group of related work areas | Trading Systems, HR, Marketing |
| List | Permanent, continuous area of work | MT5, CRM, Accounting |
| Task | Actual work with an outcome | Update MT5 symbols, review provider agreement |
| Subtask | Smaller step within that work | Review fees, test withdrawals |
| Custom Field or Tag | Type/category, not another work area | Plugin, Report, Bug, Receivable |
| Documentation | Information useful after completion | Procedures, configuration, recovery instructions |
| Main cloud storage | Canonical official file | Signed contract, license, financial report |

Do not make separate Lists for every topic. MT5 Plugins, MT5 Reports, MT5 Downloads, CRM Bugs, and CRM Integrations normally belong inside the MT5 or CRM List as Tasks or field values.

Create a new List when a work area is permanent, substantial, and meaningfully needs separate visibility, workflow, permissions, statuses, or fields. A different topic alone is not sufficient.

## List budget: two alternatives

| Space | Original compact proposal | With expanded Brokerage |
| --- | ---: | ---: |
| 01_Operations | 12 | 12 |
| 02_Finance | 7 | 7 |
| 03_Websites & Marketing | 8 | 8 |
| 04_Brokerage | 7 | 10 |
| 05_Sharing | 2 | 2 |
| Total | 36 | 39 |
| Spare capacity if the cap is 40 | 4 | 1 |

The source's initial target is roughly 32-35 Lists; its full compact tree actually uses 36. Replacing its seven Brokerage Lists with the later ten-List version produces 39. The later draft's broad department ranges likewise do not guarantee a total below 36.

Prefer the compact proposal if growth headroom is important. Adopt the expanded Brokerage version only after reviewing the total budget or consolidating elsewhere. Neither alternative is recorded as the adopted design.

## Compact company structure: 36 Lists

Indented department headings are Folders; their leaves are Lists. Finance, Brokerage, and Sharing can have Lists directly under their Spaces.

```text
RocoBroker
├── 01_Operations [12]
│   ├── Company
│   │   ├── General
│   │   ├── Policies & SOPs
│   │   └── Templates & Branding
│   ├── IT
│   │   ├── Infrastructure
│   │   ├── Software
│   │   └── Documentation & Backups
│   ├── HR
│   │   ├── Employees
│   │   ├── Recruitment & Training
│   │   └── HR Admin
│   └── Legal & Compliance
│       ├── Compliance
│       ├── Legal
│       └── Licenses & Audits
├── 02_Finance [7]
│   ├── Accounting
│   ├── Banking
│   ├── Budget & Payroll
│   ├── Taxes
│   ├── Invoices
│   ├── Providers
│   └── Reports
├── 03_Websites & Marketing [8]
│   ├── Websites
│   │   ├── RocoBroker.com
│   │   ├── New Website
│   │   └── SEO & Analytics
│   ├── Marketing
│   │   ├── Campaigns
│   │   ├── Social Media
│   │   ├── Email & Content
│   │   └── Design & Brand
│   └── Media
│       └── Media Library
├── 04_Brokerage [7]
│   ├── MT5
│   ├── CRM
│   ├── IB & PAMM
│   ├── Risk
│   ├── Liquidity & Payments
│   ├── Clients & Products
│   └── Brokerage Reports
└── 05_Sharing [2]
    ├── Shared Resources
    └── Training & Forms
```

### Details that do not need their own Lists

- Infrastructure: Servers, Network, DNS, SSL, Monitoring.
- Software: Chatwoot, CRM, MT5, Internal Tools, Licenses.
- Compliance: AML, KYC, Regulators, Policies, Reviews.
- Invoices: Receivable and Payable.
- Finance Providers: Coinigo, Coinsbuy, Liquidity, PSPs.
- Reports: Monthly, Quarterly, Annual.
- Liquidity & Payments: liquidity/payment providers, new providers, technical issues, commercial issues.
- RocoBroker.com Tasks: fix mobile menu, update About page, add banner, fix redirect, update plugin. Suggested Type values: Development, Content, Design, SEO, Bug, Update.

## Expanded Brokerage alternative: 10 Lists

```text
04_Brokerage
├── Trading Systems
│   ├── MT5
│   ├── CRM
│   └── R&D
├── Business
│   ├── BD Operations
│   ├── IB & PAMM
│   └── Clients & Products
├── Risk & Compliance
│   ├── Compliance
│   ├── Risk
│   └── Liquidity & Payments
└── Reports
    └── Brokerage Reports
```

Source migration recommendations:

- Keep HR under Operations, not Brokerage.
- Use recurring birthday Tasks in HR Admin, not a Birthday List.
- If Establishment means registration, licensing, office setup, or company formation, place it under Operations > Company or the relevant Legal area.
- Rename generic MT5/CRM Lists to MT5/CRM; avoid single-List Folders unless they serve a useful grouping purpose.
- Use either Business Development or BD Operations consistently.
- Keep R&D in Brokerage only when it concerns trading systems, brokerage products, or related development.

> [!warning] Ownership ambiguity to resolve
> The expanded version includes Brokerage Compliance while Operations already has Compliance. Finance Providers also overlaps with Brokerage Liquidity & Payments, and IT Software overlaps with MT5/CRM. Define ownership and link related work rather than copying the same Tasks or official documents into both locations. This warning is an operator synthesis of the proposed trees.

## Task and Custom Field examples

| List | Example Tasks | Suggested Type values |
| --- | --- | --- |
| MT5 | Update symbols; add instrument; check swap rates; fix server issue; update plugin; review configuration; prepare monthly report; update documentation; upload installer | Configuration, Plugin, Server, Symbols, Pricing, Report, Documentation, Download, Issue |
| CRM | Fix KYC issue; add email template; update registration form; connect payment provider; change client status; fix API issue | KYC, Payments, Email, API, Registration, Bug, Improvement |
| BD Operations | Contact partner; prepare partnership offer; follow up with provider; review commercial terms; prepare meeting; onboard partner | Partner, Provider, Sales, Meeting, Follow-up, Onboarding |

Keep fields simple. Use Type for work categories and the normal priority mechanism for Urgent, High, Normal, Low. Add Department only when cross-department movement warrants it. Request Source may distinguish Management, Client, Partner, Provider, Internal, and Compliance.

### Naming and task quality

- Begin Task names with an action: Update, Review, Fix, Prepare, Contact, Check.
- Make the outcome understandable without opening the Task. Avoid vague names such as MT5, Provider, Important issue, or General task.
- Every active Task should have an owner; important Tasks should have a due date.
- Use simple, consistent English for Folders and Lists rather than unnecessarily long corporate wording.
- Use Subtasks for steps, not separate Lists. Example: Add new payment provider → review provider, check fees, review API, sign agreement, configure CRM, test deposits, test withdrawals, go live.

### Sprint Points — راهنمای برآورد تلاش تیم

Sprint Points برآورد **نسبی تلاش** برای انجام یک تسک است؛ ترکیبی از حجم کار، پیچیدگی، عدم‌قطعیت و هماهنگی لازم. امتیاز، ساعت یا معیار ارزش و عملکرد افراد نیست؛ «۱ امتیاز = ۱ ساعت» تعریف نکنید. برای برنامه‌ریزی ظرفیت، امتیاز کارهای تکمیل‌شده در چند دوره مشابه را مبنا قرار دهید، نه مقایسه مستقیم تیم‌های مختلف.

#### مقیاس پیشنهادی و مثال‌های کارگزاری

از مقیاس فیبوناچی **1 / 2 / 3 / 5 / 8 / 13** استفاده کنید. مثال‌ها نقطه شروع‌اند؛ تیم باید آن‌ها را با تجربه خودش کالیبره کند، نه اینکه نوع تسک همیشه امتیاز ثابت داشته باشد.

| امتیاز | اندازه نسبی | مثال برای RocoBroker |
| ---: | --- | --- |
| 1 | بسیار کوچک | اصلاح متن یک ایمیل آماده CRM |
| 2 | کوچک | به‌روزرسانی مشخصات یک نماد MT5 با تنظیمات معلوم |
| 3 | متوسط | تهیه گزارش معمول ماهانه نقدینگی با داده‌های آماده |
| 5 | قابل‌توجه | اصلاح جریان KYC در CRM همراه با تست |
| 8 | بزرگ یا دارای ابهام | اتصال یک PSP با API شناخته‌شده و تست واریز/برداشت |
| 13 | بسیار بزرگ یا نامطمئن | مهاجرت داده‌های مشتریان بین دو CRM؛ نیازمند خردکردن |

> [!tip] قاعده پیشنهادی تیم، نه محدودیت ClickUp
> تسک‌های **بیش از ۸ امتیاز** معمولاً باید به تسک‌ها یا Subtaskهای کوچک‌تر، با خروجی و معیار تکمیل روشن، تقسیم شوند. اگر ابهام زیاد است، ابتدا یک تسک بررسی تعریف کنید. این قاعده برای کار اجرایی است؛ مجموع Rollup یک تسک والد می‌تواند بیشتر از ۸ باشد.

#### تفاوت با سایر مشخصات تسک

| مشخصه | سؤال اصلی |
| --- | --- |
| Sprint Points | انجام کار نسبت به کارهای دیگر چقدر تلاش می‌خواهد؟ |
| Priority | کار چقدر مهم یا فوری است؟ |
| Time Estimate | تقریباً چند ساعت یا روز کاری لازم دارد؟ |
| Due Date | مهلت انجام کار چه تاریخی است؟ |
| Status | کار اکنون در چه مرحله‌ای است؟ |
| Milestone | آیا این تسک یک نقطه کلیدی پروژه را مشخص می‌کند؟ |

مثلاً اصلاح فوری نرخ Swap می‌تواند Priority = Urgent و Sprint Points = 2 داشته باشد؛ فوری‌بودن به معنی پیچیده‌بودن نیست. Time Estimate و Due Date را جداگانه تعیین کنید؛ امتیاز جایگزین زمان، موعد یا وضعیت نیست.

#### Rollup Sprint Points و Points per Assignee

- **Rollup Sprint Points:** در صورت فعال‌بودن، امتیاز والد و Subtaskها با هم نمایش داده می‌شوند؛ امتیاز Subtaskهای تو‌در‌تو به والد سطح اول می‌رود، نه به والد میانی. اگر والد فقط ظرف تجمیع است، تلاش تکراری برای آن ثبت نکنید و در گزارش ظرفیت، مجموع والد را دوباره با فرزندان جمع نزنید.
- **Points per Assignee:** با فعال‌بودن این گزینه و Multiple Assignees، می‌توان برای هر مسئول امتیاز جدا گذاشت؛ امتیاز نمایش‌داده‌شده تسک جمع آن‌هاست. مثلاً بررسی PSP: مسئول فنی 3 و مسئول عملیات 2، مجموع 5. امتیاز کل کار را برای هر نفر تکرار نکنید.

این بخش در 2026-09-17 بر اساس درخواست کاربر اضافه شد. رفتار قابلیت‌ها با [راهنمای رسمی Sprint Points در ClickUp](https://help.clickup.com/hc/en-us/articles/6303883602327-Use-Sprint-Points) بررسی شده؛ مقیاس، مثال‌ها و قاعده خردکردن، پیشنهاد تیمی هستند. هیچ تنظیمی در ClickUp تغییر نکرده است.

### Recurring work and archives

Use recurring Tasks for monthly reports, backup checks, SSL reviews, birthdays, weekly sales meetings, compliance reviews, and liquidity reports.

Keep completed Tasks completed in their existing ClickUp location; use status, filters, and search rather than proliferating Archive Lists. Use document Archive folders when inactive records must be retained, subject to the company's retention rules.

## Task information, documentation, and official storage

| Location | What belongs there |
| --- | --- |
| ClickUp Task | Temporary discussion, screenshots, checklists, approvals, working files, owner, due date |
| ClickUp Docs | Team procedures closely connected to execution: client/IB onboarding, monthly reporting, marketing and internal workflows |
| Main company cloud storage | Signed contracts, legal/financial records, licenses, policies, official templates, large assets, controlled backups |
| Obsidian second brain | Searchable knowledge, decisions, research, operating guides, and links to canonical Tasks, procedures, and files |

The Obsidian row is an operator adaptation to the user's second-brain setup, not an explicit fourth layer from the pasted three-level storage recommendation. Avoid duplicating final versions across all four locations.

When a Task finishes, extract knowledge that remains useful. For Configure new MT5 server, preserve approved setup/configuration, recovery steps, and known issues in the appropriate controlled documentation. Sensitive infrastructure details must remain in an access-controlled location; do not place credentials in general notes.

### One source of truth

1. Store the canonical official file in the designated company storage.
2. Link it from the related ClickUp Task and relevant knowledge note.
3. Keep work tracking, deadlines, responsibility, and discussion in ClickUp.
4. Update the canonical copy instead of producing conflicting Final, Final 2, and Final Approved versions across email, local disks, messaging apps, and storage services.

Example: Review Liquidity Provider Agreement contains an owner, due date, checklist, comments, and a link. The signed agreement remains in permanent document storage.

### Suggested company storage layout

```text
RocoBroker
├── 01_Operations
├── 02_Finance
├── 03_Websites & Marketing
├── 04_Brokerage
└── 05_Shared
```

Storage may have more detailed subfolders than ClickUp. Similar names aid navigation; identical hierarchies are unnecessary. Choose Sharing or Shared consistently where practical.

Example mapping:

```text
ClickUp: Brokerage > Liquidity & Payments > Add New PSP
    links to
Storage: 04_Brokerage > Payment Providers > Provider Name
         ├── Agreement
         ├── Technical
         ├── KYC
         └── Reports
```

## Permissions and maintenance

The source recommends managing access mainly at Space/Folder level where supported, rather than individually for every Task. Validate actual inheritance and sharing behavior before changing access.

Restrict HR, payroll, legal, compliance, management, and sensitive finance records appropriately. Document storage and Obsidian access must also respect those restrictions; a link does not grant authorization. Review access when employees join or leave.

Review the structure every few months. Keep Sharing small rather than turning it into a second archive. Do not create Lists without a genuine ongoing need.

## Decisions before implementation

- [ ] Confirm actual List limit and current List count.
- [ ] Choose compact 36-List or expanded 39-List alternative, or explicitly budget a revised version.
- [ ] Resolve Compliance, Providers, and IT versus Brokerage ownership overlaps.
- [ ] Select canonical company storage and document owners.
- [ ] Confirm naming, Type values, workflows, and permissions with the team.
- [ ] Trial the design with representative MT5, CRM, HR, and provider Tasks before broad migration.

No ClickUp migration or permission changes have been performed by adding this note.

## Related vault context

- [[02 Areas/RocoBroker/Work Logs/2026/September/work report]] — includes ClickUp structure, task-entry, workspace-review, and team-guide action items.
- [[02 Areas/RocoBroker/Operations/meet by sjd]] — records ClickUp task-management use and HR/BD responsibilities.
- [[90 System/Codex Operator]] — operating contract for Obsidian as the primary knowledge base.
- [[01 Projects/RocoBroker/ClickUp/ClickUp Tips and Future Ideas]] — collected tips, cross-Workspace ideas, and feedback references for future brainstorming.

- [[01 Projects/RocoBroker/ClickUp/ClickUp MCP Server Reference]] — official server documentation, authentication, rate limits, and tool availability caveats.
