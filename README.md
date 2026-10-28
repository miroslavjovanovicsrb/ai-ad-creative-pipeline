# AI Ad Creative Pipeline

AI-powered pipeline that automates the creation and optimization of ad creatives:
headlines are optimized via the **OpenAI API (GPT-4o)** into two psychological variants
(emotional & benefit-driven), image ideas are technically refined for image AIs
(DALL-E / Midjourney), and everything is combined into a structured test matrix.

## The Problem

Creating ad variations for A/B testing is manual, slow and unstructured. This pipeline
turns a raw list of headlines and image ideas into a complete, ready-to-test creative
matrix — in minutes instead of hours.

## How It Works

1. **Data setup** — base list of headlines (focus: solar & finance topics) with
   corresponding image prompts
2. **AI optimization (OpenAI API, GPT-4o)** —
   - Headlines automatically rewritten into two psychological variants:
     *emotional* and *benefit-driven*
   - Image ideas technically refined into precise prompts for image AIs
     (DALL-E / Midjourney)
3. **Matrix generation** — cross-join of every headline variant with every optimized
   image prompt → structured, complete test basis
4. **Possible extensions** —
   - Direct sync to Airtable API (no manual CSV import)
   - DALL-E 3 integration to generate visuals inside the workflow
   - Approval step (e.g. via Slack) before creatives go live in the ad manager

## Tech Stack

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)
![OpenAI](https://img.shields.io/badge/-OpenAI%20API%20(GPT--4o)-412991?style=flat-square&logo=openai&logoColor=white)
![Pandas](https://img.shields.io/badge/-pandas-150458?style=flat-square&logo=pandas&logoColor=white)

## Example

| Original Headline | Variant: Emotional | Variant: Benefit |
|---|---|---|
| *„Cut your energy bill"* | *„Stop watching your hard-earned money disappear into the grid"* | *„Save up to 40% on your monthly energy bill"* |

*(→ combined with optimized image prompts into a full test matrix)*

## Getting Started

```bash
git clone https://github.com/miroslavjovanovicsrb/ai-ad-creative-pipeline.git
cd ai-ad-creative-pipeline
pip install -r requirements.txt
jupyter notebook
```

> Note: An `OPENAI_API_KEY` environment variable is required to run the optimization step.

## Project Structure

```
ai-ad-creative-pipeline/
├── notebooks/            # pipeline notebooks
├── data/                 # input headlines & image prompts
├── output/               # generated matrices
├── requirements.txt
└── README.md
```

## Author

**Miroslav Jovanovic** — Python Backend & AI Engineer
[LinkedIn](https://www.linkedin.com/in/miroslav-jovanovic-python) ·
[GitHub](https://github.com/miroslavjovanovicsrb)
