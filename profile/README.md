# Moorcheh - Revolutionary Information-Theoretical Search Engine for Enterprise AI Applications

[comment]: <> (Add GIF or video here)

 ---
 <p align="center"><b>Upload ● Search</b></p>
 ---
 
 <p align="center">
   <a href="https://www.npmjs.com/package/moorcheh-chat-boilerplate">
     <img src="https://img.shields.io/npm/dt/moorcheh-chat-boilerplate?style=flat-square" alt="npm downloads"/>
   </a>
   <a href="https://pepy.tech/project/moorcheh-sdk">
     <img src="https://static.pepy.tech/personalized-badge/moorcheh-sdk?period=total&units=international_system&left_color=grey&right_color=blue&left_text=Downloads" alt="Downloads"/>
   </a>
 </p>
 
 <p align="center">
   <a href="https://www.linkedin.com/company/moorcheh-ai">
     <img src="https://img.shields.io/badge/Follow_us_on_LinkedIn-0077B5?style=for-the-badge&logo=LinkedIn&logoColor=white" alt="Follow us on LinkedIn"/>
   </a>
   <a href="https://x.com/moorcheh_ai">
     <img src="https://img.shields.io/badge/Follow_us_on_X-000000?style=for-the-badge&logo=x&logoColor=white" alt="Follow us on X"/>
   </a>
 </p>
 
 <p align="center">
   <picture>
     <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/moorcheh-ai/moorcheh-boilerplate/main/template/public/moorcheh-logo-dark.svg">
     <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/moorcheh-ai/moorcheh-boilerplate/main/template/public/moorcheh-logo-light.svg">
     <img width="250px" alt="Moorcheh Logo" src="https://raw.githubusercontent.com/moorcheh-ai/moorcheh-boilerplate/main/template/public/moorcheh-logo-light.svg">
   </picture>
 </p>
 
 ---
 
 ### Repositories
 
 <p align="center">
   <a href="https://github.com/moorcheh-ai/moorcheh-python-sdk">
     <img src="https://github-readme-stats.vercel.app/api/pin/?username=moorcheh-ai&repo=moorcheh-python-sdk&theme=dark" alt="moorcheh-python-sdk"/>
   </a>
   <a href="https://github.com/moorcheh-ai/moorcheh-boilerplate">
     <img src="https://github-readme-stats.vercel.app/api/pin/?username=moorcheh-ai&repo=moorcheh-boilerplate&theme=dark" alt="moorcheh-boilerplate"/>
   </a>
   <a href="https://github.com/moorcheh-ai/moorcheh-mcp">
     <img src="https://github-readme-stats.vercel.app/api/pin/?username=moorcheh-ai&repo=moorcheh-mcp&theme=dark" alt="moorcheh-mcp"/>
   </a>
   <a href="https://github.com/moorcheh-ai/n8n-nodes-moorcheh">
     <img src="https://github-readme-stats.vercel.app/api/pin/?username=moorcheh-ai&repo=n8n-nodes-moorcheh&theme=dark" alt="n8n-nodes-moorcheh"/>
   </a>
 </p>
 
 ---
 
 ### Use Cases
 
 - **[Analyzing Codebases with Firecrawl and LlamaIndex](https://github.com/moorcheh-ai/moorcheh-examples/tree/main/AnalyzingCodebases_WithFirecrawlAndLlamaIndex)**
 
 ---
 
 ### Quick Start Example
 
 ```python
 import os
 from moorcheh_sdk import MoorchehClient
 
 # Initialize client
 client = MoorchehClient(api_key=os.getenv("MOORCHEH_API_KEY"))
 
 # Create namespace and upload documents
 client.create_namespace("my-rag", "text")
 client.upload_documents("my-rag", [
     {"id": "doc1", "text": "Your content...", "metadata": {}}
 ])
 
 # Get AI-powered answers
 answer = client.get_generative_answer(
     namespace="my-rag",
     query="Your question here"
 )
 print(answer["answer"])
 ```
 
 ---
 
 **Transform your search. Elevate your AI. Choose Moorcheh.ai.**
 
 *Built for developers, trusted by enterprises.*
