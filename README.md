# 📚 Virtual Research Assistant

A powerful AI-powered research assistant that helps you discover, summarize, and analyze academic papers from ArXiv and Google Scholar. Built with Streamlit and powered by Groq's language models.

## ✨ Features

- **Smart Paper Discovery**: Search and retrieve research papers from ArXiv and Google Scholar
- **AI-Powered Summarization**: Get concise, relevant summaries of complex research papers
- **Pros & Cons Analysis**: Automatically analyze advantages and disadvantages of each paper
- **Interactive Web Interface**: Clean, user-friendly Streamlit interface
- **Multi-Agent System**: Specialized AI agents for different research tasks

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- Groq API key ([Get one here](https://console.groq.com/))

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd virtual-research-assistant
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   
   Edit `.env` and add your Groq API key:
   ```
   GROQ_API_KEY=your_actual_groq_api_key_here
   ```

### Running the Application

```bash
streamlit run app.py
```

The application will open in your browser at `http://localhost:8501`

## 🎯 How to Use

1. **Enter a Research Topic**: Type your research query in the input field
2. **Click Search**: The system will fetch relevant papers from ArXiv
3. **Review Results**: Get AI-generated summaries and analysis for each paper
4. **Access Papers**: Click the provided links to read the full papers

## 🏗️ Project Structure

```
virtual-research-assistant/
├── app.py              # Main Streamlit application
├── agents.py           # AI agent definitions and logic
├── data_loader.py      # Data fetching from ArXiv and Google Scholar
├── requirements.txt    # Python dependencies
├── .env.example       # Environment variables template
├── .env              # Your actual environment variables (not in git)
└── README.md         # This file
```

## 🤖 AI Agents

The system uses specialized AI agents powered by Groq's `deepseek-r1-distill-qwen-32b` model:

- **Summarizer Agent**: Creates concise summaries of research papers
- **Analysis Agent**: Identifies advantages and disadvantages of each paper

## 🔧 Configuration

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `GROQ_API_KEY` | Your Groq API key for AI model access | Yes |

### Model Configuration

The application uses the `deepseek-r1-distill-qwen-32b` model from Groq. You can modify the model in `agents.py` if needed.

## 📋 Dependencies

- **streamlit**: Web interface framework
- **autogen**: Multi-agent conversation framework
- **scholarly**: Google Scholar API wrapper
- **python-dotenv**: Environment variable management
- **streamlit-chat**: Enhanced chat components
- **requests**: HTTP library for ArXiv API
- **xml.etree.ElementTree**: XML parsing for ArXiv responses

## 🛠️ Development

### Adding New Features

1. **New Data Sources**: Extend `DataLoader` class in `data_loader.py`
2. **New AI Agents**: Add agents in `agents.py` with specific system messages
3. **UI Improvements**: Modify the Streamlit interface in `app.py`

### Code Structure

- `ResearchAgents`: Manages AI agents for summarization and analysis
- `DataLoader`: Handles data fetching from external APIs
- Main app: Orchestrates the workflow and UI

## 🚨 Security Notes

- Never commit your `.env` file with actual API keys
- The `.env` file is excluded from git via `.gitignore`
- Use the `.env.example` template for sharing configuration structure

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🆘 Troubleshooting

### Common Issues

**"GROQ_API_KEY is missing" error**
- Make sure you've created a `.env` file with your actual API key
- Verify the API key is valid and active

**No papers found**
- Try broader or different search terms
- Check your internet connection
- Verify ArXiv API is accessible

**Agent responses are empty**
- Check your Groq API key and quota
- Verify the model name is correct in `agents.py`

## 📞 Support

If you encounter any issues or have questions, please:
1. Check the troubleshooting section above
2. Search existing issues in the repository
3. Create a new issue with detailed information about your problem

---

Made with ❤️ for researchers and academics worldwide