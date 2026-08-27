# hands-on-lab-neo4j-and-microsoft-customer-360

Neo4j is the [leading graph database](https://db-engines.com/en/ranking/graph+dbms) vendor.  We’ve worked closely with Microsoft engineering for years.  Our SaaS database, Neo4j Aura, is offered as a managed service on Azure.  This is available through the [Azure Marketplace](https://marketplace.microsoft.com/en-us/product/neo4j.neo4j-aura).

LLMs are great at language, but they struggle with logic across disconnected data. In this workshop, we’re using Neo4j and Microsoft Foundry to provide the source of truth that agents need. You’ll build a pipeline that transforms raw Customer 360 data into a structured knowledge graph, giving your AI the context it needs to actually be useful.

In this session, data scientists and engineers will build a functional GraphRAG pipeline within a live Azure environment. Moving beyond high-level theory, you will deploy Neo4j Aura and integrate it with Microsoft Foundry to implement a complete, end-to-end architecture for reasoning over connected data.

The Data & Workflow
We’ll use a Customer 360 dataset—specifically the orders, clickstream events, devices, products, and support tickets of these customers as our primary dataset. This data is ideal for demonstrating how to map complex ownership structures and many-to-many relationships.

During this session, you will:
• Streamline Ingestion: Use Cypher to parse and load data from Azure Blob Storage into Neo4j.
• Model Relationships: Use Cypher and the Neo4j Browser to map connections between thousands of customers orders and their clickstream events.
• Orchestrate Agents: Layer a Microsoft Foundry AI agent over the graph to enable natural language reasoning across the connected customer data.

Practical Application
For those in the customer satisfaction marketspace, this architecture provides a blueprint for algorithmic product recommendation, user behavioral patterns, and support ticket satisfaction. If you work in another industry, this session will still be useful for learning how to build agentic AI pipelines with Neo4j and Microsoft Foundry.
## Venue

These workshops are organized onsite in a Microsoft office.

## Duration

3 hours.

## Prerequisites

You'll need a laptop with a web browser.  Your browser will need to be able to access the Microsoft Azure Portal and the Neo4j Aura Console running on Microsoft Azure.  If your laptop has a firewall you can't control, you may want to bring your personal laptop.

## Agenda

* Introductions
* Lecture - Introduction to Neo4j (30 min)
* Lab 1: Deploy & Connect to Neo4j (10 min)
* Lab 2: Load Data (10 min)
* Lab 3: Query Data (15 min)
* Lab 4: Aura Agent (10 min)
* Lecture - Foundry (30 min)
* Connect to Cloud Environment (15 min)
* Lab 5: Deploy Foundry Agent (15 min)
* Lab 6: Use Foundry Agent (15 min)
* Break (10 min)
* Lab 7: Visualize Data - Bloom (10 min)
* Lab 8: Visualize Data - Dashboards (10 min)