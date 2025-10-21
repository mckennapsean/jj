## **Project Plan: Contributing to Jujutsu (jj-vcs)**

### **Phase 1: Foundation & Strategy (Your First 1-2 Weeks)**

The goal of this phase is to align your skills with the project's actual needs and technical stack.

1.  **Confirm the Tech Stack (A Key Pivot)**
    * You mentioned learning Go, which is a great skill. However, the `jj` CLI is written in **Rust**.
    * **Action:** If you want to contribute to the core codebase, your project plan must include **learning Rust**, not Go. You can start this in parallel with other contribution paths.

2.  **Internalize the Contribution Workflow**
    * The `jj` project has a specific and well-documented workflow. Reading this first will save you a lot of time.
    * **Action:** Read the official [**Contributing Guidelines**](https://jj-vcs.github.io/jj/latest/contributing/).
    * **Key Takeaways:**
        * **CLA:** You will need to sign a Contributor License Agreement.
        * **Commit-by-Commit Review:** They review each commit separately, not the PR as a whole. They do *not* squash-merge, so your commits must be clean.
        * **Amending Commits:** When you get PR feedback, you are expected to *amend the original commit* (e.g., using `jj squash`) rather than adding new "fixup" commits.
        * **Tooling:** You'll need to install Rust. The key commands for testing and formatting are `cargo insta test --workspace` (for snapshot tests) and `cargo +nightly fmt` (for formatting).

### **Phase 2: Choose Your First Contribution Path**

Here are your ideas, validated against the project's needs, ranked from lowest to highest barrier to entry. You can start with Path A while learning Rust for Paths C and D.

#### **Path A: Documentation & Tutorials (Low Difficulty, High Impact)**

Your ideas to "Help with docs" and "Create tutorials" are excellent and highly valued. The `jj` documentation is good, but the community is actively growing it.

* **Your Project Task:**
    1.  **Fix Doc Discrepancies:** The [official CLI reference](https://jj-vcs.github.io/jj/latest/cli-reference/) is auto-generated and marked as "experimental." A perfect first task is to run `jj help <COMMAND>` (e.g., `jj help log`) and compare the output to that webpage. If you find any differences, file a bug or a PR to correct the reference.
    2.  **Write a Learner's Tutorial:** You are in the perfect position to write a "getting started" guide. As you learn, document your process. Community tutorials are frequently shared and appreciated.

#### **Path B: UI & Tooling (Medium Difficulty)**

Your interest in `jjui` is spot on. Improving the UI/UX and developer tooling is a major goal for the `jj` project.

* **Your Project Task:**
    1.  **Contribute to `jjui`:** Find the `jjui` repository (it's separate from `jj-vcs/jj`) and look at its issue tracker for "good first issues." Helping that project directly helps the `jj` ecosystem.
    2.  **Monitor the API Roadmap:** The [official roadmap](https://jj-vcs.github.io/jj/latest/roadmap/) explicitly mentions plans for a "Better Rust API for UIs" and an "RPC API." Engaging in discussions about these (on Discord or GitHub) is a great way to get involved in the "simpler UIs" concept you mentioned.

#### **Path C: Core Code Contribution (High Difficulty)**

This is the most involved path but also very rewarding. This requires learning Rust.

* **Your Project Task:**
    1.  **Start with "Good First Issues":** Go to the `jj-vcs/jj` [GitHub repository Issues tab](https://github.com/jj-vcs/jj/issues) and filter by labels like **"good first issue"** or **"help wanted"**. This is the single best way to find a task the maintainers have already approved.
    2.  **Help the Roadmap:** The roadmap mentions a need to move logic from the `jj-cli` crate into the `jj-lib` crate (to help UI builders like `jjui`). This is an advanced but critical refactoring task. You could search for issues related to this.

#### **Path D: Profiling & Performance (Advanced)**

Your idea to "Profile and speed things up" is a core value of `jj`.

* **Your Project Task:**
    1.  **Find a Bottleneck:** Search the issue tracker for "performance" or "benchmark."
    2.  **Open an Issue First:** Before writing a lot of code, run your own profiling, find a bottleneck, and *open an issue* to discuss your findings. This ensures your work aligns with the project's direction.

***

### **Phase 3: Executing Your First Contribution**

1.  **Pick One Small Task:** Choose a single, small task from Phase 2 (e.g., a documentation fix).
2.  **Communicate:** Use the **Discord** (which you're already on) or open a **Draft Pull Request** on GitHub to state what you're working on. This prevents duplicated effort.
3.  **Develop:** Follow the contribution guidelines from Phase 1 (use `cargo +nightly fmt`, run `cargo insta test`, and write a clean commit message like `docs: Fix help text for 'jj log'`).
4.  **Submit & Iterate:** Submit your PR. Be ready for feedback and remember to *amend* your commit rather than adding new ones.

