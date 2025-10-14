# Theme Overview
Accessibility testing remains challenging due to **labor-intensive** processes, **expensive** tooling, and the difficulty of testing without personal experience using assistive technologies. There's also **over-reliance on automated tools** that cannot solve all accessibility problems.


# Recommended Next Steps
While we did identify many items within each of the following categories, this was not an exhaustive discussion, and our strongest focus for change was on the community support needs.
If we were to continue the discussion with a fresh take on the categories, knowing what we now know, the conversation would be focused primarily on **engaging the open-source community to create concerted efforts to test for accessibility.**
In practice, we referred often to the current state of cybersecurity as a great example on crowdsourcing testing. Through CTFs, bug bounties, and many other incentives, a culture has been created focused on responsibly testing the cybersecurity posture of open-source and public projects.
We see this as the goal for accessibility: **Incentivizing the open-source community to crowd-test the accessibility of public projects, software, websites, and anything else they can.**


# Categories, summaries, and sticky notes
During the small group, we used sticky notes to identify elements of five categories of the challenege of testing and tooling: Key Challenges, Solution Approaches, Success Metrics, Action Plan, and Community Support Needs.

| Key Challenges | Solution Approaches | Success Metrics | Action Plan | Community Support Needs |
|---|---|---|---|---|
| **Overview:** Testing tools don't accurately reflect or address the needs of all. | **Options:** <br>• Training <br>• Culture <br>• AI-based testing <br>• User-based testing | **Overview:** Hard to prove success - the more specific the disability, the less % of the user-base. | **Overview:** Many steps are available for internal- or project-based testing, but don't influence the community as a whole. | **Overview:** Success happens when the lowest common denominator is engaged with the effort. Incentivize the community to build adoption. |
| **Staffing** | More accessibility training (e.g., test your websites, monitor) | Increase in accessibility users through web traffic | Sell financial & moral value of accessibility to leadership | Create a "Step 0" to lower the floor for getting engaged with Accessibility development. |
| **Leading testing by someone lacking experience** (e.g., in usability and accessibility) | Improve accessibility (e.g., close gap between designer/developer/tester) | Accessibility friendly bridges | Design a unified design system | Drive interest in accessibility through community challenges |
| **Ambiguity in standards** or how to make something accessible | Change global culture | Decrease in lawsuits | Automate accessibility tests covered by design system | Raise awareness of tools (e.g., Lighthouse, axe, Wave) |
| **Specific App challenges**, i.e. "Screen reader in a terminal" | AI-based testing | **Time-to-success** <br>• Time-to-degree <br>• Time-to-certification, etc | Introduce an accessibility training program (e.g., gamification) | Promote a culture of visibility / reporting |
| **Multiple accessibility standards** and required skillsets (e.g., in a team) | Target accessibility efforts on areas that need them | | Employment contract commitment for developers, project managers, special heads (e.g., accessibility leads) | |
| **Scope of testing** | Evaluate universal accessibility vs. accessibility-specific implementation | | Self-training of at least one accessibility skill per month | |
| **Manual testing / Resources / Availability of tools** | | | Centralized reporting (e.g., for project managers, product managers, designers) | |
| **Universal Availability vs. Accessibility** | | | Design a mix of dev/tester teams (maybe with accessibility resources) | |
| | | | Add different testing arrays (e.g., devices, operating systems, tools) | |


---

