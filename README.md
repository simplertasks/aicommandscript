![AICommandScript Logo](images/bee-64.png)

# AICommandScript (AICS)

*A lightweight, natural-language framework for creating structured, shareable AI applications.*

---

AICommandScript makes AI app creation accessible to everyone — as easy as writing a note, as powerful as writing an app. 
## Why AICS?

> **AICS is the only framework where writing an app feels like writing a note.**  
> **You can run an AICS app by pasting text — no setup, no installs.**

With AICS, apps are just plain-text notes with lightweight structure.  
They’re easy to create, easy to share, and run instantly inside an AI environment — no coding, no installation, no special tools required.

---

## The Vision

A future where building an “application” is as easy as writing a structured note.

AICommandScript solves the **Goldilocks Problem** in AI development:

- **Too little structure** → Inconsistent, unreliable, hard to maintain  
- **Too much structure** → Intimidating, requires technical knowledge, loses accessibility  
- **AICS** → Just right  

This balance bridges the gap between *citizen developers* and professional developers, enabling both to work with the same approachable toolchain.

---

## What is AICommandScript?

AICommandScript (AICS) is a framework for creating AI applications using natural language instructions instead of programming code. It’s designed to be **accessible to non-programmers** while offering enough structure and power for repeatable, reliable AI workflows.

At its core is the **Command Script**:  
a lightweight, natural-language framework that adds just enough discipline to AI interactions through:

- **Reusable templates**  
- **Explicit structure**  
- **Data integration**  
- **Flow control**

Unlike freeform prompting, AICS ensures your AI interactions are not just powerful, but **predictable, shareable, and consistent**.  

---

## How It Works

Instead of writing code, you define:

- **Behaviors** → session flow and user interactions  
- **Templates** → reusable message formats with placeholders like `[[emoji]]`, `[[user_fruit]]`  
- **Data structures** → facts and content your app will use  
- **AI instructions** → rules that guide how the AI responds  

The AI reads these instructions and executes your application exactly as described.

---

## Key Features

- **Plain Text & Natural Language** → Write apps like you’re writing notes  
- **Zero Setup** → Paste and run immediately, no installs required  
- **Shareable** → AICS files can be sent, copied, or versioned anywhere  
- **Structured** → Clear organization with sections for behaviors, templates, and data  
- **Multi-language Support** → Switch outputs seamlessly into multiple languages  
- **Template System** → Enforce consistent, repeatable outputs  
- **Data Verification** → Distinguish between AI-generated and human-verified facts  
- **Reliable & Repeatable** → Eliminate AI “drift” with explicit control  
- **Accessible** → Designed for teachers, creators, and professionals alike  

---

## Example Structure

```yaml
// AICommandScript APP
title: Fruit Quiz
author: Your Name
version: 1.0
type: Quiz App

// BEHAVIORS
- On session start: prompt with [language_selection]
- After language selection: display [welcome_message]

// TEMPLATES
template: welcome_message
Welcome to [title]!

// DATA
fruits:
- apple: 🍎
- banana: 🍌
```

⸻

Getting Started
	1.	Browse examples in the examples/ folder
	2.	Start with the AICS-master-template.md file
	3.	Customize behaviors, templates, and data
	4.	Share your AICS file — anyone can run it instantly

⸻

Examples
	•	Fruit Quiz → a multi-language quiz app showcasing AICS basics
	•	Master Template → a comprehensive demo of all features

⸻

Documentation

See docs/AICommandScript.md for detailed specifications.

⸻

License

This project is licensed under the MIT License — see the LICENSE file for details.

⸻

Contributing

Contributions are welcome! Please open issues, suggest features, or submit pull requests.

⸻

Contact

	•	Project: AICommandScript (AICS)
	•	GitHub: aicommandscript



---

