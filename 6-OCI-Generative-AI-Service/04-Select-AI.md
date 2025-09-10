# Natural Language Queries in Oracle Autonomous Database (Select AI) - Learning Notes

## Overview
This lesson introduces **Select AI** in **Oracle Autonomous Database**, demonstrating how to use **natural language queries** to analyze data. It explains the role of Select AI within the Oracle AI landscape, shows how natural language is translated into SQL queries, and highlights how these capabilities can be built into applications securely and easily using large language models.

## Key Concepts
- **Select AI**: A feature of Oracle Autonomous Database that allows querying data using natural language instead of writing SQL.
- **Natural Language Queries**: Users can ask questions in plain language without needing knowledge of table names or schema.
- **SQL Query Generation**: Select AI translates natural language into SQL queries using large language models.
- **APEX Integration**: Applications can be built in Oracle APEX to return query results interactively with charts and filters.
- **AI Profiles**: Define which large language models (OCI Gen AI, Cohere, OpenAI, Llama, etc.) and database objects (schemas, tables, views) to use.
- **Security**: Data remains within the Oracle tenancy and is not exposed to external LLM providers.
- **Future Enabled**: Ability to choose new or fine-tuned models as they become available.

## Detailed Notes  

### Oracle AI Landscape
- Oracle provides AI at every layer of the enterprise.
- This lesson focuses on how **Oracle Autonomous Database** leverages **large language models (LLMs)** for querying and analyzing data using natural language.

### What is Select AI?
- **Select AI** simplifies business insights by letting users ask questions in natural language.
- Users don’t need to know:
  - Data structure.
  - How to write SQL queries.
- The Autonomous Database manages:
  - Connecting to a large language model.
  - Engineering an optimized prompt for Oracle Database sources.
  - Delivering the result set, narrative, or SQL.

### Building Apps with Select AI
- Example: A simple **APEX app** built with Autonomous Database.
  - Query: "Top 10 streamed movies."
  - Query: "Actors in those movies."
  - Query: "Total number of movies streamed."
- Features:
  - Interactive reports with filters.
  - Data visualization as charts.
  - Results without needing table or column knowledge.

### SQL Query Generation
- Select AI shows the SQL it generates:
  - Example: `select ai showsql` displays the tables and joins.
- SQL Developer and similar tools support:
  - Writing `SELECT AI` followed by the natural language question.
  - Database processes it like any other SQL statement.
- Users can refine questions for more details.

### Large Language Models
- Different LLMs specialize in writing SQL and inferring user intent.
- Users can:
  - Review queries to validate results.
  - Use existing applications or build new ones.
- Models can be:
  - Publicly available.
  - Fine-tuned for business-specific use cases.

### Security
- Oracle ensures that:
  - Data remains inside the Oracle tenancy.
  - Data is not shared with external providers or other customers.
- Secure at every layer of processing.

### AI Profiles and Configuration
- **AI Profile** encapsulates pluggability.
- Users can:
  - Choose models (OCI Gen AI, Cohere, OpenAI, Llama).
  - Configure which schemas, tables, or views are used.
- Managed with `dbms_cloud_ai` PL/SQL package.

### Example Use Case
- Query: "Find the top customer segments for George Clooney movies."
- Workflow:
  - AI profile uses metadata and models.
  - Prompt generated from natural language.
  - SQL generated and executed.
  - Result sets returned to SQL Developer or an application.

## Important Terms
- **Select AI**: Oracle Autonomous Database feature enabling natural language queries.
- **Natural Language Queries**: Questions written in plain language to retrieve data.
- **APEX**: Oracle Application Express, used to build interactive apps.
- **SQL Developer**: Tool to query and review generated SQL.
- **AI Profile**: Configuration object defining which LLM and database objects to use.
- **dbms_cloud_ai**: PL/SQL package to configure AI profiles.
- **OCI Generative AI**: Oracle’s service for integrating LLMs securely within the tenancy.

## Summary
Select AI in Oracle Autonomous Database enables **natural language querying** of enterprise data. It:
- Translates questions into SQL queries using LLMs.
- Provides interactive results through APEX apps or SQL Developer.
- Supports pluggability through **AI profiles** for selecting LLM providers and database objects.
- Ensures **security** by keeping data within Oracle tenancy.
- Is **future enabled**, supporting new and fine-tuned models as they become available.  
This makes it simple to build AI-powered applications that unleash the creativity of generative AI while protecting enterprise data.
