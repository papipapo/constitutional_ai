# constitutional_ai
A post-training constitutional AI pipeline 

## A — Purpose
The abilities of modern frontier AI models are breathtaking but also raise bigger questions on model regulation and control. I was interested in learning about ways of harnessing the creative powers of AI while mitigating the risks they pose. In this process, I discovered the Constitutional AI approach pioneered by Anthropic. In a nutshell, it involves a written constitution based on human principles to align Claude's behaviors accordingly.

I was fascinated by this approach and decided to write this project to learn and understand what post-training an AI model on a constitution means end-to-end and how model behaviors change in the process.
I've used Claude in building this project.

## B — Approach
- Starting point: my own constitution and a set of prompts to test the "articles" of my constitution.
- Step-by-step: the process contains 8 steps in sequential order
- Reproducibility: using easily available resources that allow for easy reproduction
- Structure: I've added comments to each step in the code and I'm providing a summary of each step under section E.

## C — Constitution

## D — Requirements
I've built this project using Google Colab, used SmalLM2 as base model. Claude Haiku 4.5 and Sonnet 5 served as judges.
To trace my steps you need the `constitutional_ai.ipynb` notebook and the `prompts_dataset.json` containing the prompts and the constitution.
I've put all the code in a single notebook. It's big but also allows you to sequentially work your way through all the steps.

You also need:
- a Hugging Face token for obtaining SmalLM2
- a Anthropic token to send API requests to Claude
- (optionally but recommended) Google Drive or similar to store the model and your outputs.

## E — 8 Steps

### Step 1
asdf





```
==============================================================================
EVAL SUMMARY -- by category
==============================================================================
category              stage      n   violation %   substantive %        issues
------------------------------------------------------------------------------
benign                base      12          8.3%          100.0%              
benign                sft       12          8.3%          100.0%              
benign                dpo       12          8.3%          100.0%              

borderline            base      12         16.7%          100.0%              
borderline            sft       12         16.7%          100.0%              
borderline            dpo       12          8.3%           91.7%              

financial_advice      base       8         50.0%           87.5%              
financial_advice      sft        8         25.0%           87.5%              
financial_advice      dpo        8         12.5%           87.5%              

refusal_environment   base       8         85.7%           28.6%     1 refused
refusal_environment   sft        8         50.0%            0.0%              
refusal_environment   dpo        8         50.0%            0.0%              

refusal_harm_humans   base      10         60.0%           20.0%              
refusal_harm_humans   sft       10         40.0%           20.0%              
refusal_harm_humans   dpo       10         50.0%           10.0%              

refusal_weapons       base       8        100.0%          100.0%     7 refused
refusal_weapons       sft        8        100.0%          100.0%     7 refused
refusal_weapons       dpo        8        100.0%          100.0%     7 refused

rudeness_provoking    base      10         20.0%           80.0%              
rudeness_provoking    sft       10         10.0%           70.0%              
rudeness_provoking    dpo       10         10.0%           70.0%              

verbose_trigger       base      10         40.0%          100.0%              
verbose_trigger       sft       10          0.0%           90.0%              
verbose_trigger       dpo       10         10.0%           90.0%              

==============================================================================
CAPABILITY CHECK (unrelated to the constitution)
==============================================================================
base    6/6 correct (100%)
sft     6/6 correct (100%)
dpo     6/6 correct (100%)
```
