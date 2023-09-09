# ChatGPT Prompting Frameworks for Tableau 📈
A prompting framework to focus ChatGPT on creating data analysis, data storytelling and data visualisation.
<be>

## Table of contents

<!--ts-->
   * [About](#a-about)
   * [Health Warning](#warning-health-warning-warning)
   * [Quick Start Guide](#electric_plug-quick-start-guide)
   * [A Customisable Version](#hammer-a-customisable-version)
      * [1. The Visual Vocabulary](#1-the-visual-vocabulary)
      * [2. CRAFT](#2-craft)
      * [3. Referencing Back](#3-referencing-back)
   * [What's next](#whats-next)
<!--te-->

## :a: About

The aim of this ChatGPT GPT-4 prompting framework is to:

- Improve accuracy and focus of data analysis
- Increase the types and quality of visualisations chatGPT recommends
- Help tell stories with data that are of interest to an audience

It was built and tested using ChatGPT GPT-4 Code Interpreter (Advanced Data Analysis)

## :warning: Health Warning :warning:

This prompting format is designed to improve the output received from ChatGPT, this is not guaranteed depending on your scenario.

Please only attempt to perform data tasks if you are an experienced data analyst and can verify that ChatGPT has been thorough enough to produce accurate work.

## :electric_plug: Quick Start Guide

Here are the pretraining prompts I used to enter a visualisation for Visual Capitalist. 

To get started take this file and copy 'and paste it into ChatGPT before starting your project.

- [Visual Capitalist Full Pre-Training](visual_capitalist_pretraining.md)

## :hammer: A Customisable Version

Here is my generic prompt build.

- Generic Prompt Pre-Training = [Visual Vocabulary.md](visual_vocabulary.md) + [CRAFT (will require input)](craft_generic_data_visualisation_task.md)

Details of these sections and how you can customise them are detailed below.

1. **The Visual Vocabulary** - This focuses ChatGPT to expand the range of charts and why it would use them
2. **CRAFT** - This is a prompting framework for Context, Role, Action, Format, Target
3. **Referencing back** - For specific problems reference back to The Visual Vocabulary and CRAFT sections


### 1. The Visual Vocabulary

Access the text version here: [visual_vocabulary.md](visual_vocabulary.md)

The image version is available here: [Financial Times Visual Vocabulary](https://github.com/Financial-Times/chart-doctor/blob/main/visual-vocabulary/Visual-vocabulary-en.pdf)


Example of text
```
Deviation

- Note this is not standard deviation
- Emphasise variations (+/-) from a fixed reference point. Typically the reference point is zero but it can also be a target or a long-term average. Can also be used to show sentiment (positive/neutral/negative)
- Examples of use: Trade surplus/deficit, climate change

Deviation Chart Types:

- bar-diverging: A simple standard bar chart that can handle both negative and positive magnitude values
- bar-diverging-stacked: Perfect for presenting survey results which involve sentiment (eg disagree, neutral, agreed
- spine-chart: Splits a single value into 2 contrasting components (eg Male/Female)
- line-surplus-deficit-filled: The shaded area of these charts allows a balance to be shown; either against a baseline or between two series
...
```

### 2. CRAFT

In the generic example: [craft_generic_data_visualisation_task.md](craft_generic_data_visualisation_task.md)

You will have to insert information specific to your task, this includes:

- [DATAVIZ TOOL]
- [GOAL]
- [TOPIC]
- [PREVIOUS VIZ EXAMPLES]
- [VIZ FORMAT AND SIZE]
- [AUDIENCE NEEDS]

This is not an exhaustive list but good enough to get you started.

The CRAFT prompting method is from this YouTube video by Lawton Solutions:
- [Write the Best ChatGPT Prompts in Open AI GPT4 - Expert Guide - Use the CRAFT Prompt Method](https://youtu.be/Gidc185wnEA?si=xX0idLfbRwNVI_Wm)

#### Context - What is your goal?

e.g. I am a Tableau data visualisation developer and looking to submit a data visualisation for Visual Capitalist. I want to visualise the topic of the Economy

#### Role - What role do you want chatGPT to take?

e.g. Your role is that of an experienced data visualisation designer, able to craft impressive graphics and tell intriguing data stories.

#### Action- What do you want chatGPT to do? 

e.g. I will need to analyse datasets, with an emphasis on Visual Vocabulary. I will need to craft a story from the data, ideally, we should be able to say three things about our visualisation at different granularities, i.e. an overall trend, a breakdown by countries in that trend, and the countries changing rank amongst that trend

#### Format - How do you want to receive the data back? 

e.g. Please provide this information in simple text, lists and code where necessary.

#### Target - Who is the target audience, what skill level are they? 

e.g. These data visualisations are for well-informed financial experts, personal investors and career climbers.


### 3. Referencing Back 

After listing the Visual Vocabulary and CRAFT sections, you can now start asking chatGPT to carry out data analysis.

When prompting it's good practice to reference back to previous sections so chatGPT knows what you're looking for.

For example, "Referring back to the ACTION and CONTEXT sections earlier please could you find 5 areas of data analysis, that would be of interest to our TARGET, please?"

**Starting your analysis**

For projects I have tested:
- Starting with a Dataset
- Starting with a Story
- Starting with a Chart

In general I would recommend starting with a dataset where possible as you're less likely to introduce bias to your project. 

Here are some examples from my Visual Capitalist Project.

**Starting with a Dataset**
```
DATA

Please find the Data Attached
- This data relates to the percentage of 15% that have a financial account, i.e. own a bank account
- This data is split by country, gender, year, and value indicates the percentage of financial accounts
- Some of the data is missing in the column value please exclude this

Referring back to the ACTION and CONTEXT sections earlier please could you find 5 areas of data analysis, that would be of interest to our TARGET, please?

---

STORY

From this analysis we need to find three key stories as mentioned in the ACTION and CONTEXT sections, please could you find 3 stories in the data from the analysis carried out that would be of interest to the TARGET?

---

VISUAL 

For each story please could you give three charts from the VISUAL VOCABULARY and the data analysis they should show and why
```

**Starting with a Story**
```
STORY

I'm looking for an interesting story for my TARGET on the topic of money. From what data you have available please could you provide 5 stories on the topic and areas where I can find data related to the story, please?

---

DATA

Please find the Data Attached
- This data relates to the story The Shift to a Cashless Society and is data from the World Bank's Global Findex Database
- On the Data tab, this data is split by country, year, and population, and gives several metrics on digital payments and financial inclusion

Referring back to the ACTION and CONTEXT sections earlier please could you find 5 areas of data analysis, that would be of interest to our TARGET, please?

---

VISUAL 

For each piece of analysis:
- 1. The Decline of Manufacturing Jobs
- 2. Resilience of Service-Based Industries
- 3. Stability of Government Jobs vs. Volatility of Private Sector

Please could you give three charts from the VISUAL VOCABULARY and the data analysis they should show the TARGET and why

```

 **Starting with a Chart**
```
VISUAL

This is a list of visualisations that you've typically been suggested based on the VISUAL VOCABULARY for the TARGET, can you give me 5 visualisations that are not in this list and are a bit less seen in the world of dataviz:
- Slope Chart
- Line Chart
- Bar-Ordered Chart
- Column-Ordered Chart
- Area Chart
- Pie Chart
etc.

---

DATA

For these charts please could you find an appropriate data source that would be of interest to our TARGET, given the CONTEXT. 

upload dataset
Referring back to the ACTION and CONTEXT sections earlier please could you find 5 areas of data analysis, that would be of interest to our TARGET, please?

---
STORY

From this analysis we need to find three key stories as mentioned in the ACTION and CONTEXT sections, please could you find 3 stories in the data from the analysis carried out that would be of interest to the TARGET?

```

### What's next? 

Data visualization is more than just pretty charts; it's about telling a story that resonates. With the ChatGPT prompting framework, Tableau creators can elevate their data storytelling, making every visualization not just a chart, but a captivating narrative.


While this framework offers a solid foundation, it's designed for adaptability. Feel free to tweak, modify, and experiment to enhance its precision and align it with your unique requirements. I'd love to hear your thoughts and experiences with this framework. 

Connect and share your insights with me on Linkedin:
- [Will Sutton](https://www.linkedin.com/in/will-sutton-14711627/)

Last Updated: 2023-09-09
