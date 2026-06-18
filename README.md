# Cyberpunk Project Management Matrix (Hackerman Edition)

A high-performance, single-file project management application that wraps core engineering
workflows inside an immersive retro-terminal aesthetic.

---

## 🚀 What is it?
This application is a self-contained, browser-native dashboard designed for agile workflow
monitoring and chronological timeline planning. It features an interactive **Kanban Board**
(`KANBAN_CORE`) synchronized directly with a day-by-day cell **Gantt Chart** (`GANTT_FLOW`).

Built exclusively with Vanilla HTML5, CSS3, and JavaScript, it requires zero external
dependencies, compilation steps, or backend servers. It runs entirely on the client side, using
standard web APIs to manage rendering and state.

---

## ⚙️ Core Functions (The 6 Pillars)
The internal architecture relies on six explicit functional capabilities to maintain full
application synchronization:

1. **State Persistence & Auto-Seeding (`localStorage`):** Reads and writes the entire project
data structure to the browser's persistent storage under the key `HIRE_OS_V7_ELITE`. Spawns
fallback project and developer operative variables if local storage is uninitialized to avoid
blank execution.
2. **Dynamic Project & Team Scoping:** Allows real-time registration of multiple independent
project matrices and operator profiles (`@operatives`) with automatic delete cascading (purging
a project wipes its sub-threads).
3. **Status Stream Kanban Routing:** A 4-stage pipeline layout (`TODO`, `PROCESSING`,
`REVIEW_QA`, `DEPLOYED`) equipped with native HTML5 drag-and-drop mechanics and conditional
visual overlays.
4. **Chronological Gantt Flow Mapping:** Translates start and deadline timestamps into
pixel-perfect floating timeline blocks distributed dynamically across individual day cells for
any target month cycle.
5. **Cross-View Jump Linking:** Click interceptors on the Gantt bars automatically switch the
primary layout view to the Kanban board, trigger a smooth scroll to focus on the target task
card, and execute a 2.5-second white flash-highlight loop.
6. **Data Form Sanitization & Modal Overlays:** Governs interface overlays with explicit input
validation, including automated `min` boundary configuration on calendar selectors to prevent
illogical scheduling logic (deadlines preceding start dates).

---

## 📝 The Blueprint Prompt
To recreate or expand this application from scratch with identical specifications, feed the
following instruction set into an advanced LLM generation agent:
Create a single, self-contained HTML file implementing a fully functional Cyberpunk/Hacker-themed
Project Management Matrix that includes a Kanban Board and a Gantt Chart. The application must run
entirely in the browser using standard Vanilla HTML5, CSS3, and JavaScript, with state persisted via
localStorage.
   1. Color Palette & Visual Theme (The Matrix/Hackerman Aesthetic)
   * Typography: Import and use 'Fira Code', monospace from Google Fonts. All text throughout the
     entire interface must be completely UPPERCASE (except for user-entered descriptions).
   * Colors: Define CSS custom variables matching: --bg-base: #000000; --bg-surface: #050a05;
     --bg-card: #081008; --border-bright: #00ff41; --border-dim: #003b00; --text-main: #00ff41;
     --text-muted: #008f11.
   * Scanline Overlay: Include a low-opacity fixed overlay (pointer-events: none) using linear
     gradients to create a retro CRT monitor raster/scanline effect.
   * Interactivity & Glow: Buttons and cards should have box shadows (0 0 10px var(--border-bright))
     on hover or when active. Active elements invert to text color #000 on a bright green background.

   2. Layout Structure
  Split the full-viewport layout (height: 100vh; overflow: hidden;) into:
   * Left Sidebar (300px width): Contains header logo "NEURAL_LINK_V6.7", a Projects section labeled
     "// PROJECTS" with a [+] button to create projects, and a Team Roster labeled "// TEAM_ROSTER"
     with a [+] button to register operators prefixed with "@". Hovering items reveals edit (✎) or
     delete (×) icons.
   * Main Content Area (Flex-1): Top header shows the current active project name (prefixed with
     "ACTIVE_SESSION: ") and view toggle buttons ("KANBAN_CORE" and "GANTT_FLOW") alongside a "+
     NEW_THREAD" task creation button.

   3. Core Functionality & Views
   * Kanban View (KANBAN_CORE): Display a 4-column layout grid (TODO, PROCESSING, REVIEW_QA, DEPLOYED)
     with inverted headers. Implement native HTML5 Drag and Drop. Hovering a card over a column
     highlights the dropzone with a translucent green background. Task cards must display the title,
     description (text-transform: none), assignee, due date, creation timestamp, and a colored
     priority badge.
   * Gantt Chart View (GANTT_FLOW): Include a center-aligned month indicator framed by "< PREV_CYCLE"
     and "NEXT_CYCLE >" navigation buttons. Render a table grid mapping tasks across individual day
     cells numbered from 1 to the month's maximum length. Tasks spanning the selected month cycle must
     render a floating horizontal block. Gantt bars must be color-coded by priority: critical (Red),
     high (Orange), medium (Cyan), and low (Green).
   * Cross-View Jump Link: Clicking a task's Gantt bar must switch the viewport back to the
     KANBAN_CORE view, smoothly scroll the target task card into center view, and momentarily flash
     its border/shadow pure white for 2.5 seconds.

   4. Data Modals & Validation Overlays
   * Task Modal (TASK_DATA_ENCODING): Fields include Task Header (required text field), Core
     Description (textarea), Start Stamp (date), Deadline Stamp (date), Assigned Operative (dropdown
     from roster), and Priority Level (dropdown). Submitting without a header adds a red warning
     border. The Deadline Stamp min attribute must adjust whenever the Start Stamp changes to prevent
     invalid deadlines.
   * Confirmation Modal ([ TERMINATE_PROTOCOL ]): A custom structural modal used when deleting
     projects, tasks, or members. Renders a red title banner, confirmation query, an "EXECUTE" button
     (styled red), and an "ABORT" option.

   5. State Management & Logic
  Maintain a local JSON database holding arrays for projects, team, and tasks. Persist the structure
  to localStorage under the key: HIRE_OS_V7_ELITE. On application initialization, check if data
  exists; if empty, seed it with a default project ("NEXUS_RECOVERY_PHASE") and a default member
  ("NEO_ZERO_ONE"). All logic must be contained in a single unified <script> tag at the footer of the
  document.
