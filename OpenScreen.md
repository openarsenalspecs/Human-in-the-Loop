# OpenScreen

OpenScreen is a modular, extensible screen recording and video production platform designed for creators, educators, developers, and businesses. The platform separates recording, editing, automation, AI, and export capabilities into independent modules, allowing new functionality to be added without disrupting the core application.

> **Specification Notice**
>
> The modular architecture described below is a specification created by **Roxanne Ardary** and is licensed under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.
>
> Attribution is required under Section 7 of the license to:
>
> **Roxanne Ardary**
>
> https://www.roxanneardary.com/

---

# Specification

## Design Goals

OpenScreen is designed around several core principles:

- Modular architecture
- Extensible plugin ecosystem
- Human-in-the-Loop AI
- Cross-platform compatibility
- Professional quality exports
- Local-first editing
- Privacy-focused workflows
- Open standards
- Community-driven development

---

# Core Modules

## Screen Capture Engine

Provides the foundation for screen recording across supported operating systems.

### Features

- Full screen recording
- Window recording
- Region recording
- Multi-monitor support
- High resolution capture
- High frame rate recording
- Hardware acceleration
- Recording presets
- Session management

---

## Audio Engine

Handles all audio capture and synchronization.

### Features

- Microphone recording
- System audio capture
- Multiple audio devices
- Audio synchronization
- Noise suppression
- Volume normalization
- Audio monitoring
- Audio mixing

---

## Camera Module

Provides webcam and video overlay capabilities.

### Features

- Webcam recording
- Picture-in-picture
- Camera positioning
- Camera borders
- Circular camera mode
- Camera backgrounds
- Camera effects

---

## Editing Engine

The non-destructive editing environment.

### Features

- Timeline editing
- Clip trimming
- Clip splitting
- Clip merging
- Multi-track editing
- Frame navigation
- Undo history
- Project management

---

## Motion Engine

Provides camera movement and animation effects.

### Features

- Automatic zoom
- Manual zoom
- Pan animations
- Motion blur
- Cursor tracking
- Keyframe animation
- Smooth transitions
- Focus movement

---

## Annotation Module

Provides visual overlays and instructional tools.

### Features

- Text
- Arrows
- Shapes
- Callouts
- Images
- Blur effects
- Highlight effects
- Cursor indicators
- Click animations

---

## Canvas Module

Controls presentation layout.

### Features

- Wallpapers
- Solid backgrounds
- Gradient backgrounds
- Device frames
- Shadows
- Borders
- Padding
- Canvas resizing
- Aspect ratio management

---

## Export Engine

Generates final output.

### Features

- MP4 export
- WebM export
- GIF export
- Multiple resolutions
- Multiple aspect ratios
- Export presets
- Batch rendering
- Hardware encoding

---

# Optional Modules

## AI Assistant

Provides intelligent editing assistance.

### Features

- Caption generation
- Auto summaries
- Voice narration
- Smart editing
- Suggested zooms
- Suggested highlights
- Silence detection
- Editing recommendations

---

## Human-in-the-Loop Engine

Ensures AI remains under user control.

### Features

- AI approval workflows
- Edit review
- Suggestion acceptance
- Suggestion rejection
- Manual overrides
- Confidence indicators
- Explainable AI
- Revision history

---

## Automation Engine

Automates repetitive workflows.

### Features

- Recording automation
- Scheduled recording
- Batch processing
- Workflow automation
- Macro recording
- Event triggers

---

## Collaboration Module

Supports collaborative production.

### Features

- Shared projects
- Comments
- Review workflows
- Version history
- Team workspaces
- Change tracking

---

## Translation Module

Provides multilingual content support.

### Features

- Subtitle generation
- Subtitle translation
- Voice translation
- Localization
- Language detection

---

## Plugin SDK

Allows developers to extend OpenScreen.

### Features

- Plugin API
- Custom exporters
- Custom AI providers
- Custom transitions
- Custom effects
- UI extensions

---

## Cloud Module

Optional synchronization services.

### Features

- Cloud backup
- Project synchronization
- Asset libraries
- Remote rendering
- Shared assets

---

## Analytics Module

Measures application performance.

### Features

- Export analytics
- Recording metrics
- Rendering statistics
- Performance monitoring
- Storage analysis

---

## Accessibility Module

Improves usability for all users.

### Features

- Screen reader support
- Keyboard navigation
- High contrast mode
- UI scaling
- Accessibility shortcuts
- Automatic captions

---

## Theme Engine

Customizes the application appearance.

### Features

- Dark mode
- Light mode
- Custom themes
- Workspace layouts
- Icon packs

---

# Future Modules

The modular architecture allows OpenScreen to continue evolving without redesigning the core platform.

Potential future modules include:

- Live streaming
- Real-time collaboration
- AI workflow orchestration
- Presentation mode
- Template marketplace
- Community plugin registry
- Mobile companion
- Enterprise management
- Federated project sharing
- Remote recording agents
- Workflow scripting
- AI model marketplace

