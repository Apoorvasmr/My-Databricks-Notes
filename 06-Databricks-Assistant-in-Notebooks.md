# Chapter 6: Databricks Assistant in Notebooks

## Introduction

This walkthrough covers using Databricks Assistant in notebooks to generate code, write SQL, and investigate errors.

## Locating Assistant in Notebooks

You can open Assistant in a notebook from several places:

- Select the **Assistant icon** in the right sidebar to show the chat panel beside your notebook.
- Select the **Assistant button** in the top navigation bar to open the same side panel.
- Select the inline **Assistant** button between cells to work with Assistant in a new cell. The chat panel can remain open as you write and run code.

## Writing Python with Assistant

Describe the task in plain language to ask Assistant for Python code. You can insert the returned snippet into a new cell, or accept and run it in one step.

For example, ask it to “compute the sum of integers 1 through 10.” Assistant can return a short Python snippet that you can run and check.

## Writing SQL with Assistant

Assistant can draft SQL queries for your existing tables. If the notebook's default language is Python, it may return PySpark SQL unless you name the language you want. For clearer results, specify the language in your prompt, for example: “Use SQL to select the first 10 rows from my table.” Check that the generated code is in the appropriate cell type.

## Debugging with Assistant

If **Assistant Quick Fix** is enabled, a failed cell may display **Diagnose Error**. Select it to send the failing code and error message to Assistant, which opens in the side panel. Assistant will analyze the issue, explain a possible cause, and suggest a fix.

You can run the suggested code to test it or edit the suggestion with additional context. A fix may reveal another issue, so further diagnosis may be needed to resolve the error fully.

## Assistant Best Practices

Keep these practices in mind when using Assistant:

- Review generated code and its results before using them in production or sharing them.
- Make prompts specific. Include relevant table and column names, along with the programming or query language you want.
- If an error remains, compare Assistant's explanation with the full stack trace. Together, they may help identify an incorrect or missing table, schema, or permission.
- Assistant is available across the platform, so look for it as a development aid in other areas too.

## Conclusion

In this lesson you learned how to:

- Open and use Assistant from several places in a notebook.
- Request Python and SQL code with natural-language prompts.
- Use **Diagnose Error** to investigate failed cells.
- Write specific prompts and review generated code carefully.
