---
#https://www.notion.so/n8n/Frontmatter-432c2b8dff1f43d4b1c8d20075510fe4
title: Oracle Database node documentation
description: Learn how to use the Oracle Database node in n8n. Follow technical documentation to integrate Oracle Database node into your workflows.
contentType: [integration, reference]
priority: high
---

# Oracle Database node

Use the Oracle Database node to automate work in Oracle Database, and integrate Oracle Database with other applications. n8n has built-in support for a wide range of Oracle Database features, including executing an SQL query, as well as inserting, and updating rows in a database.

On this page, you'll find a list of operations the Oracle Database node supports and links to more resources.

/// note | Credentials
Refer to [Oracle Database credentials](/integrations/builtin/credentials/oracledb.md) for guidance on setting up authentication. 
///

--8<-- "_snippets/integrations/builtin/app-nodes/ai-tools.md"

## Operations

* Delete
* Execute SQL
* Insert
* Insert or Update
* Select
* Update

## Templates and examples

<!-- see https://www.notion.so/n8n/Pull-in-templates-for-the-integrations-pages-37c716837b804d30a33b47475f6e3780 -->
[[ templatesWidget(page.title, 'oracledb') ]]

## Related resources

Refer to [APIs documentation](https://docs.oracle.com/en/database/oracle/oracle-database/23/sqlrf/index.html) for more information about the service.

## Use query parameters

When creating a query to run on a Oracle database, you can use the **Bind Variable Placeholder Values** field in the **Options** section to load data into the query. n8n sanitizes data in query parameters, which prevents SQL injection.

For example, you want to find a person by their email address. Given the following input data:

```js
[
    {
        "FRUIT_ID": 1,
        "FRUIT_NAME": "Apple",
        "COLOR": "Red" 
    },
    {
        "FRUIT_ID": 2,
        "FRUIT_NAME": "Banana",
        "COLOR": "Yellow"
    }
]
```

You can write a query like:

```sql
SELECT * FROM FRUITS WHERE COLOR = :col
```

Then in **Bind Variable Placeholder Values**, provide the field values to use. You can provide fixed values or expressions. For this example, use expressions so the node can pull the email address from each input item in turn:

```js
// fruits is an example table name
users, {{ $json.color }} 
```

## Common issues

For common errors or issues and suggested resolution steps, refer to [Common issues](/integrations/builtin/app-nodes/n8n-nodes-base.oracledb/common-issues.md).
