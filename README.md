Rocky Chatbot 

A RAG-Based Chatbot Built with LangChain 

 

Project Overview: 

Rocky Chatbot is an intelligent conversational assistant that uses Retrieval-Augmented Generation (RAG) powered by LangChain. 
The chatbot is capable of reading information directly from specific web URLs and answering user questions based on that content. 

Unlike ordinary chatbots that rely on pre-defined data, Rocky Chatbot dynamically retrieves and processes information from the web, giving you accurate and context-aware answers. 

 

Objective: 

The main goal of this project is to: 

    Build a chatbot that can extract, process, and understand real-time data from given URLs. 

    Enable users to paste any URL of a website and ask questions related to its content. 

    Demonstrate how RAG (Retrieval + Generation) can be implemented using LangChain and LLMs (Large Language Models). 

Technical Workflow: 

1. Data Source 

Initially, the chatbot was trained on 3 URLs: 

urls = [ 

    'https://www.bbc.com/news/business-12345678', 

    'https://tribune.com.pk/story/1234567/specific-story', 

    'https://www.thenews.com.pk/print/123456-specific-news' 

] 

These URLs contain business and current-affairs related content. 
Rocky Chatbot retrieves data from these pages to provide context-based answers. 

 

2. Pipeline Steps 

    Web Page Loading: 
    LangChain’s UnstructuredURLLoader is used to fetch and clean text from each webpage. 

    Text Splitting: 
    The text is divided into small, manageable chunks using RecursiveCharacterTextSplitter. 

    Embedding Creation: 
    Each chunk is converted into a numerical representation (embedding) using a model like HuggingFaceEmbeddings. 

    Vector Store: 
    These embeddings are stored in a vector database (e.g., FAISS ) for efficient retrieval. 

    Retrieval-Augmented Generation (RAG): 
    When the user asks a question: 

    Relevant document chunks are retrieved from the vector store. 

    The LLM (e.g., ChatGroq ) generates a response using those retrieved texts as context. 

 

3. Dynamic URL Feature 

To make the chatbot more flexible, an additional feature was developed: 

Users can paste any website URL directly into the interface. 
The chatbot automatically scrapes that URL, processes its content, and allows the user to ask questions about it. 

This means Rocky Chatbot isn’t limited to predefined URLs — it can adapt to any web page, making it a universal web-based knowledge assistant. 

Example Interaction 

User: 

What is the key business update mentioned in the BBC article? 

Rocky Chatbot: 

The BBC article highlights recent market trends, emphasizing the impact of inflation on global trade and consumer spending. 

User: 

Now, I want to know what the Tribune article says about local industry growth. 

Rocky Chatbot: 

According to the Tribune article, the local industry sector has shown steady growth due to increased export demand and government incentives. 

User: 

I’ll paste a new URL — can you summarize this website? 

Rocky Chatbot: 

Sure! Please paste your link below, and I’ll fetch and summarize the key points for you. 

 

Technologies Used 

 

Component 
	

Tool / Library 

Programming Language 
	

Python 

Framework 
	

LangChain 

Model 
	

 

Vector Store 
	

              FAISS  

Web Data Loader 
	

UnstructuredURLLoader 

Embeddings 
	

HuggingFace Embeddings 

Interface 
	

Gradio (optional for UI) 

 

Results 

    Built a chatbot capable of answering questions based on live web content. 

    Enabled dynamic input of URLs for flexible content retrieval. 

    Showcased the power of RAG architecture in building intelligent conversational systems. 

 

Future Improvements 

    Add support for PDFs and YouTube video transcripts. 

    Implement conversation memory for multi-turn dialogues. 

    Deploy the chatbot as a web application with authentication. 

    Integrate summarization and sentiment analysis modules. 

 

Author 

Developed by: Arbaz Aslam 
Project Name: Rocky Chatbot 
Framework: LangChain (RAG-based Web Information Chatbot) 
