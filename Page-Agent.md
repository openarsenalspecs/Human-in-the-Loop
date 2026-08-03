# Page-Agent Specification

Page-Agent is a modular open specification for building AI-driven browser agents that understand natural language, analyze web pages, and perform interactive tasks through a secure, extensible architecture.

The specification defines standardized interfaces for browser interaction, AI reasoning, automation workflows, security, user oversight, knowledge management, voice interaction, scheduling, licensing, autonomous operation, monitoring, and extension development.

Originally inspired by the Alibaba Page-Agent project, this specification expands the concept into a modular ecosystem where core capabilities are built into the foundation and advanced capabilities can be added through optional plugin modules.

**Original Repository:** https://github.com/alibaba/page-agent

---

# Modular Design

Page-Agent uses a modular architecture separating required functionality from optional extensions.

Core modules define the required capabilities of compliant implementations.

Optional plugin modules expand functionality without requiring changes to the core architecture.

---

# Core Modules

## Natural Language Interface

Provides standardized APIs for interpreting user instructions written in natural language and converting them into structured automation tasks.

Features include:

- Natural language command parsing
- Intent extraction
- Context-aware instruction processing
- Multi-step task planning
- Conversation state management

---

## Semantic DOM Engine

Provides AI-assisted semantic understanding of web page structures beyond traditional selectors.

Features include:

- Intent-based element discovery
- Semantic element identification
- Accessibility tree analysis
- Layout understanding
- Context-aware element matching
- Dynamic DOM adaptation
- Resilient element targeting

---

## DOM Interaction Engine

Defines standardized interfaces for interacting with web pages.

Features include:

- DOM discovery
- Element identification
- Dynamic selector generation
- Shadow DOM support
- Event triggering
- Form interaction
- Accessibility-aware element detection

---

## AI Agent Runtime

Provides the execution environment for AI-assisted browser automation.

Features include:

- Task execution pipeline
- Reasoning workflows
- Action scheduling
- Error recovery
- Execution state management
- Agent lifecycle management

---

## Autonomous Agent Mode

Provides controlled autonomous operation capabilities while maintaining user-defined permissions, safety boundaries, and oversight.

Features include:

- Goal-based task execution
- Long-running workflows
- Autonomous decision-making
- Self-monitoring
- Recovery workflows
- Scheduled autonomous tasks
- User-defined boundaries
- Human escalation when required
- Autonomous execution policies

---

## LLM Provider Interface

Provides a vendor-neutral abstraction layer for language models.

Features include:

- Multiple AI provider support
- Local model support
- Remote API support
- Model capability detection
- Failover support
- Prompt management

---

## Client Runtime

Defines browser-side execution requirements.

Features include:

- Client-side processing
- Browser compatibility
- Session management
- Resource optimization
- Offline operation support
- Runtime security controls

---

## Knowledge Base

Provides a standardized repository for storing and retrieving information used by browser agents.

Features include:

- Local knowledge storage
- User preferences
- Page metadata
- Semantic indexing
- Retrieval interfaces
- Knowledge organization
- Search capabilities

---

## Configuration Manager

Provides centralized configuration management for the Page-Agent ecosystem.

Features include:

- Global configuration
- Module configuration
- Environment profiles
- Runtime configuration updates
- Configuration validation
- Secure configuration storage
- Import and export support

---

## Human-in-the-Loop (HITL)

Provides user oversight between AI decision-making and action execution.

Features include:

- Action review
- Approval workflows
- Action modification
- Execution rejection
- Safety confirmations
- User intervention
- Audit logging

---

## Speech Interface

Provides voice-based interaction with browser agents.

Features include:

- Speech recognition
- Text-to-speech
- Voice command processing
- Wake word support
- Continuous listening
- Voice confirmations
- Multi-language speech support

---

## Scheduler

Provides standardized scheduling and automation capabilities.

Features include:

- Scheduled task execution
- Recurring jobs
- Delayed execution
- Event-based triggers
- Calendar integration
- Job management
- Retry policies

---

## Security Framework

Defines baseline security requirements.

Features include:

- Permission management
- Origin validation
- Content sanitization
- CSP compatibility
- Secure storage
- API credential protection
- Security policies

---

## Digital Rights Management

Provides a framework for managing ownership, licensing, permissions, and authorized use of agents, modules, and capabilities.

