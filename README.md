### Local Vector database, Langchain, Embedding and Generative AI LLM example ###

This example demonstrates the following concepts for generative AI

1. Use propriertary documents. These documents can be downloaded using API on periodic basis. For example, here I have a few 10Ks from the companies. These are released by the company every year. We can run a cron job or a downloader from SEC.gov site to download these documents periodically

2. These documents are then chunked and embedding is generated. This example is using GooglePalm to generate embeddings. It is using the default setting for search (similarity) and default setting for the similarity. There are various options on how to generate these embeddings. Please refer to the documentation. You can use cosine, L1, L2 etc. similarities

3. These embeddings are saved locally on chroma vector database locally. The advantage of doing this is that we don't have to send the whole text every time. We can get the relevant documents from the vector database before sending the query to the LLM

4. Here langchain is used to create the chain and send the query to the LLM. The response is then captured and shown to the user. This can be easily implemented either as a web page or a loop where we wait for the question prompt from the user



