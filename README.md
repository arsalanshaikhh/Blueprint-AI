# Design OS

> **AI-powered product planning and design tool for building better products faster.**

Design OS helps you define your product vision, structure your data model, design your UI, and prepare export packages for implementation. Rather than jumping straight into code, you work through a guided process that captures what you're building and why—then hands off everything your development team needs to build it right.

---

## 🎯 The Problem

AI coding tools are incredible at building fast. But the results often miss the mark. You describe what you want, the agent builds *something*, but it's not what you envisioned. The UI looks generic. Features get half-implemented. You spend as much time fixing and redirecting as you would have spent building.

**The core issue:** we're asking coding agents to figure out what to build *and* build it simultaneously. Design decisions get made on the fly, buried in code, impossible to adjust without starting over. There's no spec. No shared understanding. No source of truth for what "done" looks like.

---

## ✨ The Solution

Design OS provides a structured planning and design workflow:

1. **Product Planning** — Define your vision, break down your roadmap, and model your data
2. **Design System** — AI suggests colors, typography, and generates your application shell
3. **Section Design** — For each feature area: specify requirements, create sample data, and design screens
4. **Export** — Generate a complete handoff package ready for implementation

Each step is enhanced by AI. The AI generates suggestions based on your product context, you review and refine, and together you shape a product that matches your vision—before any implementation begins.

---

## 🚀 Features

### 🤖 AI-Powered Generation
- **Smart Data Models** — AI generates entities and relationships from your product overview
- **Design Token Suggestions** — AI recommends colors and fonts that match your product personality
- **Shell Generation** — AI creates navigation structure based on your roadmap sections
- **Context-Aware** — Uses your product overview and roadmap for all suggestions
- **Multiple AI Models** — Choose from various OpenRouter models (Gemini, Claude, GPT-4o, etc.)
- **Always Optional** — Works perfectly without AI too

### 💾 Persistent Workspace
- **Auto-Save** — Files automatically save to your project directory
- **Persistent Folder** — Selected folder remembered across browser sessions
- **Smart Paths** — Files go exactly where they belong
- **Folder Creation** — Automatically creates necessary directories
- **File System API** — Direct file access in Chrome/Edge (downloads in other browsers)

### 🎨 Design System
- **Tailwind Colors** — Choose from the full Tailwind palette
- **Google Fonts** — Select from curated heading, body, and mono fonts
- **Dark Mode** — All designs support light and dark modes
- **Responsive** — Mobile-first designs with Tailwind breakpoints

### 📦 Export & Handoff
- **Complete Package** — All components, types, and documentation
- **Ready-to-Use Prompts** — Pre-written prompts for coding agents
- **Implementation Guides** — Step-by-step instructions for each milestone
- **Test Specifications** — TDD-ready test descriptions

---

## 📋 The Planning Flow

Design OS follows a structured planning sequence:

### 1. Product Overview
Define your product's core description, the problems it solves, and key features.

**Output:** `product/product-overview.md`

### 2. Product Roadmap
Break your product into 3-5 development sections. Each section represents a self-contained area that can be designed and built independently.

**Output:** `product/product-roadmap.md`

### 3. Data Model
Define the core entities and relationships in your product. This establishes the "nouns" of your system and ensures consistency across sections.

**Output:** `product/data-model/data-model.md`

### 4. Design Tokens
Choose your color palette (from Tailwind) and typography (from Google Fonts). These tokens are applied to all screen designs.

**Output:** `product/design-system/colors.json`, `product/design-system/typography.json`

### 5. Application Shell
Design the persistent navigation and layout that wraps all sections.

**Output:** `product/shell/spec.md`

### 6. For Each Section
- **Spec** — Define the specification
- **Data** — Create sample data and types
- **Screen Designs** — Create screen designs
- **Screenshots** — Capture screenshots

### 7. Export
Generate the complete export package with all components, types, and handoff documentation.

**Output:** `product-plan/` directory

---

## 🛠️ Tech Stack

- **React 19** — Modern React with TypeScript
- **Tailwind CSS v4** — Utility-first styling
- **shadcn/ui** — Beautiful, accessible components
- **Vite** — Fast development and building
- **OpenRouter** — Multi-model AI integration

---

## 🏁 Quick Start

### Prerequisites
- Node.js 18+
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/arsalanshaikhh/Blueprint-AI.git
cd Blueprint-AI

# Install dependencies
npm install

# Run development server
npm run dev
```

### Configure AI (Optional)
1. Click the **Settings** icon (⚙️) in the app header
2. Add your OpenRouter API key ([get one here](https://openrouter.ai/keys))
3. Choose your preferred AI model
4. Save settings

### Start Planning
1. Click **"Choose Project Folder"** to select your project directory
2. Define your **Product Overview**
3. Create your **Product Roadmap**
4. Let AI help generate the rest!

---

## 📁 Project Structure

```
product/                           # Product definition (portable)
├── product-overview.md            # Product description, problems/solutions, features
├── product-roadmap.md             # List of sections with titles and descriptions
├── data-model/
│   └── data-model.md              # Entity descriptions and relationships
├── design-system/
│   ├── colors.json                # { primary, secondary, neutral }
│   └── typography.json            # { heading, body, mono }
├── shell/
│   └── spec.md                    # Shell specification
└── sections/
    └── [section-name]/
        ├── spec.md                # Section specification
        ├── data.json              # Sample data for screen designs
        ├── types.ts               # TypeScript interfaces
        └── *.png                  # Screenshots

src/                               # Design OS application
├── components/                    # React components
├── lib/                          # Services and utilities
├── sections/                     # Section design components
└── types/                        # TypeScript types

product-plan/                      # Export package (generated)
├── README.md                      # Quick start guide
├── prompts/                       # Ready-to-use prompts
├── instructions/                  # Implementation guides
├── design-system/                 # Tokens, colors, fonts
├── data-model/                    # Types and sample data
├── shell/                         # Shell components
└── sections/                      # Section components
```

---

## 🎨 Design System

Design OS uses a "Refined Utility" aesthetic:

- **Typography:** DM Sans for headings and body, IBM Plex Mono for code
- **Colors:** Stone palette for neutrals (warm grays), orange-pink gradient (#FD2D00 to #DF007C) for accents
- **Layout:** Maximum 800px content width, generous whitespace
- **Cards:** Minimal borders (1px), subtle shadows, generous padding
- **Motion:** Subtle fade-ins (200ms), no bouncy animations

---

## 🤝 How It Works

### For Product Managers & Designers
1. Work through the guided planning process
2. Define what you're building and why
3. Review AI-generated suggestions
4. Export a complete specification package

### For Developers
1. Receive structured product documentation
2. Use the export package with your coding agent
3. Follow implementation guides
4. Build with confidence knowing the spec is clear

---

## 📝 Documentation

- [Getting Started](docs/getting-started.md) — First steps with Design OS
- [Product Planning](docs/product-planning.md) — Guide to the planning process
- [AI Integration](docs/ai-integration.md) — How AI enhances the workflow
- [Export](docs/export.md) — Understanding the export package

---

## 🔄 Changelog

See [CHANGELOG.md](CHANGELOG.md) for version history and updates.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🤖 Built with AI

Design OS was built using AI-assisted development, demonstrating the power of human-AI collaboration in software creation.
