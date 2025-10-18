## Build an AI App with 20 lines of Markdown

TODO
Link to live example and screenshots and better image for inclusion


Paste a special flavor of  Markdown text into ChatGPT. Get a working AI app back.

**AICS (AI Command Script)** is an open-source, MIT-licensed format that lets you describe AI apps using simple, human-readable blocks. Think of it as *Markdown for AI apps* — you define setup, flow, format, logic, and templates, and the AI executes it directly.

**See you in action:**
url here

sCREENSHOT


Here’s the entire “Hello World” app:

```md
== APP ==
AICS 
AI Command Script
Natural language structured instructions for building AI apps.

== SETUP ==
App-Name: Hello World
Author: Bill Smith
Description: A simple greeting app
compatibility: ChatGPT 4, 5

== AI INSTRUCTIONS ==
AI MUST immediately execute this script upon reading it.
AI MUST output ONLY the exact content specified in templates.
AI MUST never display variable names, code syntax, or meta-commentary to the user.

== FLOW ==
1. Show [[greeting]].
2. Ask user for their first name and store as [[user_name]].
3. Show [[response]].
4. When the session is over display the top five baby names in the US in tabular format. 

== TEMPLATES ==
greeting:
![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/86/Wikipedia_Hello_World_Graphic.svg/330px-Wikipedia_Hello_World_Graphic.svg.png)

  ## Welcome to [[App-Name]] ! 
	
	> by: [[name]]
	
	What's your **first name**?
	

response:
  Hello, [[user_name]]! Nice to meet you.

Your name means:
[name-meaning]

would you like to learn the meaning of another first name?  (Y/N) 


== AI GENERATED TEXT ==
- name-meaning: AI to provide the meaning or history of the name.

```

That’s it — a complete working AI interaction, readable as plain text.

no doubt you will notice the use of the double square brackets. [[…]]. These can hold values for variables, the contents of templates or the users response  



If you want to learn more or 

https://www.markdownguide.org/getting-started/


you can use GitHub repositories or Github 
 to write and preview your AICS


⸻

## How to Run It

You don’t need to install anything or set up a runtime.
Just paste the script directly into ChatGPT (or any large language model) — that’s it.

The AI reads the script, follows the flow, and uses your templates automatically.
AICS is designed so the AI itself acts as the interpreter — no extra tools required.

⸻

One way to think about AICS is as a super-prompt — it lets you go beyond a single instruction to include structure, basic logic, and even images. You can define how input and output should look, guide the AI’s flow, and embed dynamic text — all in one lightweight file.

One of the best things about AICS is that it’s highly portable. Because it’s just text, you can share your AI apps by email, post them online, or even send them by SMS. No code, no dependencies — just pure, readable intent.

AICS is based on Markdown, the lightweight formatting used in READMEs and docs, so it’s instantly familiar. The goal is to make AI orchestration human-friendly — to let anyone describe structure, behavior, and purpose in plain language.

## Why AICS vs. Just Writing a Good Prompt?

If you’re already comfortable prompting AI, you might wonder: why use AICS at all?

**Plain prompts become unreadable fast.** Try cramming multi-step logic, output formatting, and examples into one block of text — it gets messy, hard to follow, and nearly impossible to maintain or share.

**AICS gives you structure.** Separate sections for flow, templates, and data make complex interactions clear and organized. Six months later, you’ll actually understand what you built.

**Templates solve the consistency problem.** Getting an AI to format output the same way twice with a plain prompt? Nearly impossible. AICS templates give you reliable, repeatable formatting that just works.

**Total control over input and output.** You define exactly how the AI should ask for information and exactly how it should respond. No more “the AI decided to add extra commentary” or “it reformatted everything differently this time.”

⸻

**Think of it this way:** A prompt is a conversation. AICS is a blueprint. Both work for simple tasks, but only one scales.​​​​​​​​​​​​​​​​

⸻

## Tips for Creating Your Own AICS

1. **Test thoroughly.** A single success doesn’t guarantee consistency across runs or models. AI compliance with directives isn’t guaranteed — always test your scripts with your target model to ensure reliability.
1. **Keep instructions short and accurate.** Prefer clear, minimal directives over long explanations.
1. **If it’s not behaving, ask an LLM for help.** Have a model suggest better wording, structure, or templates.
1. even non-programmers could easily learn how to create AICS And host them on the Internet using GitHub Gists which also that you to preview the markdown so you can see how it looks
1. aics could be written in a Google document which offers revision history and they are easily shared
1. it's probably best to use the file extension.md 
Although.yaml can give you some nice highlighting




⸻

## Going Further

Don’t be fooled by the apparent simplicity of AICS.

You can easily build data-driven mini apps by adding a data section:

```md
== DATA ==
cities:
- Toronto
- Washington
- London
```

The DATA section can include lists, JSON, or even API calls for external data your app can use.

You can achieve basic logic just by using natural language — simple “if… then…” statements work surprisingly well.

Multi-language apps are also possible: just ask the user which language they want to use at the start, and instruct the AI to respond accordingly.

if you need some programming like functions you can simply ask for things like, a random city from [[cities]]. 

AICS isn’t meant to replace complex frameworks or heavy APIs, but considering its development speed, extendability, low friction, and human readability, it’s absolutely worth a look.

## Future LLM Native Support

Right now, each AICS script includes its own format documentation so any LLM can interpret it immediately. As AICS gains adoption, LLM providers could easily add native support — it’s a simple decision since AICS is just structured Markdown. Built-in support would make AICS far more dependable and consistent across runs. 

## Conclusion

AI apps shouldn't require complex frameworks or deployment pipelines. AICS brings them back to basics: readable text that anyone can write, share, and run.

Start building today. Copy, paste, experiment.

AICS is open source (MIT):
→ **[View on GitHub](repo-ur

⸻
Authors note:
LLMs significantly contributed to the development of AICS and to this article. 




 