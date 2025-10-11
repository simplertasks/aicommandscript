AI.Web.Script - Natural structural language instructions for AI to interpret. 


________________
AI INSTRUCTIONS

The AI will read this entire script and execute the flow. 

Note: 

- AI must output ONLY the exact content specified in templates and data, with no additional text, explanations, or deviations.

- never display variable names to the user

_________
META DATA

title: Cities Quiz
author: J. Smith
description: A simple quiz testing the knowledge of cities. 

______________________
AI GENERATED VARIABLES

ai-selected-city: AI randomly select one city from {cities}

ai-evaluation:  Evaluate answer based on accuracy and completeness

ai-grade: AI to assign a grade (A, B, C, D, or F) 

ai-funfact: Share a fun fact about the {ai-selected-city} 

ai-cities-list: Display in a numbered list of countries and append a flag for that country

_________
APP FLOW

{start.template}

user-response: Ask user to provide three facts about the {ai-selected-city}

{reply.template}

{funfact.template}

Then ask the user if they want to answer another question or if they want to quit.

If they want to quit display:
{goodbye.template}

__________
TEMPLATES

template: footer.template
{title} QUIZ - **Q** to quit


template: start.template  

# Welcome to {title} by {author}.
![Bee](https://www.birdlife.org/wp-content/uploads/2021/06/Hummingbird-Norbert-Hentges-Unsplash-edited-scaled.jpg)

{footer.template}


template: reply.template
You were asked about: {ai-selected-city} and you replied:

_{user-response}_

{ai-evaluation}

Grade: **{ai-grade}**


template: funfact.template

## Fun Fact
_{ai-funfact}_
{footer.template}

template: goodbye.template
## Thanks for playing {title}.

by the way the other cities were:

{ai-cities-list}

> Goodbye

____
DATA

cities:
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