# Chapter 5: Create a Notebook and Explore the Notebook UI

## Introduction

This walkthrough covers creating and navigating a Databricks notebook, understanding its layout, and using cells, Markdown, Focus mode, and visualizations.

## Create and Name a notebook

Create a notebook in any of these ways:

- In the Workspace browser, right-click the destination folder and choose **Create** > **Notebook**.
- Open the destination folder, select **Create** at the upper right, and choose **Notebook**.
- Select **+ New** in the navigation sidebar and choose **Notebook**. This places the notebook in your default home folder.

New notebooks start with a temporary name. Select the title at the top to rename it. Use the compute selector in the upper right to attach a cluster or SQL warehouse. In Free Edition, serverless compute is the available option and starts automatically when you run a cell.

## Working with notebook cells

Use **+ Code**, **+ Text**, or **Assistant** between cells to add a cell. Run a code cell with its **Run** button or press **Shift + Enter**.

The notebook's default language appears near the top, next to Help. Databricks notebooks support **Python** and **SQL**. New cells use the default language, but you can choose a different language for an individual cell from its upper-right dropdown. The language switch adds a magic command such as `%py`, `%sql`, or `%md` at the beginning of the cell.

If notebook tabs are enabled in Settings, each notebook opens in a separate tab. This lets you switch between notebooks without returning to the Workspace browser; drag tabs to rearrange them.

## Markdown in notebooks

Markdown cells let you document work with headings, lists, links, and tables. Add one with **+ Text**, select Markdown in the cell language menu, or start the cell with `%md`.

Double-click a Markdown cell to edit it. Choose **Show Preview** to see the rendered version alongside the text. Markdown headings are listed in the notebook's **Table of Contents** panel, where selecting a heading jumps to that section.

## Left and Right Sidebar options

The notebook's left sidebar provides:

- **Table of Contents** — Headings generated from the notebook's Markdown.
- **Folder icon** — A side-panel Workspace browser for locating notebooks and other workspace assets.
- **Catalog icon** — A compact Catalog Explorer for browsing catalogs, schemas, tables, and volumes, and inserting references into code.

The right sidebar offers shortcuts to **Comments**, **MLflow experiments**, **Version history**, **Variables**, **Environment** (compute-related), **Information**, and **Assistant**. These tools support collaboration, experiment tracking, and inspection of notebook details.

## Executing code and viewing outputs

Cell results appear below the cell after it runs. For a cell that uses a language other than the notebook default, make sure the appropriate magic command is present so it executes in that language.

Run a single cell with its **Run** button or **Shift + Enter**. Choose **Run All** in the toolbar to execute the notebook from top to bottom.

## Focus mode

**Focus mode** enlarges a cell and its results to use the notebook view, minimizing surrounding content. Select the Focus mode icon in the cell's upper-right corner to enter or leave this view.

Comments, Assistant, and the terminal panel remain available in Focus mode. Use the left and right arrows at the top of the window to move between cells without exiting it.

## Visualizations in Notebooks

For tabular cell output, select the **+** beside the results to add a visualization alongside the table. Choose a chart type—such as bar, scatter, or line—set the X and Y values, and save it. You can then switch between the table and visualization within the cell.

## Conclusion

In this lesson you learned how to:

- Create and rename a notebook, then attach compute.
- Add and run cells using supported languages.
- Document a notebook with Markdown and navigate its headings.
- Use the notebook's left and right sidebars.
- Focus on an individual cell and its output.
- Create visualizations from tabular cell results.
