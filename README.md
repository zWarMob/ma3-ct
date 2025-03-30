**AI & Machine Learning (KAN-CINTO4003U) - Copenhagen Business School | Spring 2025**

***

### Group members
| Student name | Student ID |
| --- | --- |
| #NAME# | #ID# |
| #NAME# | #ID# |
| #NAME# | #ID# |

***

<br>

# Mandatory assignment 3

This repository contains the third mandatory assignment (MA3) for AIML25.  

* **Dev setup**: Just like for MA1 and MA2, to complete this assignment, you need to follow the Development Setup guide. Please complete this setup before starting the assignment.

* **Guides**: Each of the sub-assignments has a corresponding *guide notebook*. Everything needed to complete the assignments is in those notebooks. The guide notebooks are there to help you understand and practice the concepts. Please refer to the table below:

    | Assignment | Assignment notebook | Guide notebook | Description |
    | --- | --- | --- | --- |
    | Part 1 | [assignments/rag.ipynb](assignments/rag.ipynb) | [guides/rag_guide.ipynb](guides/rag_guide.ipynb) | Retrieval-Augmented Generation |
    | Part 2 | [assignments/agents.ipynb](assignments/agents.ipynb)| [guides/router_agents_guide.ipynb](guides/agents_guide.ipynb)<br>[guides/tool_agents_guide.ipynb](guides/tool_agents_guide.ipynb) | Agentic LLM Systems |

* **Dataset**: In the `rag_guide.ipynb` notebook, we use a single markdown document (`data/madeup_company.md`) as our external knowledge source, to simulate the very common scenario of building a RAG system with access to company information. For your assignment, you can experiment further with this dataset or use your own. It could be any PDF, website, text file etc. that you find interesting. In `tool_agents_guide.ipynb`, we will use built tools like web search and RAG. You are, of course, more than welcome to add any tools and knowledge sources you find interesting.

* **Local modules**:
Some of the guide notebooks rely on `src/llm.py` for LLM inference with `instructor` and `litellm`. Please read through the [`instructor_guide.ipynb`](guides/instructor_guide.ipynb) notebook to understand how and why this can be useful. 

* **Using Google Colab**: The heavy compute (i.e., LLM inference and text embedding) for this assignment will all be remote via WatsonX.ai. However, as always, you are free to use Google Colab. If you do use Colab, please make sure to download the finished notebook and save it to your local machine as `ma3/assignments/<type>` before committing your code to GitHub and submitting the assignment. We are calling `src/llm.py::LLMCaller` in the `router_agents_guide.ipynb` notebook, so you will need to copy-paste the `src/llm.py` file to your Colab environment.

## Part 1: Retrieval-Augmented Generation (RAG)
In this part, you will implement and evaluate a simple RAG system. You will use an embedding model to vectorize your documents and an LLM for text generation. Both types of models are available through WatsonX.ai. Specifically, your task is to:

- Explore the accompanying guide in the `guides/rag_guide.ipynb` notebook.
- Use an embedding model to vectorize the dataset
- Chunk and preprocess the vectorized dataset and store the vectors in a vector index
- Use the vector index to retrieve the most similar documents to a given query.
- Use the retrieved documents as context for the LLM to generate a response.
- Experiment with different hyperparameters to (possibly) improve performance over the baseline in `rag.ipynb`.
- Evaluate your RAG system.
- Briefly reflect on the performance of your system and your choices of preproceessing, model hyperparameters etc.
    - Write your analysis as a markdown cell in the bottom of the notebook.

## Part 2: AI Agents
In this part, you will implement and evaluate a simple tool-using LLM Agent using LangGraph (or any other framework you want!). Specifically, your task is to:

- Explore the accompanying agents guides (`guides/router_agents_guide.ipynb` and `guides/tool_agents_guide.ipynb`).
- Use LangGraph to create a simple `router` agent *OR* tool-using LLM Agent in the `assignments/agents.ipynb` notebook.
- Experiment with different techniques covered in the course to (possibly) improve performance over the baseline in `router_agents.ipynb` or `tool_agents.ipynb`.
- Evaluate your AI Agent - or at least comment on how you would evaluate it.
- Briefly reflect on the performance of your system and your choices of preprocessing, hyperparameters etc.
    - Write your analysis as a markdown cell in the bottom of the notebook.

***

**NOTE**: Please be mindful of token usage - but don't worry too much about it. The WatsonX.ai platform provides a generous amount of tokens for this assignment but don't use `while True` loops or similar constructs that could potentially consume a lot of tokens. If you are unsure about your token usage, please reach out to us!
***

<br>

**Please see due dates and other relevant information in the assignment description on Canvas.**

<br>

***

## Getting started
Please see the relevant sections in the `Development setup guide` document on Canvas for instructions. To iterate, you need to:

1. Fork this repository to your own GitHub account.
2. Clone the forked repository to your local machine.
3. Create a virtual environment (from `environment.yml` with conda) and install the required packages.
4. Start working on the assignment.
5. Commit and push your changes to your GitHub repository.
6. Submit a link to your GH assignment repo on Canvas (make sure that your repository is public!).

___