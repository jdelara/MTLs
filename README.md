# Model Transformation Languages as Research Topic
This repository provides some data about model transformation languages (MTLs) as research topic in MDE.

## Trends in model transformation research
we downloaded all the papers published until 2025 in SoSyM and MoDELS (the two main scientific venues for MDE research) and extracted the following information: title, abstract, keywords, and submission date (or publication date if the submission date was not available). This totalled 2,384 papers (1,390 from SoSyM and 994 from MoDELS).

Then, to identify those papers related to model transformation, we fed the information to an LLM (Qwen3-30B) asking two questions: (1) whether the paper is about model transformation, and (2) whether the paper discusses an MTL or features of MTLs. We manually checked a small percentage of the papers, to ensure coherence of results.
The prompt used is:

```
 Context:
 In Model-Driven Engineering, a model transformation is the automated process of modifying a model in-place or 
 converting a model into another software artifact, such as code, or a different model. 
 A model transformation is typed against one or more meta-models.

 Task:
 You are given the title, abstract and keywords of a research paper about Model-Driven Engineering (MDE).
 Your task is to classify whether the paper is about a model transformations or not. 
 If the paper is about model transformations, also classify whether it introduces or discusses some
 transformation language or feature related to transformation languages. 
 Extract also the name of the transformation language if any.

 Information:
 - Title: {title}

 - Abstract: {abstract}

 - Keywords: {keywords}

 The answer MUST be in json. Mark it with &#96;&#96;&#96;json, using the following format:
 &#96;&#96;&#96;json
 {
     "is_transformation": "<whether the paper is about model transformations: true/false>",
     "is_transformation_language": "<whether the paper discusses a transformation language: true/false>",
     "language": "<if the paper discusses a transformation language, the name of the language (or languages separated by commas), otherwise 'None'>",
     "why": "<explain your classification>"
 }
 &#96;&#96;&#96;
```
The raw data is available at: [to-do]

The next graphic shows the percentage of papers about model transformations published in SoSyM and MODELS:
<img width="1000" height="600" alt="mt_papers" src="https://github.com/user-attachments/assets/8c4eb397-08b8-49a7-b8b9-65c3d346a580" />

The next graphic shows the percentage of papers about model transformation languages published in SoSyM and MODELS:
<img width="1000" height="600" alt="mtl_papers" src="https://github.com/user-attachments/assets/e0e1ae46-92c2-4ae8-b97c-644a9be9d535" />

## Tools
Many tools to support MTLs have been developed along the years. To have an up-to-date view of their current status that complements our study, we have examined which are actively maintained and evolved. The data is showsn in the image below, and the raw data is available at: [to-do].

<img width="843" height="487" alt="image" src="https://github.com/user-attachments/assets/04928a52-9400-414f-9734-46eabaa325b0" />



