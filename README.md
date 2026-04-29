
# Tvara AI Tasks Submission

This repository contains the implementation of assigned tasks for the Tvara AI evaluation.

---

## Task A — LeetCode Problem (In Progress)

**Problem:** Linked List Cycle II  
Link: https://leetcode.com/problems/linked-list-cycle-ii/

### Status:
Currently learning Data Structures and Algorithms (DSA) concepts required to solve this problem efficiently.

### Approach (Planned):
The problem involves detecting a cycle in a linked list and identifying the node where the cycle begins.

The optimal approach uses Floyd’s Cycle Detection Algorithm (Tortoise and Hare):

1. Use two pointers (slow and fast)
2. Detect if a cycle exists
3. Reset one pointer to head
4. Move both one step at a time
5. The meeting point is the start of the cycle

### Learning Outcome:
- Understanding linked list traversal
- Cycle detection techniques
- Pointer manipulation

---

## Task B — API Integration (Gemini 2.5 Flash)

### Objective:
Integrate Google's Gemini API and build a simple interface to send prompts and receive responses.

### Implementation:
- Built a CLI-based interface using Python
- Used `requests` library to send POST requests
- Integrated Gemini 2.5 Flash model via REST API

### Key Features:
- Accepts user input dynamically
- Sends request to Gemini API
- Displays generated response
- Optional debug mode to view raw API response
- Error handling for API failures

### API Details:
- Endpoint:
  https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash:generateContent
- Authentication via API Key (header-based)

### Request Format:
```json
{
  "contents": [
    {
      "parts": [{"text": "user prompt"}]
    }
  ]
}
````

### Output:

Returns generated text from the model.

### Example:

**Input:**

```
What is RAG?
```

**Output:**
Retrieval-Augmented Generation (RAG) is a technique that enhances LLM responses by retrieving relevant external data before generating answers.

### Learnings:

* Working with real-world AI APIs
* Handling HTTP requests and responses
* Debugging API errors (e.g., 503 overload)
* Structuring clean and minimal API integration

### Improvements:

* Move API key to environment variables
* Add retry mechanism for failed requests

---

## Task C — Vectorization with Hugging Face

### Objective:

Use an embedding model to convert text into vectors and perform similarity search.

### Model Used:

`intfloat/e5-small-v2`

### Implementation Steps:

1. Load embedding model using Sentence Transformers
2. Define sample sentences (knowledge base)
3. Convert sentences into embeddings
4. Convert query into embedding
5. Compute similarity using cosine similarity
6. Return the most relevant sentence

### Important Detail:

The E5 model requires prefix formatting:

* "passage: " for stored sentences
* "query: " for user input

### Example:

**Query:**

```
What is machine learning?
```

**Output:**

```
Best Match: Machine learning is a subset of AI.
Score: 0.87
```

### Learnings:

* Understanding embeddings and vector representations
* Semantic search using cosine similarity
* Basics of retrieval systems
* Foundation for Retrieval-Augmented Generation (RAG)

### Notes:

* Hugging Face authentication warning was observed but does not affect functionality since the model is public.



