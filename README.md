# OJ Prism

**See Beyond Code.**

OJ Prism is an interactive programming-learning environment designed to help developers understand code beyond syntax: how it is structured, how it behaves during execution, and how language concepts connect to the underlying computer.

Rather than treating programming as a sequence of lessons and exercises, OJ Prism aims to make concepts explorable. Look up an idea, inspect a piece of code, follow its behavior, and build a clearer mental model of the systems behind it.

**Learn · Explore · Understand**

## Vision

Programming knowledge is scattered across documentation, tutorials, compiler output, debuggers, and countless small experiments. Learners often have to combine several tools just to answer one question.

OJ Prism aims to bring these activities into one coherent environment:

- Explore programming and computer-science concepts through a structured knowledge base.
- Inspect source code and understand its structure.
- Experiment with small examples without unnecessary setup.
- Observe execution and the relationships between values, variables, and memory.
- Connect high-level language features to the behavior of the underlying machine.

The goal is not to hide complexity. It is to make complexity easier to see.

## Planned capabilities

The capabilities below are project goals, not implemented features.

### Interactive knowledge base

A searchable, interconnected reference covering language fundamentals, common patterns, data types, control flow, data structures, common bugs, compiler diagnostics, memory, execution, and computer-science foundations.

The knowledge base should be language-aware without being tied to a single programming language.

### Code analysis

Tools that inspect source code and explain its structure and meaning.

For example, in C:

```c
int *x, y, c;
```

OJ Prism should clarify that `x` is a pointer to `int`, while `y` and `c` are ordinary `int` objects. Longer term, it should explain declarations, types, expressions, scopes, and relationships using structured analysis rather than guesswork.

### Execution exploration

An environment for experimenting with code and following what happens as it runs.

For example:

```c
int a = 10;
int *x = &a;

*x = 50;
```

A learner should be able to follow how `x` refers to `a`, how dereferencing accesses the object, and how the assignment changes its value.

### Memory visualization

A visual explanation of objects, values, addresses, pointers, and references.

OJ Prism will distinguish clearly between:

- **Conceptual models:** educational representations of language and computer-science concepts.
- **Static analysis:** reasoning about source code without executing it.
- **Runtime observations:** information collected from a particular execution.

These are related, but they are not interchangeable. Visualizations must communicate what is observed, what is inferred, and what is simplified.

## Technical direction

- **Primary implementation language:** Rust.
- **Initial analysis target:** C.
- **Compiler infrastructure:** LLVM/Clang tooling may be used where it provides reliable parsing, diagnostics, or program information.
- **Initial interface:** an interactive terminal experience.
- **Architecture:** modular components with clear boundaries between knowledge, analysis, execution, and presentation.

Rust is selected to support productive development while providing strong abstractions and memory safety for the core application. The implementation language does not limit the languages OJ Prism can inspect.

Specific libraries and implementation choices will be evaluated as the project develops.

## Development roadmap

The roadmap is incremental. Each stage should produce something useful before the project grows more ambitious.

- [ ] **Project foundation** — repository structure, development principles, and initial technical design.
- [ ] **Knowledge prototype** — a small searchable collection of concepts and examples.
- [ ] **C analysis prototype** — parse and explain a limited set of C constructs.
- [ ] **Interactive CLI** — a consistent terminal workflow for exploring concepts and code.
- [ ] **Execution prototype** — run controlled examples and collect useful runtime information.
- [ ] **Memory visualization** — connect source-level concepts with observed runtime behavior.
- [ ] **Expanded language support** — add language features, concepts, and eventually additional languages.

## Design principles

1. **Understanding over memorization.** Explain why something behaves as it does, not only what to type.
2. **Visible complexity.** Make hidden relationships easier to inspect instead of pretending they do not exist.
3. **Accuracy and honesty.** Separate facts, analysis, runtime observations, and educational simplifications.
4. **Incremental development.** Prefer small, testable capabilities over a huge unfinished system.
5. **Modularity.** Keep knowledge, language tooling, execution, and interface independently evolvable.
6. **Practical exploration.** Make it easy to move from a question to an experiment.

## Project status

**Early concept / under development.**

OJ Prism is currently at the planning and foundation stage. The capabilities described above are goals and should not be considered implemented or ready for use.

## License

OJ Prism is licensed under the **GNU General Public License v3.0 or later (GPL-3.0-or-later)**. See the [LICENSE](LICENSE) file for the full license text.
