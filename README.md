# AI Agent Team for Financial Data and Web Search

This project is a Python-based application that leverages the `phi` library to create and manage a team of AI agents capable of performing specific tasks, such as retrieving financial data and searching the web. The agents are powered by advanced language models (like Groq's `llama-3.3-70b-versatile` or OpenAI's `gpt-4o`) and are equipped with specialized tools to accomplish their roles.

---

## Key Components

### 1. Agents
- **Web Agent**: 
  - Searches the web using the `DuckDuckGo` tool.
  - Always includes sources in its responses.
  - Shows tool calls and formats output in Markdown.
  
- **Finance Agent**:
  - Retrieves financial data using the `YFinanceTools` tool.
  - Fetches stock prices, analyst recommendations, and company information.
  - Displays data in tables and formats output in Markdown.

- **Agent Team**:
  - A collaborative team of agents (Web Agent and Finance Agent).
  - Handles complex tasks with shared instructions (e.g., include sources, use tables for data display).

### 2. Tools
- **DuckDuckGo**: Used by the Web Agent for performing web searches.
- **YFinanceTools**: Used by the Finance Agent for fetching financial data.

### 3. Language Models
- The agents use either **Groq's `llama-3.3-70b-versatile`** or **OpenAI's `gpt-4o`** as their underlying language models.

### 4. Output Handling
- Captures the output of the agents' responses using `io.StringIO`.
- Redirects the standard output (`sys.stdout`) to a buffer.
- Saves the output to a text file (`output.txt`).

### 5. Environment Configuration
- Uses `dotenv` to load environment variables (e.g., API keys).

---

## Workflow

1. The `agent_team` is tasked with summarizing analyst recommendations and sharing the latest news for a specific stock (e.g., TSLA).
2. The Web Agent retrieves the latest news, while the Finance Agent fetches financial data and analyst recommendations.
3. The output is captured, formatted, and saved to a text file (`output.txt`).

---

## Use Case

This project is ideal for users who need to automate the retrieval of financial data and web-based information. For example:
- **Investors**: Get quick summaries of analyst recommendations and news for specific stocks.
- **Researchers**: Gather and organize data from the web and financial markets.

---

## Example Output

The output saved in `output.txt` might include:
- A table summarizing analyst recommendations for the stock (e.g., TSLA).
- A list of the latest news articles related to the stock, with sources included.

---

## Scalability

The project can be extended by:
- Adding more agents with specialized tools.
- Integrating additional data sources.
- Adapting it for other domains, such as market research, competitive analysis, or general-purpose information retrieval.

---

## Requirements

- Python 3.x
- `phi` library
- `dotenv` library
- API keys for Groq or OpenAI (if using their models)
