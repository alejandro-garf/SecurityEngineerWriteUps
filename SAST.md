## Code Review

### Notes
- Review from the previous room.

### Questions
- Automated code reviews are not a substitute for manual reviewing.
- The second question is fairly self-evident.
- Manual review would be more thorough.

---

## Manual Code Review

### Notes
- We `cd` into the directory of the simple web app.
- Run the provided `grep` command.
- Through this, we find a SQL injection vulnerability.

### Questions
- For the first question, examine the code of `hidden-panel.php`.
- Run the `grep` command again with `include` and got 9 instances.
- `view.php` is vulnerable because it is the only file with a GET request.
- The GET request is at line 22.

---

## Automated Code Review

### Notes
- Most SAST tools represent code using Abstract Syntax Trees (AST).
- **Semantic analysis** can be compared to grepping for potentially insecure functions during manual code reviews. It aims to find flaws concerning the use of potentially insecure code in a localised context.
- **Dataflow analysis** traces how information flows from inputs the user can manipulate to potentially vulnerable functions.
  - In dataflow analysis terminology, data inputs are referred to as **sources**, and potentially vulnerable functions are referred to as **sinks**. If data flows from a source to a sink without sanitisation, a vulnerability exists.
- **Control flow analysis** analyses the order of operations in code in search of race conditions, use of uninitialised variables, or resource leaks.
- **Structural analysis** analyses specific code structures of each programming language.
- **Configuration analysis** searches for application configuration flaws rather than flaws in the code itself.

### Questions
- A running application is not required to run a SAST tool.
- A structural analysis would likely flag a dead code segment.
- A configuration analysis would detect flaws in configuration files.
- Semantic analysis is similar to grepping the code in search of flaws.

---

## Rechecking Our Application with SAST Tools

### Notes
- **Psalm** (PHP Static Analysis Linting Machine) is a simple tool for analysing PHP code.
- We run the provided command to execute Psalm.
- Dataflow analysis typically yields the most interesting findings from a security standpoint.
- Annotations can be used to give the tool more context.
- A certain level of false positives and false negatives is always expected when using SAST tools. The report must always be manually reviewed for errors. SAST is an excellent complement to manual reviews but should never be considered a replacement.

### Questions
- The answer is a **false positive**.
- 9 errors were returned after annotating the file.

---

## SAST in the Development Cycle

### Notes
- **CI/CD integration:** Each time a pull request or merge is made, SAST tools check the code for vulnerabilities.
- **IDE integration:** SAST tools can be integrated directly into developers' IDEs rather than waiting for a pull request or merge.

### Questions
- Open the file in VS Code.
- Upon opening, 27 errors were detected by Semgrep.
- 8 errors were shown in the `showrecipe.inc.php` file.
- The other rule shown is `echoed-request`.
- `echoed-request` relates to **Cross-Site Scripting (XSS)**.