---

# Architecture Principles

- Modular by design
- Plugin-first architecture
- Human-in-the-Loop AI
- Local-first processing
- Privacy-focused
- Cross-platform
- Open standards
- API-driven integration
- Backward compatibility
- Community extensibility

The modular architecture allows every major subsystem to evolve independently while maintaining compatibility with the core recording platform.

---

## AI & Automation Roadmap with Human-in-the-Loop - (AGPL-3.0+)

**Attribution:** This roadmap was created by **Roxanne Ardary** – **[roxanneardary.com](https://www.roxanneardary.com/)**  
**License:** Contributions in this section are licensed under **AGPL 3.0+**.

| Phase | Timeline      | Features                                                                                   |
|-------|---------------|--------------------------------------------------------------------------------------------|
| **Phase 1 – Quick Wins** | 1–3 months    | - Auto Captions / Subtitles (Whisper/Vosk) **[HITL approval for accuracy]**<br>- AI Editing Suggestions (trim silence, highlight action) **[HITL final decisions]**<br>- Hotkey + Macro Automation (start/pause/stop triggers) |
| **Phase 2 – Medium Complexity** | 3–6 months    | - AI Narration / Voice-over (Coqui TTS, ElevenLabs) **[HITL to review voice, tone, pacing]**<br>- Auto-focus / Smart Zoom (mouse tracking + CV element detection) **[HITL confirms zoom/focus points]**<br>- Auto Highlight / Callouts (OpenCV UI detection, animated arrows) **[HITL approves highlights]** |
| **Phase 3 – Advanced AI Features** | 6–12 months   | - Content Summarization / Clip Generation (AI video/audio analysis) **[HITL chooses clips & ordering]**<br>- AI Editing Assistant (suggest edits, transitions, storyboard) **[HITL accepts/rejects edits]**<br>- Auto Voice Modulation (effects: whisper, echo, robotic) **[HITL selects style/effect]** |
| **Phase 4 – Future / Optional** | 12+ months    | - Interactive AI Tutorials (real-time AI guidance) **[HITL controls final content]**<br>- Smart Multi-Source Recording (automatic PiP, app/window selection) **[HITL approves sources & layout]**<br>- Adaptive Auto-Layout (automatic resizing/repositioning for different aspect ratios) **[HITL confirms layout]** |

---

### Legend / Notes
- **Quick Wins:** Minimal AI complexity, fast to implement.  
- **Medium Complexity:** AI assists user workflow, reduces manual editing.  
- **Advanced AI:** AI automates major parts of video creation, improves production quality.  
- **Future:** Cutting-edge AI features for next-gen recording platform.  
- **HITL (Human-in-the-Loop):** User always has final approval for AI decisions, ensuring quality, accuracy, and personal style.

---

## Human-in-the-Loop (HITL) - (AGPL-3.0+)

OpenScreen integrates a **Human-in-the-Loop (HITL)** approach to ensure that all AI-powered features remain **user-controlled, transparent, and high-quality**.

### What is Human-in-the-Loop?
Human-in-the-Loop means that while AI can **suggest, automate, and accelerate workflows**, the **user always has final control and approval** over decisions. This prevents unwanted changes and ensures outputs match the user’s intent.

### How HITL Works in OpenScreen
- **AI Suggestions, Not Decisions:**  
  AI proposes edits (e.g., trims, zooms, highlights), but nothing is applied without user confirmation.
  
- **Approval Checkpoints:**  
  Key actions—such as captions, summaries, zoom focus, and highlights—require user review before being finalized.

- **Editable Outputs:**  
  All AI-generated content (captions, narration, edits) can be modified, rejected, or refined by the user.

- **Transparent Actions:**  
  Users can clearly see what the AI changed or recommends, ensuring full visibility into the editing process.

### Why HITL Matters
- Maintains **creative control** for the user  
- Ensures **accuracy and quality** in recordings  
- Prevents **over-automation mistakes**  
- Supports **professional-grade output** without complex manual editing  

### Examples
- AI suggests removing silent sections → user approves or adjusts timing  
- Auto-generated captions → user reviews and corrects text  
- Smart zoom focuses on UI elements → user confirms or repositions  
- Highlighted buttons or text → user approves or modifies emphasis  

OpenScreen’s HITL design combines the **speed of AI** with the **judgment of the user**, delivering powerful automation without sacrificing control.

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
  - [https://roxanneardary.com/openscreen/](https://roxanneardary.com/openscreen/)

---

## License

OpenScreen Contributions by Roxanne Ardary are released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.  
By contributing to these portions of the project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions to AGPL-designated sections must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- OpenScreen specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.

---

## Links

- siddharthvaddem, Original OpenScreen Repository, Original author – Created: [OpenScreen Repository](https://github.com/siddharthvaddem/openscreen)
