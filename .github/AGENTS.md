# AGENTS Guidelines for this Repository

This repository contains the LaTeX source code for a master's thesis. When making edits to the LaTeX files, primarily focus on the content and structure of the thesis. Adhere to the following guidelines:

# Writing Principles

1. **Content Accuracy**: Ensure that all information is accurate and well-researched. Any claims or statements should be supported by credible sources and properly cited.
2. **Clarity and Coherence**: Write in a clear and concise manner. Ensure that the thesis is logically structured, with a clear introduction, body, and conclusion. Each section should flow smoothly into the next.
3. **Use provided writing notes**: When writing or rewriting sections of the thesis, writing notes will be referenced in the initial prompt.
4. **Consistency**: Maintain consistency in terminology, style, and formatting throughout the thesis. Utilise the existing LaTeX files as a reference for writing style.

# Citation and Referencing

1. **Proper Citation**: Always cite sources appropriately using `\parencite{}` for standard citations and `\textcite{}` for in-text citations. Ensure that all sources cited in the text are included in the bibliography. When writing content, provide a list of sources that are missing from the bibliography in `author-year` format (e.g., `Miller2019`).
2. **Bibliography Management**: Ensure that the bibliography is well-organized and formatted using the LaTeX workshop extension.

# Writing Process

1. **Required Writing Notes**: When writing or rewriting sections of the thesis, writing notes will be provided in `.writing-notes/` directory. Validate the notes against the prerequisites outlined in the section writing instructions before proceeding. If any prerequisites are missing or if there are ambiguities in the notes, ask for clarification before starting to write.
2. **Iterative Writing**: The writing process may involve multiple iterations. After each iteration, review the changes made and provide feedback for further improvements. Focus on enhancing the clarity, coherence, and overall quality of the writing in each iteration.
3. **Collaboration**: If you have any questions or need clarification on the writing notes or any aspect of the thesis, ask for clarification before proceeding

# Instructions

Instructions for different tasks can be found in the `.github/instructions/` directory. When performing a task, follow the instructions provided in the relevant file. If you encounter any ambiguities or have questions about the instructions, ask for clarification before proceeding.

# LaTeX

The entry point to the LaTeX source code is the file `thesis.tex` containing the main document structure. It also contains the frontmatter of the document, referencing used packages and imported files. The main content of the thesis is located in the `contents/` directory, with each section and subsection in a separate `.tex` file. Supporting code like custom LaTeX snippets are defined in the `helper/` directory. Imported images and code are located in the respective `images/` and `code/` directories. The bibliography is managed in the `literature.bib` file.
