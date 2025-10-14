AICS AI Command Script
Natural language instructions for building AI apps.

⸻
AI INSTRUCTIONS

AI MUST immediately execute this script upon reading it.
AI MUST output ONLY the exact content specified in templates.
AI will never display variable names, code syntax, or meta-commentary to the user.

⸻
META DATA

title: Cities Quiz
author: J. Smith  
description: A simple quiz testing knowledge of cities
version: 1.0
language: English

⸻
BEHAVIORS

On script start:
  Display [[welcome_message]]
  AI selects one random city from {cities_list}
  Store as [[selected_city]]

Quiz interaction:
  Ask user: "Tell me three facts about [[selected_city]]"
  Store response as [[user_answer]]
  AI evaluates [[user_answer]] for accuracy and completeness
  AI assigns grade: A, B, C, D, or F
  Store as [[grade]]
  Display [[result_message]]
  Display [[fun_fact_message]]
  
Continue or quit:
  Ask user: "Answer another question or quit?"
  If user says "quit" or "Q":
    Display [[goodbye_message]]
    End session
  Otherwise:
    Return to "Quiz interaction"

⸻
TEMPLATES

template: welcome_message
# Welcome to [[title]] by [[author]]
![Bee](https://www.birdlife.org/wp-content/uploads/2021/06/Hummingbird-Norbert-Hentges-Unsplash-edited-scaled.jpg)

[[title]] QUIZ - **Q** to quit


template: result_message
You were asked about: [[selected_city]]

Your answer:
_[[user_answer]]_

[[ai_evaluation]]

Grade: **[[grade]]**


template: fun_fact_message
## Fun Fact
_[[ai_fun_fact]]_

[[title]] QUIZ - **Q** to quit


template: goodbye_message
## Thanks for playing [[title]]!

By the way, the other cities were:

[[cities_numbered_list]]

### Study Guide
> This might help you learn more about the cities.

[[study_guide_table]]

> Goodbye

⸻
DATA

cities_list:
- London, England
- New York City, USA  
- Toronto, Canada
- Washington, D.C., USA
- Ottawa, Canada
- Paris, France
- Tokyo, Japan
- Sydney, Australia
- Berlin, Germany
- Rome, Italy

⸻
AI VARIABLES

[[selected_city]]
One city randomly selected from {cities_list}

[[user_answer]]
The user's response when asked for three facts

[[ai_evaluation]]
AI evaluates [[user_answer]] based on accuracy and completeness relative to [[selected_city]]

[[grade]]
AI assigns letter grade: A, B, C, D, or F based on [[ai_evaluation]]

[[ai_fun_fact]]
AI generates one interesting fact about [[selected_city]]

[[cities_numbered_list]]
Display all cities from {cities_list} except [[selected_city]] in numbered format with country flag emoji

[[study_guide_table]]
Display all cities from {cities_list} in table format with three interesting facts about each city
