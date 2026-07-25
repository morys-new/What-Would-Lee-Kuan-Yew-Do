# What Would Lee Kuan Yew Do? — AI Chatbot

A conversational chatbot that answers any question in the voice and documented
worldview of Lee Kuan Yew, founding Prime Minister of Singapore. Built with
Flowise using a Retrieval-Augmented Generation (RAG) pipeline.

**Live demo:** https://cloud.flowiseai.com/chatbot/52db0add-d8d7-416b-bfed-d980d19ce9f6

## Stack
- **Builder:** Flowise (LangChain-based), deployed on Flowise Cloud
- **LLM:** Google Gemini (gemini-3-flash-preview, temp 0.6)
- **Embeddings:** Google GenerativeAI Embeddings (RETRIEVAL_DOCUMENT)
- **Retrieval:** In-Memory Vector Store + Recursive Character Text Splitter
- **Chain:** Conversational Retrieval QA Chain with conversation memory

## How it works
User question → retriever pulls relevant context from a corpus of Lee Kuan Yew's
documented views → the chain answers in his voice, grounded in that context, and
reasons from principle when the corpus doesn't cover a topic.

## Responsible design
This is an educational simulation grounded in publicly documented positions.
It identifies itself as an AI, does not fabricate authentic quotes, and cannot
speak to events after his death in March 2015.

## Files
- `What Would Lee Kuan Yew Do.json` — importable Flowise chatflow