Features include:

- Module licensing support
- Capability usage controls
- License verification
- Attribution tracking
- Commercial deployment management
- Rights enforcement
- Usage auditing
- Digital ownership records
- Contribution tracking

---

## Monitoring & Observability Module

Provides visibility into agent operations, system performance, and automation behavior.

Features include:

- Agent activity logs
- Performance metrics
- Distributed tracing
- Error tracking
- Execution analytics
- Resource monitoring
- Workflow monitoring
- Security event monitoring
- Health checks
- Operational dashboards

---

## Security & Privacy Module

Provides protection for user data and AI interactions.

Features include:

- Data classification
- Privacy controls
- Secure data handling
- Encryption support
- Local-first processing
- Data retention policies
- Privacy auditing

---

## Core API

Defines standardized communication interfaces between modules.

Features include:

- Module registration
- Event interfaces
- Lifecycle hooks
- Configuration management
- Capability discovery
- Extension interfaces

---

## Event Bus

Provides communication between system modules.

Features include:

- Publish and subscribe messaging
- Event routing
- Event filtering
- Priority handling
- Asynchronous communication
- Module notifications

---

## Capability Registry

Allows modules to advertise and discover available functionality.

Features include:

- Module discovery
- Version negotiation
- Dependency management
- Capability detection
- Health monitoring

---

## Extension SDK

Provides a standardized development framework for building compatible extensions.

Features include:

- Plugin APIs
- Module lifecycle management
- Extension hooks
- Development utilities
- Testing framework
- Documentation generation
- Version compatibility tools

---

# Optional Plugin Modules

Optional plugin modules expand Page-Agent functionality.

---

## End-to-End Encryption (E2EE)

Provides secure encrypted communication for sensitive browser interactions.

Features include:

- Client-side encryption
- AES-256 encryption
- Session key management
- Secure key exchange
- Encrypted prompts
- Encrypted responses

---

## Multi-Agent Collaboration

Enables multiple agents to coordinate tasks.

Features include:

- Agent communication
- Shared context
- Task delegation
- Distributed workflows
- Collaborative execution

---

## Browser Automation Extensions

Adds specialized browser automation features.

Features include:

- Multi-tab automation
- Cross-window workflows
- Popup handling
- File uploads
- Downloads
- Clipboard automation

---

## Computer Vision

Adds visual understanding capabilities.

Features include:

- Screenshot analysis
- OCR
- Image recognition
- Visual element detection
- Screen comparison

---

## Workflow Automation

Provides reusable automation workflows.

Features include:

- Workflow builder
- Conditional logic
- Loops
- Templates
- Execution history
- Workflow sharing

---

## Memory Module

Provides persistent agent memory.

Features include:

- Long-term memory
- Short-term memory
- Memory retrieval
- User-controlled memory
- Semantic recall

---

## Retrieval-Augmented Generation (RAG)

Adds document and knowledge retrieval capabilities.

Features include:

- Document indexing
- Vector search
- Knowledge retrieval
- Source references
- Multi-source information access

---

## Policy Engine

Provides governance and compliance controls.

Features include:

- Action policies
- Domain restrictions
- Permission rules
- Approval requirements
- Compliance enforcement

---

## Audit & Compliance

Provides detailed activity tracking.

Features include:

- Action history
- User approvals
- Change tracking
- Compliance reports
- Digital signatures

---

## Browser Extension Integration

Provides browser extension deployment support.

Features include:

- Chrome support
- Firefox support
- Edge support
- Brave support
- Extension APIs

---

## Marketplace

Provides a community ecosystem for modules.

Features include:

- Plugin registry
- Module discovery
- Version management
- Dependency resolution
- Digital signatures

---

## Translation & Localization

Provides multilingual support.

Features include:

- Multi-language commands
- Interface localization
- Language detection
- Regional formatting

---

## Federated Agent Network

Enables independent Page-Agent deployments to communicate.

Features include:

- Agent discovery
- Federated communication
- Trust management
- Cross-instance collaboration

---

## API Gateway

Provides external service integration.

Features include:

- REST adapters
- GraphQL adapters
- WebSocket support
- Authentication middleware
- Rate limiting

---

# Design Principles

