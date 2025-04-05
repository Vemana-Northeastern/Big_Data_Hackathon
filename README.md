# HACKATHON : SOCIAL DETERMINANTS OF HEALTH

**Project Description**

In this hackathon project, we present a multi-agent research assistant focused on analyzing stress and its contributing social determinants—such as income level, employment status, education, and healthcare access. The system is designed to help hospital administrators, healthcare professionals, and policymakers generate real-time, data-driven reports that explore how stress levels vary across different populations and what actions can be taken to improve well-being.
As the U.S. healthcare system grapples with rising costs, staffing shortages, and the growing burden of mental health challenges, there is a critical need for tools that combine multiple data sources to inform better decisions.

**Live Links**

Streamlit Application: http://192.241.155.93:8501/
FastAPI: http://192.241.155.93:8000/docs
CodeLabs link:


# Technologies Used
Storage and Cloud: Snowflake, Pinecone, s3

Frontend Application: Streamlit

Backend: FastAPI

Agent Orchestration: LangGraph

Real-Time Data Extraction: Tavily

Document Retrieval & Embedding: LangChain + OpenAI

Containerization & Deployment: Docker

Secrets Management: .env, python-dotenv

# PROBLEM STATEMENT
The task at hand involves analyzing large volumes of structured and unstructured health data to uncover patterns in stress across different population groups. The challenge is to integrate stress-related indicators such as income, employment, and sleep with real-time trends and policy documents. This requires an intelligent, scalable system capable of extracting, processing, and presenting insights from multiple sources. Efficient agent orchestration and tool integration are essential to ensure accurate, timely, and actionable stress intelligence for healthcare decision-making.

# PROOF OF CONCEPT
Our application is a platform designed to analyze and visualize stress-related insights by processing structured, unstructured, and real-time data. It can be broken down into 3 stages:

**Structured Data Processing:**
Snowflake was chosen as the central data warehouse for storing and querying health indicators such as stress scores, income levels, employment status, and sleep duration. The platform uses optimized SQL queries to aggregate and compare stress metrics across demographics and regions, enabling high-performance visualization and reporting.

**Unstructured Data Retrieval (RAG):**
 Pinecone is used to store vectorized embeddings of healthcare research papers, mental health policy documents, and social determinant frameworks. LangChain-powered RAG agents retrieve the most relevant context based on the user's stress-related query, allowing for rich, contextualized insights from unstructured PDFs.

**Real-Time Insights (Web Search):**
 Tavily APIs are used to fetch live news articles, government programs, and ongoing mental health initiatives related to stress. This allows the final report to include up-to-date context, public response, and evolving healthcare strategies.

** Automation, Application and Deployment:**
LangGraph handles orchestration between agents to ensure clean data flow and dependency resolution. FastAPI serves as the high-performance backend managing user queries and coordinating agents. Streamlit offers an interactive and simple frontend for users to submit queries, select agent types, and download reports. The complete system is Dockerized and deployed on DigitalOcean, ensuring scalability and reliability.

**Challenges and Optimizations:**
One of the challenges was efficiently filtering large datasets on stress by income, employment, and geography. To solve this, parameterized SQL queries were used with backend filters based on user inputs. RAG performance was optimized by chunking PDF reports intelligently and embedding them with metadata such as topic and year. Web search results were post-processed using ranking logic to eliminate irrelevant or low-quality content.

**Architecture Diagram**

![Editor _ Mermaid Chart-2025-04-05-151537](https://github.com/user-attachments/assets/7a11dc8c-cb20-48ed-ae01-505686ccacea)


# APPLICATION WORKFLOW 
The Stress Analytics Research Assistant follows a multi-stage workflow designed to process, analyze, and summarize stress-related data across structured, unstructured, and real-time sources.

**1. User Query Input**
* The user enters a stress-related question (e.g., “How is stress distributed across different income groups in California?”) through the Streamlit frontend.

* Users can choose to activate one or more agents: Snowflake, RAG, and Web Search.

**2. Agent Orchestration (LangGraph)**
* The query is passed to a LangGraph-based backend, which routes it through the selected agents in parallel:

* Snowflake Agent: Executes parameterized SQL queries on structured datasets containing stress, income, employment, and sleep-related indicators.

* RAG Agent: Performs vector-based retrieval from embedded documents such as mental health policy PDFs, returning relevant passages and summaries.

* Web Search Agent: Uses or Tavily to retrieve real-time data on stress management, policy changes, or public health trends.

**3. Data Aggregation**
* Outputs from all agents are collected, organized, and converted into:

* Visualisation (e.g., line charts, bar graphs, box plots)

* Text summaries of retrieved content

* Live data from web sources

**4. Report Compilation**
* All data is compiled into a Markdown-based template, which includes:

* Overview of findings

* Agent-wise contributions

* Recommended frameworks and actionable insights

**5. Output Display**
* Users view the results interactively in the Streamlit UI
  
# REFERENCES
The following resources, datasets, and tools were used to build the Social Determinants of Health

* Snowflake Documentation
 https://docs.snowflake.com
 Used for storing and querying structured health datasets (stress, income, employment, sleep).


* LangGraph (LangChain)
 https://github.com/langchain-ai/langgraph
 Framework used to orchestrate the multi-agent flow between Snowflake, RAG, and Web Search agents.


* Pinecone Vector Database
 https://docs.pinecone.io
 Used to store and retrieve embedded chunks of mental health reports and stress-related documents.


* Streamlit
 https://docs.streamlit.io
 Used for building an interactive, lightweight frontend for user query input and report visualization.


* FastAPI
 https://fastapi.tiangolo.com
 Backend framework used to handle query routing, agent calls, and PDF generation.


* Tavily API
 https://serpapi.com / https://www.tavily.com
 Real-time search APIs used for extracting the latest news, trends, and health interventions related to stress.

* SDOH Data
 Primary data source for stress-related indicators used in the Snowflake database.

# DISCLOSURES
**Contributions**

Vemana Anil Kumar - 80%

Ashwin Badamikar - 10%

Madhura Adadande - 10%

WE ATTEST THAT WE HAVEN’T USED ANY OTHER STUDENTS’ WORK IN OUR ASSIGNMENT AND ABIDE BY THE POLICIES LISTED IN THE STUDENT HANDBOOK

**AI USAGE DISCLOSURE**

For this project, we used AI tools like ChatGPT, DeepSeek, and Claude to enhance various aspects of development debugging code, optimizing SQL queries, and generating explanations for complex concepts. These tools were leveraged to improve clarity, efficiency, and accuracy in our work, but all final decisions, implementations, and analyses were conducted by us.


