How this works:

1. Launch the web scraper, which scrapes the latest tech funding news articles from {Site}
2. The web scraper will search for and ingest all latest tech funding news, before outputting them to the folder Scraped Articles
3. Currently, glue.ipynb is not implemented yet as I’m unsure which environment this would be hosted in. It would be easy to write some python code to run alpha.ipynb for each file in the scraped articles folder
4. alpha.ipynb contains the main engine, which extracts information from the funding articles before creating a new article, which should always include a quote from Quest Ventures if it is listed as an investor in the article

This is a multi-shot prompt engine. Additional shots are required to maintain / ensure the quality of the output. Currently, the engine runs on GPT 3.5 Turbo - but there is no reason why it cannot work with other models, including Claude, Bard, or Llama. Instead of using the OpenAI API directly, Langchain is used to allow us to easily swap out the LLM model for another. 

All notebooks should be converted into Python code prior to usage. Python has multiple libraries that allow for the easy sending of e-mails. I recommend that this be the primary method of interaction with the engine.

You may also consider plugging the engine atop Dify (dify.ai), which would provide you with an easy to use web UX.

All prompts can be found in the folder. Embeddings were not used as they appeared to reduce the quality of the generated articles.