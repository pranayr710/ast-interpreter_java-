# MicroJava AST Interpreter

A compiler, interpreter, and visualizer for the MicroJava programming language.  
This project parses MicroJava source code into an Abstract Syntax Tree (AST), executes it through an interpreter, and provides a JavaFX-based GUI for real-time AST visualization, symbol table inspection, and debugging.

---

## What is MicroJava?

MicroJava is a simplified subset of the Java programming language designed for educational purposes, primarily to teach compiler construction and programming language concepts.  

It includes:
- Variables and arrays
- Methods
- Control structures (if-else, while)
- Input/output operations  

It does not support advanced Java features like classes, inheritance, or exceptions.

---

## Features

- AST Generation and Visualization  
  - Parses MicroJava code into an AST  
  - Displays AST graphically via SVG (Apache Batik + JavaFX WebView)  

- Interactive Interpreter  
  - Executes programs directly from the AST  
  - Manages memory areas: global data, heap, expression stack, method stack  

- Debugger Support  
  - Step-by-step execution  
  - Breakpoints on AST nodes  
  - Execution highlighting  

- Symbol Table Management  
  - Displays variables (local and global) with type, scope, address, and current values  

- Error Handling  
  - Detects runtime issues: null references, array index out of bounds, stack overflows  

- Other Features  
  - File watching: auto-reloads AST visualization when updated  
  - I/O operations (printing, reading input)  
  - Control flow (if-else, while, break, return)  

---

## Project Structure


---

## Prerequisites

- Java 17 or higher (required for JavaFX support)  
- Maven 3.6 or higher  
- No manual dependency downloads needed. Maven resolves everything automatically.  

---

## Dependencies

Main runtime dependencies:
- JavaFX 17.0.2  
  - javafx-controls – GUI components  
  - javafx-fxml – FXML layouts  
  - javafx-web – SVG rendering via WebView  
  - javafx-swing – Optional Swing integration  
- Apache Batik 1.17 – SVG rendering/manipulation  
- JetBrains Annotations – Code documentation  

Testing dependencies:
- JUnit 5 (Jupiter API + Engine) – Unit testing  

Build plugins:
- Maven Compiler Plugin – Java compilation  
- JavaFX Maven Plugin – Running JavaFX apps via Maven  

Additional tools:
- Coco/R – Parser generator (Coco.jar included in mj/run/)  

---

## Running the Project

1. Clone the repository
   ```bash
   git clone https://github.com/your-username/microjava-ast-interpreter.git
   cd microjava-ast-interpreter

2.BUild the projest using mvn clean install

3.Run java fx gui using : .\mvnw.cmd javafx:run


Usage

Open a .mj file (for example, sample.mj).

Click Compile to parse and generate the AST.

Use:

Run → Executes the program

Debug → Step-by-step execution with highlighting

Symbol Tables → Inspect variables and memory

References

MicroJava Documentation – JKU: https://ssw.jku.at/Teaching/Projects/

Coco/R Compiler Generator: https://ssw.jku.at/Research/Projects/Coco/
