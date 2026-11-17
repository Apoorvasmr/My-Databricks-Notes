# Chapter 7: Explore Catalogs and Grant Permissions in Notebooks

## Introduction

This walkthrough covers using SQL in a notebook to work with Unity Catalog. You’ll check the active context, inspect schemas, tables, and volumes, and grant permissions with SQL.

## Check current and set catalog and schema

Run `SELECT current_catalog(), current_schema();` to see which catalog and schema the notebook is currently using. This is helpful in longer notebooks, where it can be easy to lose track of the active context.

Use **USE CATALOG** and **USE SCHEMA** statements to change the context. Knowing the current catalog and schema helps you decide whether to fully qualify a table name or use the current context's defaults.

## Explore the schema

To inspect schema configuration in SQL, run `DESCRIBE SCHEMA EXTENDED current_schema();`. The output can include the schema owner, storage location, comments, and custom properties.

## Explore tables and views

Run `SHOW TABLES;` to list tables and views in the current schema. The results include names, types, and comments. Since views appear alongside tables, consider the object type when exploring dependencies or deciding whether an object can be edited.

## Explore volumes

Run `SHOW VOLUMES;` to list logical volumes registered in the current catalog and schema, including their names and storage locations. You can also use a command to list files at a particular volume path and inspect which raw files are available for ingestion or processing.

## Grant permissions in a Notebook

Unity Catalog permissions can be managed from a notebook with ANSI-style `GRANT` statements. For example, a SQL statement can grant `SELECT` on a table to all account users.

Permissions follow a hierarchy: to query a table, users also need `USE CATALOG` and `USE SCHEMA` privileges on its parent catalog and schema. Check grants with `SHOW GRANTS` or review the **Permissions** tab in Catalog Explorer. SQL is useful for automating permission updates, while Catalog Explorer provides a visual way to confirm them.

## Conclusion

In this lesson you learned how to:

- Check and change the notebook's current catalog and schema.
- Explore Unity Catalog schemas, tables, views, and volumes with SQL.
- Grant data asset permissions programmatically with `GRANT` statements.
- Verify permissions in SQL or Catalog Explorer.
- Describe Unity Catalog's hierarchical privileges and parent permission requirements.