# Resources Breakdown
## Overview
1. [Resource Categories](#resource-categories)
2. [Community Integration Concepts](#community-integration-concepts)
3. [Quick Reference](#quick-reference)
4. [Appendices](#appendices)

---

## Resource Categories

### 🎯 W3C Standards & Guidelines

#### **Web Content Accessibility Guidelines (WCAG) 2.2** 
- **URL**: [https://www.w3.org/TR/WCAG22/](https://www.w3.org/TR/WCAG22/)
- **Priority**: 🔴 Critical (P0)
- **Implementation Value**: Primary compliance standard for all web accessibility
- **Open Source Application**:
  - Baseline compliance framework
  - Automated testing criteria
  - Code review checklists
  - Documentation standards

---

### 🔧 Testing Tools & Automation

#### **axe-core (Deque Labs)**
- **URL**: [https://github.com/dequelabs/axe-core](https://github.com/dequelabs/axe-core)
- **Priority**: 🔴 Critical (P0)
- **Implementation Value**: Industry-standard automated accessibility testing engine
- **Technical Details**:
  - **License**: Mozilla Public License 2.0 (Open Source)
  - **Integration**: Jest, Cypress, Playwright, Selenium
  - **Language**: JavaScript/TypeScript
- **Open Source Implementation**:
  ```bash
  # npm installation
  npm install --save-dev @axe-core/cli @axe-core/playwright
  
  # CI/CD integration example
  npx axe --load-delay=3000 http://localhost:3000
  ```

#### **Google Lighthouse Accessibility**
- **URL**: [https://developer.chrome.com/docs/lighthouse/accessibility/scoring](https://developer.chrome.com/docs/lighthouse/accessibility/scoring)
- **Priority**: 🟡 High (P1)
- **Implementation Value**: Built-in DevTools accessibility auditing
- **Open Source Implementation**:
  ```bash
  # CLI usage
  npx lighthouse --only-categories=accessibility --output=json --output-path=./accessibility-report.json http://localhost:3000
  ```

#### **WAVE Web Accessibility Evaluation Tools**
- **URL**: [https://wave.webaim.org/](https://wave.webaim.org/)
- **Priority**: 🟡 High (P1)
- **Implementation Value**: Visual accessibility issue identification
- **Open Source Application**:
  - Developer education and training
  - Quick accessibility audits
  - Visual feedback for designers

#### **Firefox Accessibility Simulator dev tool**
-   **URL**: [https://addons.mozilla.org/en-US/firefox/addon/accessibility-simulator/](https://addons.mozilla.org/en-US/firefox/addon/accessibility-simulator/)
-   **Priority**: 🟢 Medium (P2)
-   **Implementation Value**: Simulates different types of disabilities to test web accessibility
-   **Technical Details**:
  - **Integration**: Firefox Developer Edition
  - **Features**: Simulates color-blindness, blurred vision, and more

#### **Chrome Accessibility Developer Tools (Legacy)**
- **URL**: [https://github.com/GoogleChrome/accessibility-developer-tools](https://github.com/GoogleChrome/accessibility-developer-tools)
- **Priority**: ⚪ Reference (P3)
- **Implementation Value**: Historical reference, largely superseded by axe-core
- **Note**: Now considered legacy; use axe-core or Lighthouse for new projects

---

### 🏢 Professional Resources & Training

#### **Deque Systems**
- **Primary URLs**: 
  - [https://github.com/dequelabs](https://github.com/dequelabs) (GitHub Organization)
  - [https://www.deque.com/resources/](https://www.deque.com/resources/)
  - [https://www.deque.com/training/](https://www.deque.com/training/)
- **Priority**: 🔴 Critical (P0)
- **Implementation Value**: Leading accessibility company with extensive open source contributions
- **Open Source Contributions**:
  - axe-core testing engine
  - axe-playwright integration
  - React accessibility patterns
  - Training materials and best practices

---

### 🎓 Certification Programs

#### **International Association of Accessibility Professionals (IAAP)**
- **CPACC Certification**: [https://www.accessibilityassociation.org/cpacc](https://www.accessibilityassociation.org/cpacc)
- **WAS Certification**: [https://www.accessibilityassociation.org/was-exam](https://www.accessibilityassociation.org/was-exam)
- **Priority**: 🟢 Medium (P2)
- **Implementation Value**: Professional certification for team development
- **Open Source Application**:
  - Team skill development programs
  - Project credibility enhancement
  - Professional development pathways

---

### 🤝 Community & Learning Resources

#### **Open Source Accessibility Community**
- **Center for Accessibility & Open Source**: [https://caos.org/](https://caos.org/)
- **Summit Participation**: Active engagement in Open Source Accessibility Summit planning
- **Priority**: 🔴 Critical (P0)
- **Implementation Value**: Direct community engagement and collaboration platform
- **Open Source Application**:
  - Knowledge sharing and problem-solving
  - Project coordination and collaboration
  - Best practice development
  - Real-time support and mentoring

#### **Web.dev Learn Accessibility**
- **URL**: [https://web.dev/learn/accessibility](https://web.dev/learn/accessibility)
- **Priority**: 🔴 Critical (P0)
- **Implementation Value**: Comprehensive learning resource with practical examples
- **Open Source Application**:
  - Educational materials for developer onboarding
  - Code examples and implementation patterns
  - Progressive enhancement strategies
  - Performance-accessibility optimization

#### **Web.dev Accessibility Review Guide**
- **URL**: [https://web.dev/articles/how-to-review](https://web.dev/articles/how-to-review)
- **Priority**: 🟡 High (P1)
- **Implementation Value**: Systematic approach to accessibility reviews
- **Open Source Application**:
  - Code review processes and checklists
  - Quality assurance workflows
  - Pull request review guidelines

---
### 🛠️ Assistive Technology & Testing

#### **NVDA Screen Reader**
- **URL**: [https://www.nvaccess.org/download/](https://www.nvaccess.org/download/)
- **Priority**: 🟡 High (P1)
- **Implementation Value**: Free, open-source screen reader for testing
- **Technical Details**:
  - **Platform**: Windows
  - **License**: GPL v2 (Open Source)
  - **Community**: Large user and developer community
- **Open Source Application**:
  - User testing and validation workflows
  - Development environment setup
  - Real-world usage validation
  - Cost-effective alternative to expensive screen readers

#### **National Center for Computing for the Blind (NCCB)**
- **URL**: [https://nccbinfo.org/](https://nccbinfo.org/)
- **Priority**: 🟢 Medium (P2)
- **Implementation Value**: Resources for developers with visual impairments
- **Open Source Application**:
  - Inclusive development practices
  - Developer accessibility resources and training

---

### 💻 Implementation Libraries & Frameworks

#### **Facebook Lexical Editor**
- **URL**: [https://github.com/facebook/lexical](https://github.com/facebook/lexical)
- **Description**: "Extensible text editor framework that provides excellent reliability, accessibility and performance"
- **Priority**: 🟡 High (P1)
- **Implementation Value**: Production-ready accessible rich text editor
- **Technical Details**:
  - **License**: MIT (Open Source)
  - **Framework**: React-based
  - **Features**: Built-in accessibility, extensible architecture
- **Open Source Application**:
  - Accessible rich text editing components
  - Modern web editor implementation patterns
  - Accessibility-first design examples

---

### 📊 User Research & Testing

#### **Medium: Testing with Blind Users**
- **URL**: [https://medium.com/design-bridges/accessibility-testing-babe2d84e817](https://medium.com/design-bridges/accessibility-testing-babe2d84e817)
- **Title**: "Testing sites and apps with blind users: a detailed cheatsheet"
- **Priority**: 🟡 High (P1)
- **Implementation Value**: Detailed guidance on user testing with visually impaired users
- **Open Source Application**:
  - User testing methodology development
  - Inclusive design research processes
  - Validation and feedback collection strategies

---

## Community Integration Concepts
- Join Open Source Accessibility Slack workspace
- Set up weekly accessibility review meetings
- Subscribe to web.dev accessibility updates

#### 1. Professional Development
- Enroll team members in IAAP certification programs
- Set up accessibility training schedule
- Create internal accessibility champions program

#### 2. Enterprise Patterns
- Review Enterprise accessibility documentation
- Implement VPAT reporting for your projects
- Create accessibility conformance report templates

#### 3. User Testing Program
- Implement user testing with disabled users
- Create feedback collection systems
- Establish regular accessibility user sessions

#### 4. Custom Tool Development
- Contribute to open source accessibility tools
- Develop project-specific accessibility utilities
- Create accessibility linting rules

---

## Quick Reference

### 📋 Essential Bookmarks

| Category | Resource | URL | Quick Action |
|----------|----------|-----|--------------|
| **Standards** | WCAG 2.2 | [Link](https://www.w3.org/TR/WCAG22/) | Bookmark for daily reference |
| **Testing** | axe-core | [GitHub](https://github.com/dequelabs/axe-core) | Star and follow releases |
| **Learning** | web.dev/learn/accessibility | [Link](https://web.dev/learn/accessibility) | Add to learning path |
| **Community** | Open Source A11y Slack | [Join](https://opensourceacc-kab3997.slack.com/) | Join workspace |
| **Tools** | WAVE | [wave.webaim.org](https://wave.webaim.org/) | Install browser extension |

---

## Appendices

### A. Complete Resource URLs

#### Standards & Guidelines
- WCAG 2.2: https://www.w3.org/TR/WCAG22/
- Web.dev Learn Accessibility: https://web.dev/learn/accessibility
- Web.dev Review Guide: https://web.dev/articles/how-to-review

#### Testing Tools
- axe-core: https://github.com/dequelabs/axe-core
- Lighthouse Documentation: https://developer.chrome.com/docs/lighthouse/accessibility/scoring
- WAVE: https://wave.webaim.org/
- Chrome A11y DevTools (Legacy): https://github.com/GoogleChrome/accessibility-developer-tools

#### Professional Resources
- Deque Systems GitHub: https://github.com/dequelabs
- Deque Resources: https://www.deque.com/resources/
- Deque Training: https://www.deque.com/training/

#### Certifications
- IAAP CPACC: https://www.accessibilityassociation.org/cpacc
- IAAP WAS: https://www.accessibilityassociation.org/was-exam

#### Assistive Technology
- NVDA Download: https://www.nvaccess.org/download/
- NCCB: https://nccbinfo.org/

#### Implementation
- Facebook Lexical: https://github.com/facebook/lexical
- Testing with Blind Users (Medium): https://medium.com/design-bridges/accessibility-testing-babe2d84e817

### B. Search Keywords for Reference

**Primary Keywords**: accessibility, a11y, wcag, aria, axe-core, lighthouse, deque, nvda, screen reader, inclusive design

**Secondary Keywords**: web accessibility, digital accessibility, assistive technology, accessibility testing, accessibility compliance, universal design, accessibility automation

**Tool-Specific**: axe-core, lighthouse-ci, wave-webaim, nvda-testing, accessibility-developer-tools

### C. Version Information

- **WCAG**: Version 2.2 (Current as of 2025)
- **axe-core**: Latest stable (check GitHub releases)
- **Lighthouse**: Bundled with Chrome DevTools
- **NVDA**: Latest stable release recommended