- Modular architecture
- Vendor-neutral interfaces
- Local-first execution
- Privacy-first design
- Human-controlled automation
- Secure by default
- Extensible plugin ecosystem
- Cross-browser compatibility
- Open governance
- Community-driven development
- Digital rights awareness
- AGPL-3.0+ licensing

---

## End-to-End Encryption (E2EE)

**Contribution by Roxanne Ardary, [roxanneardary.com](https://www.roxanneardary.com/)**  
**License:** [AGPL 3.0+](https://www.gnu.org/licenses/agpl-3.0.en.html)  

Page-Agent now supports end-to-end encryption for sensitive user data, ensuring that all commands and page interactions remain secure.

### How It Works

- **Client-Side Encryption:** User inputs and prompts are encrypted in the browser using AES-256 before being sent to any server or API.
- **Encrypted Communication:** Encrypted data is sent over HTTPS. The server or API only sees encrypted payloads and cannot access plaintext commands or page content.
- **Decryption in Browser:** Responses from the server or AI API are decrypted locally in the browser before execution.
- **Key Management:** Encryption keys are generated per session and never stored on the server, ensuring that only the user can decrypt their data.

### Example Usage

```js
import CryptoJS from "crypto-js";

// Encrypt a command
const key = CryptoJS.enc.Utf8.parse(sessionKey);
const iv = CryptoJS.lib.WordArray.random(16);
const encrypted = CryptoJS.AES.encrypt(
  JSON.stringify({ command: "Click the login button" }),
  key,
  { iv: iv }
).toString();

// Decrypt a response
const decrypted = CryptoJS.AES.decrypt(encryptedResponse, key, { iv: iv });
console.log(decrypted.toString(CryptoJS.enc.Utf8));
```
> ⚠️ Note: For true end-to-end encryption, avoid sending the encryption key to the server. Keys should be generated per session and managed only in the browser.

## Example Integration

```js
import { PageAgent } from 'page-agent'

const agent = new PageAgent({
  modelName: 'PAGE-AGENT-FREE-TESTING-RANDOM',
  baseURL: 'https://…',
  apiKey: '…'
})

await agent.execute('Click the login button')
```

## Use Cases

- **AI Copilot for Web Apps:** Provide natural-language control inside your web app.  
- **Smart Form Filling:** Describe workflows instead of writing manual scripts.  
- **Accessibility:** Enable natural-language interaction for users with disabilities.

## Human-in-the-Loop (HITL)

The Human-in-the-Loop (HITL) feature in Page-Agent introduces a user verification layer between AI interpretation and action execution on a web page.

Instead of immediately executing AI-generated commands, the system pauses and presents the proposed action to the user for review and approval.

### How It Works

1. The user issues a natural language command (e.g., "Click the login button").
2. The AI interprets the command and generates a proposed DOM action.
3. The action is sent to the HITL interface for review.
4. The user can:
   - **Approve** the action → it is executed on the page
   - **Reject** the action → it is discarded
   - **Modify** the action → it is re-evaluated before execution

### Benefits

- Prevents unintended or unsafe automation actions
- Gives users full control over AI-driven interactions
- Improves transparency of AI decision-making
- Enhances safety in sensitive workflows (forms, payments, data entry)

### Summary

HITL ensures that Page-Agent remains a collaborative system where AI assists execution, but the final control always remains with the user.

## License

This project includes contributions under **two licenses**:

1. **Original Page-Agent Code and Full README.md**  
   - Author: [Alibaba Page-Agent](https://github.com/alibaba/page-agent)   
   - License: [MIT License](https://opensource.org/licenses/MIT)  
   - Original repository: [https://github.com/alibaba/page-agent](https://github.com/alibaba/page-agent)  

2. **End-to-End Encryption (E2EE) and Human in the Loop (HITL) Addition**  

---

## Specification Branding License (SBL)

### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/page-agent/](https://roxanneardary.com/page-agent/)

---
   
### License & Notice Requirements

Page-Agent is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.  By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- Page-Agent specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- Open Arsenal specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.

**Usage Note:**  
- Original MIT code may be used under the terms of the [MIT License](https://opensource.org/licenses/MIT).  
- Any use of the E2EE or HITL features, or derivative works that include it, must comply with [AGPL 3.0+](https://www.gnu.org/licenses/agpl-3.0.en.html), including proper attribution to **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
