# Using Prompt Chaining to Automatically Generate Articles

## Objective
This project scrapes the web and uses GPT-3 + LangChain to automatically parse and generate new articles.

## Deployment
The application is deployed on a Flask server, a lightweight WSGI web application framework. This setup provides a balance between ease of use and powerful functionality, suitable for both simple and complex applications.

## Technologies Used
- **GPT-3.5 Turbo**: For advanced natural language processing.
- **Langchain**: Enhances large language model capabilities.
- **BeautifulSoup & Requests**: Python libraries for web scraping.
- **dotenv**: Manages environment variables for secure configuration.

## How It Works
1. **Web Scraping**: Scrape the latest tech funding news articles from a specified site, storing in 'Scraped Articles'.
2. **Article Processing**: `alpha.ipynb` processes this information for content generation.
3. **Multi-Shot Prompting**: This method is used for maintaining output quality.
4. **Model Flexibility**: Adaptable for use with various language models.

## Possible Future Extensions
- **Dynamic Information Retrieval with Retrieval-Augmented Generation**: By incorporating RAG, the project can dynamically access and integrate external information. This would require combining a language model with an information retrieval system, which fetches the most relevant and up-to-date data from the Vector Database or other external sources.
- **Automated Quality Control**: Develop a system to automatically check the factual accuracy, grammar, and style of generated articles - potentially with 3rd party data sources like Pitchbook or Crunchbase. This will ensure consistently high-quality output and reduce the need for manual reviews.
- **Multi-Language Support**: Extend the system to generate articles in multiple languages. This will cater to a broader, international audience and increase the project's reach and applicability.

## Implementation Details
- Utilizes Python's BeautifulSoup for web scraping and requests for web page fetching.
- Employs Langchain's `ChatOpenAI` for prompt-based GPT-3.5 Turbo interactions.
- Methods to filter data, convert HTML to text, and manage JSON files are implemented.

## Workflow
1. Scrape articles.
2. Convert HTML content to text.
3. Process content with GPT-3.5 Turbo.
4. Use conversation chains for checks and context maintenance.
5. Refine the article list and compile the final text file.

## Usage
Ensure all dependencies are installed and environment variables are set. Run `alpha.ipynb` to initiate the process. Follow the notebook's steps for complete article generation.

## Conclusion
This project demonstrates the integration of LLM models and web scraping for automated, relevant, and current article generation. Its design allows for easy adaptation and scalability.
