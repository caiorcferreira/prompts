# LLM Prompts Collection

This repository is a collection of LLM prompts. It includes a Taskfile for syncing the `patterns` folder with `~/.config/fabric/patterns/`, which allows them to be used with [Fabric](https://github.com/danielmiessler/fabric/tree/main).

## Prerequisites

- Task: A task runner / simpler Make alternative written in Go. [Install Task](https://taskfile.dev/#/installation)

## Usage

To sync the `pattern` folder with `~/.config/fabric/patterns/`, run the following command:

```bash
task sync
```

### Example

Given the transcript of the lecture [Lecture 1B: Boolean Logic Semantics](https://www.youtube.com/watch?v=-o1QgB4TeZk), the `thought_provoking` prompt generated the following questions:

```
1. **Essence Summary Question:**
   - In no more than 50 words, how does the lecture describe the significance of understanding the semantics of propositional sentences in logic?

2. **Analytical Deep Dive Questions:**
   - How does the lecture differentiate between the properties of consistency and validity in propositional logic, and why are these distinctions important?
   - Discuss the role of the 'models of a sentence' concept in understanding the semantics of propositional logic. How does this concept aid in determining the truth of a sentence in various worlds?
   - The lecture introduces set operations (intersection, union, complement) to manipulate the models of sentences. How do these operations facilitate reasoning about logical sentences, and can you provide examples illustrating their use?
   - Reflect on the relationship between knowledge and data as discussed in the lecture. How does knowledge help in reducing the need for data in making logical deductions?

3. **Personal Connection Question:**
   - Can you recall a situation in your life where understanding the underlying semantics or meaning behind statements could have led to better decision-making or clearer communication?

4. **Practical Application Question:**
   - Considering the lecture's discussion on semantics, how can the principles of propositional logic be applied to improve algorithms in fields like artificial intelligence or data science?

5. **Reflective Impact Question:**
   - How has your understanding of the semantics of propositional sentences changed after this lecture, and what impact do you think this new understanding could have on your approach to logical reasoning?

6. **Exploratory Future Inquiry Question:**
   - What unanswered questions or new avenues of exploration have emerged for you regarding propositional logic and its application after engaging with this lecture?
```