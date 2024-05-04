# chief_of_staff
A repo focused on use cases and tool development for OpenAI GPT use (API and Chat)

# GPT Syntax

Using a controlled and consistent vocabulary helps immensely when working with GPT tools.

## Format

GPT understands plaintext files. Use Markdown to encode emphasis or other useful shorthand.

I have confirmed the following:
- [ ] list membership (bullets)
- [ ] sequential steps (numbered list)
- [ ] Related content (headers and sub headers)
- [ ] Linking up to a previous section
- [ ] use of check boxes to indicate prerequisites
- [ ] quotes and single quotes for being explicit
- [ ] capitalize terms for emphasis

## File Use

The Chat GPT maintains a session based record of uploaded or written files.

Location of data: `/mnt/data`

Guidance:
- refer to files explicitly by name (reading or writing)
- prefer clear and descriptive names
- always define abbreviations for later if using them (e.g. FY means financial year)
- if you want GPT to actually reference the file for information say something like "Refer to the uploaded document 'Budget_Report_2023.xlsx' for financial data."
    - often GPT will just use its expansive internal dataset if it thinks it has enough info / similiarity so be explicit here

## Python use

Chat GPT comes with a preconfigured set of python libraries installed. The kernel is jupyter-like and likely runs on ipython with some custom mods

- see the file `openai_chatgpt4_libraries.json` for more detail on the installed packages

## Internet use

The baseline Chat GPT cannot access the internet. 

# Working

# Custom GPT (reddit)

From: https://www.reddit.com/r/ChatGPTPro/comments/189bcfw/how_to_build_a_custom_gpt_properly/
## Adding Scientific method to GPT

### Instructions
The document outlines a structured workflow for applying the scientific method in Natural Language Processing (NLP), encompassing several key Chain of Thought stages:

Observation: This initial phase involves observing phenomena or data that sparks curiosity, laying the groundwork for further investigation.

Question: Following the observation, a relevant question is formulated to explain the observation or solve a problem.

Hypothesis: A testable prediction or educated guess is proposed to explain the question arising from the observation.

Experiment: The hypothesis is tested through controlled, repeatable procedures designed to collect data.

Analysis: Data collected from the experiment is analyzed, often using statistical methods, to determine if the results support or refute the hypothesis.

Conclusion: Interpretation of the data analysis results occurs. If results align with the hypothesis, it is supported; otherwise, it may be revised or rejected.

Communication: Results are communicated, often through publishing in scientific journals, presenting at conferences, or other forms of sharing. This step is crucial for peer review and contributing to scientific knowledge.

Reiteration: The scientific method is iterative, with the steps being repeated to refine hypotheses, explore new questions, and build upon previous research.

This approach reflects a dynamic, continuous process of scientific inquiry, with each stage contributing to expanding knowledge and understanding of the natural world. The document emphasizes maintaining a balance between scientific rigor and articulate, engaging communication.


## General guidance

### Instructions for Referring to Uploaded Files
Explicit File Reference: Instruct the GPT to explicitly refer to the file by its name. For example, "Refer to the uploaded document 'Budget_Report_2023.xlsx' for financial data."

Specific Data Points: Be clear about what information the GPT should extract or refer to within the file. For example, "From the file 'MeetingNotes_March.pdf', summarize the key action items listed on page 3."

Cross-Referencing: If using multiple files, instruct the GPT on how to cross-reference information. For example, "Compare the data in 'Sales_2022.csv' with 'Sales_2023.csv' and highlight the major differences in sales figures."

Contextual Clarity: Provide context if the file names are not self-explanatory. For example, "Analyze the 'ClientFeedback.txt' file which contains customer reviews from the last quarter."

Error Handling: Include instructions for handling errors or ambiguities in the files. For example, "If any data in 'Inventory_List.xlsx' is missing or unclear, flag it for manual review."

### File Naming and Formatting Tips
Descriptive Names: Use clear, descriptive names that easily identify the content and purpose of the file. For instance, 'Quarterly_Earnings_Report_Q1_2023.pdf' is more informative than 'QER1.pdf'.

Consistent Naming Conventions: Stick to a consistent naming convention for files. This could include date formats, categorization tags, or project names.

Standard File Formats: Use standard file formats that are widely recognized and compatible with most systems, like .pdf for documents, .xlsx for spreadsheets, and .csv for data files.

Organized Content: Ensure the content within the files is well-organized. For documents, use headings and subheadings; for data files, use clear column headers and consistent data entry formats.

Version Control in Names: If you’re working with multiple versions of a file, include version numbers or dates in the file names to avoid confusion.

Avoid Special Characters: Exclude special characters from file names that might be misinterpreted by systems, such as slashes, colons, or asterisks.

Readable Formatting: For text documents, use a clear and readable font size and style. For data files, ensure data is cleanly separated into rows and columns with no merged cells that could confuse data extraction.

### Preparing the Instruction File
Clear Structure: Organize the instructions in a step-by-step format. Each step should be clear and concise, guiding through the deployment process systematically.

Include Necessary Details: The file should contain all necessary details such as software requirements, configuration settings, API keys (if safe to include), and environment setup instructions.

Version Control: Mention the specific versions of software or dependencies to avoid compatibility issues.

Troubleshooting Tips: Include common issues that might arise during deployment and their solutions.

Security Guidelines: Clearly state any security practices that must be followed, such as how to handle sensitive data or credentials.

Formatting: Use a format that is easy to read and navigate, such as a PDF for text instructions or a CSV/Excel file for configuration settings.

### Instructing the GPT to Use the File
Direct Reference to the File: Instruct the GPT to refer to specific sections of the file for each part of the deployment process. For example, "Refer to section 2 of the 'Deployment_Guide.pdf' for setting up the environment variables."

Contextual Understanding: Ensure the GPT understands the context of each instruction. If the file contains technical jargon or complex instructions, the GPT should be capable of interpreting these correctly.

Iterative Process: If the deployment process involves testing and validation, instruct the GPT to cycle through the deployment instructions, testing, and troubleshooting sections iteratively until successful deployment is achieved.

Feedback Loop: Instruct the GPT to provide feedback or log its progress at each step based on the instructions. This could involve confirming the completion of steps or noting any issues encountered.

Security Compliance: Make sure the GPT is instructed to flag any security concerns it identifies based on the file's instructions, especially if it detects a deviation from best practices.

### Post-Deployment
Confirmation and Testing: After following the deployment instructions, the GPT should verify the successful deployment and perform initial tests to confirm the agent is functioning as intended.

Documentation Update: If any deviations from the instruction file were necessary during deployment, instruct the GPT to note these changes for updating the deployment documentation.