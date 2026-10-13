# 🛡️ Digital Risk Protection System

### Evidence-Based Brand Trust & Risk Analyzer

A web-based application designed to help users assess potentially suspicious websites and public social media profiles. It analyzes available signals, highlights warning indicators, and presents the findings in an easy-to-understand report.

The goal is to support safer online decisions through evidence-based assessments rather than making unsupported claims about a website or profile's legitimacy.

---

## 📖 Overview

The Digital Risk Protection System provides a centralized interface for reviewing potentially deceptive websites and public profiles.

Users can submit a website URL or supported public-profile information for assessment. The application presents available risk indicators, a risk score, supporting evidence, and recommended verification steps.

By explaining what was observed and what still needs to be verified, the system helps users better understand potential online risks.

**Important:** A risk score is an indicator based on available evidence and configured rules. It is not a probability of fraud or a guarantee that a website is safe.

---

## ❗ Problem Statement

Online impersonation and fraudulent websites can create risks for individuals, customers, and businesses. Suspicious pages may imitate trusted brands, redirect visitors to unfamiliar websites, or request sensitive information.

Manually verifying these pages can be time-consuming, especially when the available evidence comes from different sources.

Common challenges include:

- Identifying suspicious website redirects.
- Recognizing warning signs on public profiles.
- Understanding why a website or profile requires further investigation.
- Reviewing the evidence behind a risk assessment.
- Distinguishing technical security indicators from proof of legitimacy.

## 💡 Proposed Solution

The Digital Risk Protection System brings the available assessment checks into a single interface.

It examines user-submitted information, reviews the signals available in the current implementation, and presents the results in a structured report.

Users can review the findings and follow the recommended precautions before interacting with a suspicious website or profile.

The solution focuses on **clear evidence, understandable risk summaries, and informed human decision-making**.

---

## ✨ Features

### 1. Website Analysis
- Accepts a website URL for assessment.
- Identifies configured URL-related and redirect indicators.
- Displays the observations used in the assessment.

### 2. Public Profile Assessment
- Supports the assessment of submitted public-profile information where the relevant checks are implemented.
- Highlights available warning signals.
- Encourages independent verification of profile ownership.

### 3. Risk Scoring
- Calculates a score using the configured analysis rules.
- Displays the corresponding risk category.
- Shows the signals contributing to the result.

### 4. Evidence Reports
- Separates warning findings from informational observations.
- Displays supporting evidence and assessment details.
- Includes confidence or coverage information where available.

### 5. Saved Reports
- Allows users to revisit previously saved assessments.
- Provides access to report history within the supported storage scope.
- Offers report-retention settings.

### 6. Recommended Actions
- Advises users to verify unfamiliar domains.
- Encourages the use of independently obtained contact information.
- Warns against sharing passwords, one-time codes, or payment details before verification.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| React | Frontend user interface |
| Vite | Frontend development and build tooling |
| Python | Backend programming language |
| FastAPI | Backend API framework |
| SQLite | Lightweight database, where implemented |
| OpenAI API | Text interpretation and explanation generation, when enabled |
| VirusTotal API | URL and domain reputation lookup, when configured |
| Git and GitHub | Version control and project collaboration |

---

## 🔄 Application Workflow

1. **Submit information:** The user enters a website URL or supported public-profile details.
2. **Validate input:** The backend checks whether the submitted information is valid.
3. **Analyze indicators:** The system evaluates the checks available in the implementation.
4. **Retrieve external information:** Configured integrations may provide additional text-analysis or reputation information.
5. **Calculate risk:** The analysis engine combines available signals according to its scoring rules.
6. **Generate a report:** The interface displays the risk score, findings, and relevant limitations.
7. **Review the evidence:** The user examines the findings and independently verifies important information.

### Workflow Diagram

```text
User Input
    ↓
Input Validation
    ↓
Signal Analysis
    ↓
External Lookups (if configured)
    ↓
Risk Scoring
    ↓
Evidence Report
    ↓
Human Verification
```

---

## 📊 Risk Analysis

The system uses observable signals to help users identify situations that may require further investigation.

| Observation | Interpretation |
|---|---|
| Redirect to another hostname | Inspect the destination domain and confirm that the redirect is expected. |
| Password request detected | Verify the page and organization before entering credentials. |
| Valid HTTPS certificate | Indicates that the connection uses a valid TLS certificate, but does not prove that the organization is trustworthy. |
| Incomplete reputation information | Indicates that additional verification may be necessary. |

### Example Assessment Results

- **Website assessment:** Risk score of 10, categorized as Low Risk, with a redirect-related warning.
- **Instagram assessment:** Risk score of 30, categorized as Moderate Risk, with redirect and password-request indicators.

These scores describe the specific examples assessed. They are not definitive judgments about the organizations or platforms involved.

### Understanding Risk Scores

Risk categories and thresholds should match the rules configured in the implementation. Scores should not be presented as statistically validated probabilities unless the scoring model has been appropriately designed and tested.

---

## 🔌 API Integrations

### OpenAI API

The OpenAI API can support the interpretation of relevant submitted text and the generation of readable explanations when enabled in the application.

**Potential uses:**
- Identifying suspicious wording in submitted page or profile text.
- Explaining why a configured rule raised a concern.
- Converting technical observations into user-friendly explanations.

The API does not independently certify a website, verify account ownership, or guarantee that an assessment is correct.

### VirusTotal API

The VirusTotal API can provide reputation information for submitted URLs or domains when the integration is configured and access is available.
**Potential uses:**
- Retrievingavailable URL and domain reputation information.
- Adding third-party signals to the assessment.
- Supporting further investigation of potentially suspicious links.

Reputation results may be incomplete or unavailable. Missing information must not be interpreted as proof that a URL is safe.

---

## 🔐 Privacy and Security

The application should follow appropriate security practices when handling submitted information and external services.

- Store API keys in environment variables or a secret manager.
- Never commit API credentials to a public GitHub repository.
- Send only the information necessary for an assessment to external services.
- Explain when submitted text may be processed by an external AI provider.
- Avoid collecting passwords, one-time codes, or unnecessary personal information.
- Treat external reputation results as supporting evidence rather than definitive proof.
- Validate URLs and handle unsafe server-side requests and redirects carefully.
- Clearly communicate report storage and retention behavior.

---

## ⚠️ Limitations

The accuracy of an assessment depends on the available evidence and the analysis rules implemented in the application.

- A low-risk score does not guarantee that a website is legitimate.
- A warning does not independently prove malicious intent.
- Third-party reputation data may be unavailable or incomplete.
- AI-generated explanations may contain errors and should be reviewed.
- A dashboard or saved-report feature does not automatically mean continuous monitoring is active.
- Automated platform checks require appropriate, authorized data sources and working integrations.

---

## 🚀 Future Enhancements

Possible improvements include:

- Integrating additional authorized threat-intelligence sources.
- Improving brand-name and public-profile similarity detection.
- Adding automated backend and API tests.
- Expanding report export and review functionality.
- Introducing authenticated users and secure centralized report storage.
- Implementing continuous monitoring when reliable, authorized data sources are available.
- Evaluating and refining risk-scoring rules using representative test cases.

---

## 🎯 Conclusion

The Digital Risk Protection System aims to simplify the review of suspicious websites and public profiles by bringing available indicators, supporting evidence, and practical verification guidance into one interface.

Its main objective is to help users understand why a website or profile may require further investigation and make more informed decisions based on the available evidence.
