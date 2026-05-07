# AI Support Ticket Classifier

A multi-agent orchestration system that automatically classifies and routes support tickets using coordinated autonomous agents. This project leverages agent-based architecture with LangGraph to process and categorize support requests intelligently.

[![API Deployed on Render](https://img.shields.io/badge/API-Render-46E3B7?logo=render&logoColor=white)](https://ai-support-ticket-classifier.onrender.com/)

&nbsp;

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Agent System](#agent-system)
- [Configuration](#configuration)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

The AI Support Ticket Classifier is a sophisticated multi-agent system designed to automate the process of analyzing, classifying, and routing support tickets. Multiple autonomous agents work together through LangGraph to provide intelligent ticket management, ensuring efficient handling and appropriate escalation.

## ✨ Features

- **Multi-Agent Architecture**: Coordinated autonomous agents for specialized ticket processing
- **Intelligent Classification**: Advanced ticket categorization using agent collaboration
- **Priority Assessment**: Automatic priority scoring and escalation based on ticket content
- **Smart Routing**: Distribute tickets to appropriate departments and teams
- **Production Ready**: Built-in modules for safety, reliability, and cost optimization
- **PII Protection**: Automatic detection and redaction of personally identifiable information
- **Prompt Injection Defense**: Security measures against malicious prompt injection attempts
- **Interactive UI**: User-friendly interface for ticket submission and monitoring
- **Comprehensive Testing**: Full test suite for validation and quality assurance

## 🛠️ Technology Stack

- **Backend**: Python 3.x
  - LangGraph for agent orchestration and workflow management
  - Agent-based architecture for distributed processing
  - Natural Language Processing capabilities

- **Frontend**: HTML
  - Interactive demo UI
  - Real-time ticket processing interface
  - Results visualization

- **Production Modules**:
  - Cost calculation and optimization
  - Fallback and retry mechanisms
  - PII redaction and data privacy
  - Prompt injection detection
  - Response validation and verification

## 📁 Project Structure

```
AI-Support-Ticket-Classifier/
├── README.md                          # Project documentation
├── LICENSE                            # MIT License
├── .env.example                       # Environment variables template
├── .gitignore                         # Git ignore rules
├── requirements.txt                   # Python dependencies
│
├── main.py                            # Main application entry point
├── graph.py                           # Multi-agent graph definition and orchestration
├── schema.py                          # Data schemas and type definitions
│
├── production_modules/                # Production-ready safety and reliability modules
│   ├── __init__.py
│   ├── cost_calculator.py            # Cost tracking and optimization
│   ├── fallback_retry.py             # Retry logic and fallback mechanisms
│   ├── non_determinism.py            # Handling non-deterministic responses
│   ├── pii_redaction.py              # PII detection and redaction
│   ├── prompt_injection.py           # Prompt injection attack prevention
│   ├── prompt_versioning.py          # Prompt version management
│   ├── structured_output.py          # Structured output validation
│   └── validate_response.py          # Response validation utilities
│
├── demo_ui/                          # User interface for demonstrations
│   └── index.html                    # Interactive web interface
│
└── tests/                            # Test suite
    ├── __init__.py
    └── test_classifier.py            # Classifier tests
```

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Saisohithk/AI-Support-Ticket-Classifier.git
   cd AI-Support-Ticket-Classifier
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

## 📖 Usage

1. **Run the main application**
   ```bash
   python main.py
   ```

2. **Access the demo UI**
   Open `demo_ui/index.html` in your browser or access through the web server

3. **Submit a ticket**
   - Enter the ticket description and details
   - The multi-agent system will analyze and classify the ticket
   - View classification, priority, and routing results

## 🤖 Agent System

The system uses multiple specialized agents that collaborate through LangGraph:

- **Analyzer Agent**: Extracts key information and context from ticket content
- **Classifier Agent**: Categorizes tickets into predefined categories
- **Priority Agent**: Determines priority level based on ticket characteristics
- **Router Agent**: Routes tickets to appropriate departments and teams
- **Orchestrator**: Coordinates agent workflow and manages data flow

### Agent Communication

Agents communicate through a structured workflow graph defined in `graph.py`, enabling:
- Parallel processing where applicable
- Sequential dependencies between agents
- Error handling and fallback mechanisms
- Logging and monitoring of agent interactions

## ⚙️ Configuration

Create a `.env` file in the root directory:

```env
# Agent Configuration
AGENT_TIMEOUT=30
MAX_AGENTS=5
AGENT_LOG_LEVEL=INFO

# LLM Configuration
LLM_MODEL=gpt-4
LLM_TEMPERATURE=0.7
MAX_RETRIES=3

# Security
ENABLE_PII_REDACTION=true
ENABLE_INJECTION_DETECTION=true

# Processing
BATCH_SIZE=10
ENABLE_COST_TRACKING=true
```

## 🧪 Testing

Run the test suite to validate the classifier:

```bash
# Run all tests
python -m pytest tests/

# Run specific test file
python -m pytest tests/test_classifier.py -v

# Run with coverage report
python -m pytest tests/ --cov=. --cov-report=html
```

## 📊 Supported Categories

- **Technical Support**: Hardware, software, and system issues
- **Billing**: Payment and invoice inquiries
- **General Support**: Account and service questions
- **Feature Request**: Enhancement and feature suggestions
- **Bug Report**: Software defects and issues
- **Other**: Miscellaneous inquiries

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📧 Contact

For questions or support, please contact:
- **Author**: Saisohithk
- **Email**: [Saisohithkommana@gmail.com]
- **GitHub**: [@Saisohithk](https://github.com/Saisohithk)

## 🙏 Acknowledgments

- Built with LangGraph for agent orchestration
- Thanks to the AI community for inspiration and best practices
- Special thanks to all contributors

---

**Last Updated**: May 2026

Feel free to ⭐ this repository if you found it helpful!
