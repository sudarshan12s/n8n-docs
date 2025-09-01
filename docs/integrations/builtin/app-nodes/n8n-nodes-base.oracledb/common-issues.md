---
#https://www.notion.so/n8n/Frontmatter-432c2b8dff1f43d4b1c8d20075510fe4
title: Oracle Database node common issues
description: Documentation for common issues and questions in the Oracle Database node in n8n, a workflow automation platform. Includes details of the issue and suggested solutions.
contentType: [integration, reference]
priority: high
---

# Oracle Database node common issues

Here are some common errors and issues with the [Oracle Database node](/integrations/builtin/app-nodes/n8n-nodes-base.oracledb/index.md) and steps to resolve or troubleshoot them.

## Update rows by composite key

**Statement Batching** (Single) value in the Oracle Database node option can only be used when all processed rows belong to the same schema and table.
