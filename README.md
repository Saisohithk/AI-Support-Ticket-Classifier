# AI Support Ticket Classifier

A machine learning-powered web application that automatically classifies and categorizes support tickets using artificial intelligence. This project combines Python backend logic with an HTML/CSS frontend to provide an intelligent ticket management system.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

The AI Support Ticket Classifier is designed to automate the process of categorizing support tickets by analyzing their content and assigning them to appropriate categories or departments. This reduces manual workload and ensures tickets are routed to the right teams efficiently.

## ✨ Features

- **Intelligent Classification**: AI-powered ticket categorization based on content analysis
- **Multi-category Support**: Classify tickets into multiple predefined categories
- **Real-time Processing**: Quick classification results for incoming tickets
- **User-friendly Interface**: Clean, responsive HTML interface for easy interaction
- **Batch Processing**: Process multiple tickets simultaneously
- **Performance Analytics**: Track classification accuracy and metrics

## 🛠️ Technology Stack

- **Backend**: Python
  - Machine Learning model for classification
  - Natural Language Processing (NLP)
  - Data preprocessing and analysis

- **Frontend**: HTML, CSS
  - Responsive web interface
  - Ticket submission and result display
  - Dashboard visualization

## 📁 Project Structure

```
AI-Support-Ticket-Classifier/
├── README.md
├── requirements.txt
├── models/
│   └── classifier_model.pkl
├── app.py
├── train.py
├── templates/
│   ├── index.html
│   ├── dashboard.html
│   └── results.html
├── static/
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── script.js
└── data/
    ├── training_data.csv
    └── categories.json
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

4. **Download pre-trained models (if applicable)**
   ```bash
   python download_models.py
   ```

## 📖 Usage

1. **Start the application**
   ```bash
   python app.py
   ```

2. **Open your browser**
   Navigate to `http://localhost:5000` (or the configured port)

3. **Submit a ticket**
   - Enter the ticket description in the text area
   - Click "Classify Ticket"
   - View the predicted category and confidence score

4. **Train the model (optional)**
   ```bash
   python train.py --data-path data/training_data.csv
   ```

## ⚙️ Configuration

Create a `.env` file in the root directory to configure the application:

```env
FLASK_ENV=development
DEBUG=True
MODEL_PATH=models/classifier_model.pkl
MIN_CONFIDENCE=0.5
MAX_WORKERS=4
```

**Configuration Options:**
- `FLASK_ENV`: Development or production mode
- `DEBUG`: Enable debug logging
- `MODEL_PATH`: Path to the trained classification model
- `MIN_CONFIDENCE`: Minimum confidence threshold for predictions
- `MAX_WORKERS`: Number of parallel workers for batch processing

## 🧠 Model Training

To retrain the model with your own data:

1. **Prepare your data**
   - Format: CSV with columns `[ticket_description, category]`
   - Place in `data/training_data.csv`

2. **Run training script**
   ```bash
   python train.py --epochs 50 --batch-size 32 --test-split 0.2
   ```

3. **Evaluate the model**
   ```bash
   python evaluate.py
   ```

## 📊 Supported Categories

- **Technical Support**: Hardware, software, and system issues
- **Billing**: Payment and invoice inquiries
- **General Support**: Account and service questions
- **Feature Request**: Enhancement and feature suggestions
- **Bug Report**: Software defects and issues
- **Other**: Miscellaneous inquiries

## 🔍 API Endpoints

- `POST /classify` - Classify a single ticket
- `POST /batch-classify` - Classify multiple tickets
- `GET /categories` - Get list of available categories
- `GET /metrics` - Retrieve model performance metrics
- `GET /dashboard` - View analytics dashboard

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
- **Email**: [your-email@example.com]
- **GitHub**: [@Saisohithk](https://github.com/Saisohithk)

## 🙏 Acknowledgments

- Thanks to the Python ML community for excellent libraries like scikit-learn and NLTK
- Inspired by modern support ticket management systems
- Special thanks to all contributors

---

**Last Updated**: May 2026

Feel free to ⭐ this repository if you found it helpful!
