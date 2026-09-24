<a id="ml-rag-и-небольшой-capstone"></a>

# ML, RAG, and a small capstone

Main stage 4. [NVIDIA RAG and prerequisites](../WORK_INTEGRATED_ROADMAP.md) · [Module map](README.md)

Prerequisites: Python/OOP and introductory deep learning; the course recommends PyTorch experience. Start with a task and a measurable baseline.

<a id="по-порядку"></a>

## In order

1. [Google ML Crash Course](https://developers.google.com/machine-learning/crash-course): splits, overfitting, classification/evaluation.
2. [PyTorch Basics](https://docs.pytorch.org/tutorials/beginner/basics/) and [HF LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) for relevant gaps, not mandatory completion of both entire courses.
3. NVIDIA Building RAG Agents from the roadmap → assessment.
4. [Stanford IR](https://nlp.stanford.edu/IR-book/): retrieval/evaluation; [Qdrant docs](https://qdrant.tech/documentation/) if chosen for the exercise.
5. Take up PEFT/fine-tuning after establishing a baseline and a demonstrated need; links and books remain in the roadmap.

<a id="практика-маленький-поиск-по-документам"></a>

## Practice: a small document search system

Prepare about 20 synthetic documents and 20 questions. Include questions without answers and documents belonging to different practice users. This dataset tests the mechanics, not production quality.

- Establish a simple baseline, then embedding retrieval and, if needed, reranking.
- Identify relevant documents for each question; separate tuning examples from the final evaluation.
- Measure retrieval separately from generation: whether the source is found, whether the answer addresses the question, whether the source supports it, and when the system should abstain.
- Check that context and answers do not reveal another owner’s documents. Post-filtering after generation does not replace access control.
- Compare one parameter: chunk size, k, or reranker. Save configurations, raw results, and errors.
- Validate LLM-as-judge against labeled examples; do not present its score as independent truth.

The [QA module](quality-and-evaluation.md) helps with sampling and regressions. Study serving and load in [CUDA/inference](cuda-and-inference.md).

<a id="capstone--по-желанию-один-сценарий"></a>

## Capstone — optional, one scenario

Choose **either** search with citations **or** PII findings review. You do not need to build two products at once.

Components: synthetic inputs → backend → chosen pipeline → review/API → result export. Add one quality report, an access boundary, reproducible startup, and a recovery scenario. The interface can be minimal.

Finish when another person, or you in a clean learning environment, can reproduce startup and verify one successful and one failing scenario. Real operation requires separate acceptance.

<a id="выход-и-награда"></a>

## Outcome and award

A baseline, an honest comparison, and clear limitations. [LLM Systems Exam](../exams/MASTER_EXAMS.md#llm-systems-exam).

The NVIDIA certificate recognizes course completion. Your retrieval baseline and capstone earn separate personal achievements; celebrate a finished project before taking any next course.
