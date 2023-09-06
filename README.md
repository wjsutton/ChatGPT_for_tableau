# ChatGPT Prompting Frameworks for Tableau 📈
A prompting framework to focus ChatGPT on creating data analysis, data storytelling and data visualisation. 
<br>

### :a: About

The aim of this ChatGPT GPT-4 prompting framework is to:
- improve accuracy and focus of data analysis
- increase the types and quality of visualisations chatGPT recommends
- help tell stories with data that are of interest to an audience 

It was built and tested using ChatGPT GPT-4 Code Interpreter (Advanced Data Analysis)

### ⚠️ Health Warning ⚠️

This prompting format is designed to improve the output received from ChatGPT, this is not guaranteed depending on your scenerio. 

Please only attempt to perform data tasks if you are an experienced data analyst and can verify ChatGPT has been thorough enough to produce accurate work. 

### 🔌 Quick Start

Here is the pretraining prompts I used to enter a visualisation for Visual Capitalist

- [Visual Capitalist Full Pre-Training](visual_capitalist_pretraining.md)

### 🔨 A Customisable Version

Here is my generic prompt build

- Generic Prompt Pre-Training = [Visual Vocabulary.md](visual_vocabulary.md) + [CRAFT (will require input)](craft_generic_data_visualisation_task.md)

Details of these sections and how you can customise them are detailed below.

### 🔑 Key Sections 

1. **The Visual Vocabulary** - this focuses ChatGPT to expand the range of charts and why it would use them
2. **CRAFT** - this is prompting framework for Context, Role, Action, Format, Target
3. **Referencing back** - for a specific problems referencing back to The Visual Vocabulary and CRAFT sections

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

#### Context - What is your goal?

e.g. I am a Tableau data visualisation developer and looking to submit a data visualisation for Visual Capitalist. I want to visualise the topic of Economy,

#### Role - What role do you want chatGPT to take?

e.g. Your role is that of an experienced data visualisation designer, able to craft impressive graphics and tell intriguing data stories.

#### Action- What do you want chatGPT to do? 

e.g. I will need to analyse datasets, with an emphasis on the Visual Vocabulary. I will need to craft a story from the data, ideally, we should be able to say three things about our visualisation at different granularities, i.e. an overall trend, a breakdown by countries in that trend, and the countries changing rank amongst that trend 

#### Format - How do you want to receive the data back? 

e.g. Please provide this information in simple text, lists and code where necessary. 

#### Target - Who is the target audience, what skill level are they? 

e.g. These data visualisations are for well-informed financial experts, personal investors and career climbers.  


### 3. Referencing Back 

Aftering listing the Visual Vocabulary and CRAFT sections, you can now start asking chatGPT to carry out data analysis. 

When prompting it's good practice to reference back to previous sections so chatGPT knows what you're looking for.

Here are some examples from my Visual Capitalist Project.

**Starting with a Dataset**
```
DATA

Please find the Data Attached
- this data relates to the percentage of 15% that have a financial account, i.e. own a bank account
- this data is split by country, gender, year, and value indicates the percent of financial accounts
- some of the data is missing in the column value please exclude this

Referring back to the ACTION and CONTEXT sections earlier please could you find 5 areas of data analysis, that would be of interest to our TARGET please?

---

STORY

From this analysis we need find three key stories as mentioned in the ACTION and CONTEXT sections, please could you find 3 stories in the data from the analysis carried out that would be of interest to the TARGET?

---

VISUAL 

For each story please could you give three charts from the VISUAL VOCABULARY and the data analysis they should show and why
```

**Starting with a Story**
```
STORY

I'm looking to for a interesting story for my TARGET on the topic of money. From what data you have available please could you provide 5 stories on topic and areas I can find data related to the story please?

---

DATA

Please find the Data Attached
- this data relates to the story the Shift to a Cashless Society, and is data from World Bank's Global Findex Database
- on the Data tab, this data is split by country, year, population, and gives several metrics on digital payments and financial inclusion

Referring back to the ACTION and CONTEXT sections earlier please could you find 5 areas of data analysis, that would be of interest to our TARGET please?

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

This is a list visualisations that you've typically been suggested based on the VISUAL VOCABULARY for the TARGET, can you give me 5 visualisations that are not in this list and are a bit less seen in the world of dataviz:
- Slope Chart
- Line Chart
- Bar-Ordered Chart
- Column-Ordered Chart
- Area Chart
- Pie Chart
etc.

---

DATA

For these charts please could you find an approriate data source that would be of interest to our TARGET, given the CONTEXT. 

upload dataset
Referring back to the ACTION and CONTEXT sections earlier please could you find 5 areas of data analysis, that would be of interest to our TARGET please?

---
STORY

From this analysis we need find three key stories as mentioned in the ACTION and CONTEXT sections, please could you find 3 stories in the data from the analysis carried out that would be of interest to the TARGET?


```

