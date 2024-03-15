# SentenceWindowNodeParser-MetaDataReplacement

This repository contains a Jupyter Notebook demonstrating how to use Metadata replacement + node sentence window in a RAG pipeline.

SentenceWindowNodeParser is a tool that can be used to create representations of sentences that consider the surrounding words and sentences. During retrieval, before passing the retrieved sentences to the LLM, the single sentences are replaced with a window containing the surrounding sentences using the MetadataReplacementNodePostProcessor. This can be useful for tasks such as machine translation or summarization, where it is essential to understand the meaning of the sentence in its entirety. This is most useful for large documents, as it helps to retrieve more fine-grained details.

In this project, we are using Ollama, for loading our LLM locally in CPU, and Llamaindex data framework for communicating with the LLM and RAG model. 

## Prerequisites

Before running the notebook, ensure you have completed the following steps:

1. Install OLLAMA Locally: You need to install OLLAMA on your local machine. Follow the installation steps provided in the OLLAMA repository: OLLAMA Installation Guide.

2. Install Mistral LLM: After installing OLLAMA, open your terminal and execute the following commands to install the Mistral LLM:

```bash
ollama pull mistral
```
3. Serve Mistral LLM: Once Mistral LLM is successfully installed, run it locally by executing:

```bash
ollama serve
```
