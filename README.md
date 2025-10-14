![AICommandScript Logo](images/bee-64.png)

# AICS (AI Command Script)

**Natural language instructions for building AI apps without coding.**

## Overview

AICS is a declarative scripting language that enables non-programmers to create interactive AI-powered applications. Simply write human-readable instructions, define templates, and let AI handle the execution.

## Key Features

- 📝 **No coding required** - Uses natural language and intuitive syntax
- 🎯 **Template-based** - Define output formats with simple placeholders
- 🔄 **Flow control** - Step-by-step logic that AI follows automatically
- 🤖 **AI-powered** - Leverage AI for randomization, evaluation, fact-checking, and more
- 📊 **Data-driven** - Simple lists and structures anyone can understand

## Quick Start

Here’s a minimal AICS script:

```md
== APP ==

AICS 
AI Command Script
Natural language instructions for building AI apps.


== SETUP ==
App Name: Hello World
Author: Your Name
Description: A simple greeting app

== AI INSTRUCTIONS ==

AI MUST immediately execute this script upon reading it.
AI MUST output ONLY the exact content specified in templates.
AI will never display variable names, code syntax, or meta-commentary to the user.



== FLOW ==
1. Show [[greeting]].
2. Ask user for their first name and store as [[user_name]].
3. Show [[response]].


== TEMPLATES ==
greeting:
  Welcome! What's your name?

response:
  Hello, [[user_name]]! Nice to meet you.

Your name means:


== TEMPLATES ==
greeting:
  Welcome! What's your first name?

response:
  Hello, [[user_name]]! Nice to meet you.


Your name means:
[name-meaning]

== AI GENERATED TEXT ==

- user_name: The user's provided names
- name-meaning: AI to provide the meaning of the name or the history of the name provided. 
```

## Structure

Every AICS script consists of four main sections:

### 1. APP

Identifies the script as AICS format.

### 2. SETUP

Basic metadata about your application:

- **App Name**: Display name
- **Author**: Creator’s name
- **Description**: What the app does
- **Tone**: How AI should communicate (friendly, professional, educational, etc.)

### 3. FLOW

Sequential steps the AI executes:

- Use numbered steps
- Reference templates with `[[template_name]]`
- Store user input or AI-generated content as variables with `[[variable_name]]`
- Include conditional logic (if/then)

### 4. TEMPLATES

Output formats with placeholder variables:

```
template_name:
  Your content here with [[variables]]
  Can include markdown formatting
  Images, emojis, and styling
```

### 5. AI GENERATED TEXT

Definitions for dynamic content:

```
- variable_name: Description of what AI should generate
```

### 6. DATA (Optional)

Static content like lists, options, or reference material:

```
cities:
- London
- Paris
- Tokyo
```

## Example: Cities Quiz

See the complete example in [`examples/cities-quiz.aics`](examples/cities-quiz.aics)

This quiz app demonstrates:

- Random selection from data lists
- User input collection and storage
- AI evaluation and grading
- Dynamic fact generation
- Conditional flow (continue/quit)
- Template reuse and variable substitution

## Variable Syntax

Variables use double square brackets:

- `[[variable_name]]` - Inserts the variable’s value
- Variables can store:
  - User input
  - AI-generated content
  - Selected data from lists
  - Evaluation results

## AI Instructions

Special instructions can be added to control AI behavior:

```
== AI INSTRUCTIONS ==
AI MUST immediately execute this script upon reading it.
AI MUST output ONLY the exact content specified in templates.
AI will never display variable names, code syntax, or meta-commentary.
```

## Use Cases

- 📚 **Educational quizzes** - Test knowledge on any topic
- 🎮 **Interactive games** - Text adventures, trivia, puzzles
- 💬 **Chatbots** - Customer service, FAQs, guided assistance
- 📋 **Surveys & forms** - Collect and evaluate responses
- 🎓 **Tutoring apps** - Personalized learning experiences
- 🔍 **Decision trees** - Guided troubleshooting or recommendations

## Best Practices

1. **Keep flows simple** - Break complex apps into clear steps
1. **Use descriptive variable names** - `[[user_age]]` not `[[x]]`
1. **Test incrementally** - Start with basic flow, add features gradually
1. **Document AI generation** - Clearly explain what AI should create
1. **Provide data** - Give AI reference material when needed

## Limitations

- Currently interpreted by AI (Claude, ChatGPT, etc.)
- No persistent storage between sessions
- Limited to AI’s capabilities and knowledge
- Best for conversational/educational apps

## Contributing

AICS is an experimental format. Contributions welcome:

- Example scripts
- Use case documentation
- Syntax improvements
- Interpreter implementations

## License

MIT License - Feel free to use and modify

## Credits

Created by J. Smith (example author)

-----

**Ready to build your first AI app? Start with the Quick Start example above!**