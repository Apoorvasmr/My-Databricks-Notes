# Chapter 4: Catalog Explorer UI + Structure and Foundation

## Introduction

This walkthrough introduces Catalog Explorer, the primary workspace interface for working with Unity Catalog.

## Catalog and the three-level namespace

Select **Catalog** in the navigation sidebar to open Catalog Explorer. Databricks organizes data assets using a three-level namespace. When referring to an asset in code, use this format: **catalog.schema.data-object**.

The catalog is the highest-level container. Within it, schemas group related objects. A schema can contain tables, volumes, models, and stored functions.

## Browse Catalog Explorer

Catalog Explorer uses a tree navigation to browse catalogs, their schemas, and the data assets in those schemas. When a schema contains different kinds of assets, the tree groups them by type.

Schemas may be called databases in other systems. In Databricks, however, a schema can hold more than datasets. Catalogs include at least two standard schemas:

- **default** — An empty schema provided as a starting point when the catalog is created.
- **information_schema** — Contains metadata views about objects in the catalog.

## Catalog tabs

The Catalog view includes these tabs:

- **Overview** — Shows the catalog description and its schemas. AI can help generate a detailed catalog description.
- **Details** — Displays technical information about the catalog.
- **Permissions** — Lets you grant or revoke catalog-level permissions.
- **Policies** — Lets you apply row or column filters at the catalog level. These policies are inherited by schemas and data objects beneath the catalog.
- **Workspaces** — Lists the workspaces that include this catalog.

## Schema tabs

The Schema view includes these tabs:

- **Overview** — Shows the schema description and its tables, volumes, models, and functions.
- **Details** — Displays technical information about the schema.
- **Permissions** — Lets you grant or revoke schema-level permissions.
- **Policies** — Lets you set row or column filters at the schema level. These filters are inherited by the data objects in the schema.

## Table tabs

The Table view includes these tabs:

- **Overview** — Shows the table description and its columns. AI can help create descriptions and column comments, and you can add tags to columns.
- **Sample Data** — Previews table contents with a simple `SELECT * FROM table_name` query.
- **Details** — Shows technical table metadata, such as the owner, data type, and whether the table is managed.
- **Permissions** — Lets you grant or revoke permissions on the table.
- **Policies** — Lets you configure table-level row or column filters that control or mask data according to a user's or group's permissions.
- **History** — Provides an audit log of changes made to the table.
- **Lineage** — Shows upstream and downstream dependencies for the table, in either table or graph form.
- **Insights** — Summarizes usage, including where the table is used most and who accesses it most often.
- **Quality** — When quality monitoring is enabled, displays freshness and completeness checks, along with information about dataset anomalies.

## Settings Permissions

Use the **Permissions** tab to grant or revoke access to data assets such as catalogs, schemas, and tables. The interface provides a point-and-select way to manage these permissions.

For a user, group, or other principal to view, use, or edit an asset, they also need the required **USE** permissions on its parent schema and catalog. The interface warns you about these inherited permission requirements when you grant access.

## Conclusion

In this lesson you learned how to:

- Open Catalog Explorer from the Databricks Workspace UI.
- Recognize the three-level namespace used to reference data objects.
- Navigate the catalog, schema, and table views and their tabs.
- Manage data asset permissions in Catalog Explorer.
- Recognize when access also requires permissions on parent catalogs or schemas.
