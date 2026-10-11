# Accessibility Auditor-and-Fixer Tool

## 1. Project Overview

The Accessibility Auditor-and-Fixer Tool is a web-based application that helps users identify common accessibility issues on public webpages.

Users can submit a webpage URL, scan the page for selected accessibility issues, understand why each issue matters, and receive practical suggestions for fixing it. The tool will also provide relevant WCAG references when reliable and allow users to download a report of the scan results.

## 2. Problem Statement

Many websites contain accessibility barriers that make them difficult to use for people with disabilities, including screen reader users, people with low vision, and people who navigate websites using a keyboard.

Although accessibility testing tools and guidelines are available, beginners and small-business website owners may struggle to understand the results and implement appropriate fixes.

This project aims to make accessibility testing more understandable and actionable by combining automated checks, plain-language explanations, practical fix suggestions, and downloadable reports in one workflow.

## 3. Target Users

### 3.1 Primary Users: Beginner Web Developers

Beginner web developers who want to identify accessibility issues in their websites and learn how to fix them. They need clear explanations, practical code suggestions, and guidance on accessibility standards.

### 3.2 Secondary Users: Small-Business Website Owners

Small-business website owners who want to identify common accessibility barriers on their websites without needing advanced technical knowledge. They need understandable scan results and actionable recommendations.

### 3.3 User Needs

The target users need a tool that:

- Accepts a public webpage URL for scanning.
- Identifies selected common accessibility issues.
- Explains each detected issue in simple language.
- Provides practical suggestions for fixing issues.
- Includes relevant WCAG references when reliable.
- Identifies issues that require manual review.
- Generates a downloadable report of scan results.

## 4. Functional Requirements

The system shall provide the following functionalities:

### FR-01: URL Submission and Validation
The system shall allow users to enter a public webpage URL and validate it before starting a scan.

### FR-02: Webpage Scanning
The system shall scan the submitted webpage using automated accessibility testing checks to identify selected common accessibility issues.

### FR-03: Display Scan Results
The system shall display detected issues in an organized format, including issue titles and severity information when available from the testing engine.

### FR-04: Issue Explanation
The system shall explain detected issues in simple language so users can understand the problem and its potential impact on accessibility.

### FR-05: WCAG References
The system shall provide relevant Web Content Accessibility Guidelines (WCAG) references when reliable information is available for a detected issue.

### FR-06: Fix Suggestions
The system shall provide practical recommendations and code examples where appropriate to help users address detected issues.

### FR-07: Manual Review Guidance
The system shall identify checks that require human judgment and provide guidance for reviewing issues that cannot be reliably confirmed through automation alone.

### FR-08: Report Generation
The system shall generate a downloadable report containing scan results, detected issues, and relevant recommendations.

### FR-09: Scan Error Handling
The system shall inform users when a webpage cannot be accessed or a scan fails, distinguishing technical failures from accessibility findings.

## 5. Non-Functional Requirements

### NFR-01: Usability
The application shall present scan results, explanations, and fix suggestions in a clear and understandable format suitable for beginner web developers and non-technical website owners.

### NFR-02: Performance
The application should complete scans of supported public webpages within a reasonable amount of time. Scan duration may vary depending on page complexity, network conditions, and browser loading behavior.

### NFR-03: Security
The application shall validate submitted URLs and restrict access to localhost, private networks, and other prohibited destinations to reduce the risk of Server-Side Request Forgery (SSRF).

### NFR-04: Reliability
The application shall handle inaccessible webpages, timeouts, and scanning errors gracefully and inform users when a scan cannot be completed.

### NFR-05: Maintainability
The application shall use a modular structure so that scanning, result processing, issue explanations, fix suggestions, and report generation can be maintained independently.

### NFR-06: Compatibility and Responsiveness
The application should provide a usable interface on commonly used modern browsers and adapt to desktop, tablet, and mobile screen sizes.

### NFR-07: Accessibility of the Application
The application's own interface shall follow relevant accessibility practices, including keyboard accessibility, appropriate form labels, sufficient color contrast, and meaningful interface structure.

### NFR-08: Accuracy and Transparency
The application shall distinguish automatically detected issues from items requiring manual review. It shall not claim that a webpage is fully accessible solely because automated checks found no issues.

## 6. MVP Scope

The Minimum Viable Product (MVP) will focus on scanning one public webpage at a time and helping users understand and address selected common accessibility issues.

### 6.1 Features Included in the MVP

The MVP shall include:

- Submission and validation of a public webpage URL.
- Automated accessibility checks for selected common issues.
- Display of detected issues and available severity information.
- Plain-language explanations of detected issues.
- Relevant WCAG references when reliable.
- Practical fix suggestions and code examples where appropriate.
- Guidance for checks requiring manual review.
- A downloadable report containing scan results and recommendations.
- Clear error messages when a scan cannot be completed.

### 6.2 MVP Limitations

The MVP will have the following limitations:

- Only one webpage will be scanned per request.
- Automated checks will cover selected issues rather than every possible accessibility barrier.
- Some accessibility issues will require manual review.
- Fix suggestions will not automatically modify the live website.
- The application will not guarantee full WCAG compliance.

The MVP will prioritize a complete, understandable workflow over a large number of features.

## 7. Out of Scope

The following features are excluded from the initial MVP to keep development focused and achievable:

- **Full-site crawling:** Scanning every page of a website automatically.
- **Automatic live-site modification:** Applying fixes directly to a user's website.
- **Complete WCAG compliance verification:** Guaranteeing that a website meets every applicable accessibility requirement.
- **Detection of every accessibility issue:** Identifying all possible barriers, including issues that require human judgment.
- **User accounts and team collaboration:** Providing registration, login, shared workspaces, or team management.
- **Enterprise-scale features:** Supporting large-scale organizational workflows and advanced administration.
- **Advanced customization:** Providing extensive configuration of scan rules, reports, or organizational policies.

These features may be considered for future versions after the core MVP has been implemented and evaluated.

## 8. Assumptions and Constraints

### 8.1 Assumptions

The project is based on the following assumptions:

- Users will submit publicly accessible webpage URLs.
- The target webpage can be accessed by the scanning system using a supported browser automation setup.
- Automated accessibility testing tools can identify selected common accessibility issues.
- Beginner web developers and small-business website owners will benefit from plain-language explanations and practical fix suggestions.
- Some accessibility issues will require human judgment and cannot be fully evaluated through automated checks alone.

### 8.2 Constraints

The project has the following constraints:

- **Development time:** The initial version must remain achievable within the available project development period.
- **Technical limitations:** Scan results may depend on webpage structure, dynamic content, network conditions, and browser behavior.
- **Automation limitations:** Automated testing cannot reliably identify every accessibility barrier or establish complete WCAG compliance.
- **Security requirements:** The system must restrict unsafe URL destinations and prevent unauthorized access to internal network resources.
- **Resource limitations:** Development and testing must remain manageable with the available hardware, software, and resources.

These assumptions and constraints will guide technical decisions and help define realistic expectations for the MVP.