# ExamScope

### Analyse Exam Papers. Discover Patterns. Prepare Smarter.

ExamScope is an AI-powered PDF-to-insights platform that helps students explore previous examination papers. It extracts text from digitally readable PDFs, organizes related questions using semantic embeddings and clustering, and provides an AI-assisted chat interface for exploring the uploaded material.

The current project demonstration uses ICSE Class 10 previous-year question papers with solutions sourced from Oswaal 360.

## Problem

Previous examination papers can contain recurring questions, related concepts, and patterns. However, these details are spread across multiple documents and are difficult to explore together manually.

ExamScope brings uploaded papers into one workflow so students can search related content and examine patterns more conveniently.

## Objectives

1. **PDF Processing and Information Extraction** — Extract, clean, and chunk text from digitally readable PDF papers using PyMuPDF4LLM.
2. **Semantic Search and Clustering** — Create embeddings and use ChromaDB with HDBSCAN to group semantically related questions and concepts.
3. **AI-Based Analysis** — Use retrieved document content to support a chatbot that helps explore questions, topics, and patterns.

## Features

* Upload and process multiple digitally readable PDF question papers.
* Extract text and split it into manageable chunks.
* Generate semantic embeddings for question-paper content.
* Store and retrieve embedded content with ChromaDB.
* Group related content using HDBSCAN clustering.
* Explore uploaded material through AI-assisted analysis and chat.
* Use a Gradio interface for document upload and interaction.

## Technology Stack

| Technology                                 | Purpose                       |
| ------------------------------------------ | ----------------------------- |
| Python                                     | Main programming language     |
| Jupyter Notebook / Google Colab            | Development and execution     |
| PyMuPDF4LLM                                | PDF text extraction           |
| LangChain Text Splitters                   | Text chunking                 |
| Sentence Transformers (`all-MiniLM-L6-v2`) | Text embeddings               |
| ChromaDB                                   | Vector storage and retrieval  |
| HDBSCAN                                    | Semantic clustering           |
| Gemini API                                 | AI-assisted analysis and chat |
| Gradio                                     | User interface                |

## How It Works

1. **Upload PDFs:** The user uploads digitally readable exam-paper PDFs.
2. **Extract Text:** PyMuPDF4LLM extracts document text.
3. **Chunk Content:** The text is divided into smaller chunks for processing.
4. **Create Embeddings:** Sentence Transformers converts chunks into vector representations.
5. **Store and Retrieve:** ChromaDB stores the vectors and retrieves relevant content.
6. **Cluster Related Content:** HDBSCAN groups semantically similar items.
7. **Analyze and Chat:** Retrieved document content is provided as context for AI-assisted analysis through the Gradio interface.

## How to Run in Google Colab

1. Open the project notebook in Google Colab.
2. Add your Gemini API key using Colab Secrets and make it available to the notebook as expected by its configuration.
3. Run the notebook cells in order.
4. Launch the Gradio interface.
5. Upload one or more digitally readable question-paper PDFs.
6. Start the analysis and wait for processing to complete.
7. Review the generated analysis and use the chatbot to ask questions about the uploaded papers.

**Note:** API access may require a valid key and may be subject to provider quotas or charges. Never upload API keys or other secrets to GitHub.

## Example Questions

* Which topics appear across the uploaded papers?
* Find questions that are semantically related.
* What patterns can be observed in these papers?
* Summarize the main concepts represented in the uploaded documents.
* Show related questions that could help with revision.

The responses depend on the uploaded documents and retrieval results. They should be checked against the original papers.

## Current Scope and Limitations

* The current workflow is intended for digitally readable PDFs; OCR for scanned papers is future scope.
* Metadata extraction is based on the current regex-based approach and may not identify every paper detail correctly.
* A semantic cluster indicates similarity, not proof that questions are exact repeats.
* AI-generated responses can be incomplete or incorrect; verify important details using the source papers.
* ExamScope does not predict future examination questions or guarantee which topics will appear.
* The project demonstration is based on ICSE Class 10 papers; broader board and source support is future work.
* No formal accuracy benchmark is claimed.

## Future Scope

* Add OCR support for scanned question papers.
* Improve paper metadata extraction.
* Add topic-wise and frequency-based analysis.
* Extend support to other boards, examinations, and educational sources, including suitable official portals, subject to access rules and terms.
* Compare prescribed syllabus topics with topics and question forms found in historical papers.
* Develop a student-focused revision assistant.
* Improve scalability, efficiency, and integration with educational platforms.

## Data Source and Attribution

The demonstration papers were sourced from Oswaal 360, including ICSE Class 10 previous-year papers with solutions. ExamScope is an educational project and is not affiliated with or endorsed by Oswaal.

Sample question papers are used for educational demonstration purposes. Please respect the original source's copyright and terms of use.

## Third-Party Software and Licensing

This project uses third-party libraries and services, each subject to its own license and terms.

**ExamScope — Analyse Exam Papers. Discover Patterns. Prepare Smarter.**
