![AICommandScript Logo](images/bee-64.png)

# AICommandScript (AICS)

A lightweight, natural-language framework for creating structured, shareable AI applications.

## The Vision

AICommandScript addresses **The Goldilocks Problem** in AI development:

- **Too little structure** → Inconsistent, unreliable, hard to maintain
- **Too much structure** → Intimidating, requires technical knowledge, loses accessibility
- **AICS** → Just right

This could be the key to finally bridging the gap between "citizen developers" and professional developers using the same toolchain.

## What is AICommandScript?

AICommandScript (AICS) is a framework that allows you to create AI applications using natural language instructions instead of traditional programming code. It's designed to be accessible to non-programmers while providing powerful AI app creation capabilities.

At its core is **Command Script** — a lightweight, natural-language framework that gives users precise control over AI. Unlike freeform prompting, Command Script introduces explicit structure, reusable templates, dataset integration, and flow control — transforming raw instructions into reliable, repeatable applications. It preserves the simplicity of natural language while adding the discipline of programming, so creators can design AI interactions that are not just powerful, but also predictable and shareable.

## How It Works

Instead of writing code, you define:

- **Behaviors** - What should happen when (session flow, user interactions)
- **Templates** - How messages should look with placeholders like `[emoji]`, `[user_fruit]`
- **Data structures** - Facts, information, and content your app will use
- **AI instructions** - How the AI should respond and behave

The AI reads these natural language instructions and executes your application accordingly.

## Key Features

- **Natural Language**: Write apps in plain English (or other languages)
- **Shareable**: AICS files can be shared and reused across different AI platforms
- **Structured**: Clear organization with sections for behaviors, templates, and data
- **Multi-language Support**: Built-in support for multiple languages
- **Template System**: Reusable message formats with dynamic content
- **Data Verification**: Distinguish between human-verified facts and AI-generated content
- **Reliable & Repeatable**: Transform raw instructions into consistent applications
- **Accessible**: Designed for both citizen developers and professionals

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

## Getting Started

1. Check out the examples in the `examples/` folder
2. Use the `AICS-master-template.md` as a starting point
3. Customize behaviors, templates, and data for your app
4. Share your AICS file with others

## Examples

- **Fruit Quiz**: A multi-language quiz app demonstrating core AICS concepts
- **Master Template**: A comprehensive template showing all available features

## Documentation

See `docs/AICommandScript.md` for detailed documentation and specifications.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Feel free to submit issues, feature requests, or pull requests.

## Contact

- **From**: rob-mccormack@gmail.com
- **Project**: AICommandScript (AICS)
- **GitHub**: [aicommandscript](https://github.com/simplertasks/aicommandscript)

---

_AICommandScript makes AI app creation accessible to everyone through natural language instructions._
