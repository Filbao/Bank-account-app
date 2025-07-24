# Bank-account-app
# 🏦 Kenya National Bank - Banking Application

A Python-based banking application built with Object-Oriented Programming (OOP) principles, featuring both command-line and Streamlit web interfaces.

## 📋 Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
  - [Command Line Version](#command-line-version)
  - [Streamlit Web App](#streamlit-web-app)
- [Project Structure](#project-structure)
- [Class Documentation](#class-documentation)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

- **Account Creation**: Automatically generates unique account numbers
- **Deposit Functionality**: Add money to your account with validation
- **Withdrawal System**: Withdraw money with insufficient funds protection
- **Balance Inquiry**: Check current account balance
- **Input Validation**: Robust error handling for all user inputs
- **Two Interfaces**: 
  - Command-line interface for local usage
  - Modern Streamlit web interface for browser-based interaction

## 🔧 Prerequisites

- Python 3.7 or higher
- pip (Python package installer)

## 📦 Installation

1. **Clone or download the repository**
   ```bash
   git clone <repository-url>
   cd banking-application
   ```

2. **Install required packages**
   ```bash
   pip install streamlit
   ```

3. **For Google Colab users**
   ```python
   !pip install streamlit
   ```

## 🚀 Usage

### Command Line Version

Run the original banking application in your terminal:

```bash
python banking_app_cli.py
```

**Features:**
- Interactive menu-driven interface
- Real-time balance updates
- Continuous operation until user exits
- Input validation and error handling

### Streamlit Web App

1. **Run locally:**
   ```bash
   streamlit run app.py
   ```

2. **For Google Colab deployment:**
   ```python
   # Get your IP address
   !wget -qO- ipv4.icanhazip.com
   
   # Run the app with localtunnel
   !streamlit run app.py & npx localtunnel --port 8501
   ```

**Features:**
- Modern web interface
- Session state management
- Real-time balance display
- Interactive buttons and forms
- Visual feedback with success/error messages

## 📁 Project Structure

```
banking-application/
│
├── app.py                          # Streamlit web application
├── banking_app_cli.py              # Command-line version
├── Creating_A_band_account_with_OOP.ipynb  # Jupyter notebook
└── README.md                       # This file
```

## 📚 Class Documentation

### `Account` Class

The core class that handles all banking operations.

#### Constructor
```python
def __init__(self, account_holder, account_number, account_balance=0.0)
```

#### Methods

- **`generate_account_number()`**
  - Generates a unique alphanumeric account number
  - Format: First 3 letters of holder's name + 10 random characters
  - Returns: String (e.g., "JOH1A2B3C4D5E6")

- **`deposit(amount)`**
  - Adds money to the account
  - Validates amount is positive
  - Updates balance and provides feedback
  - Returns: Boolean (success/failure) or String (for Streamlit)

- **`withdraw(amount)`**
  - Withdraws money from the account
  - Validates amount and sufficient funds
  - Updates balance and provides feedback
  - Returns: Boolean (success/failure) or String (for Streamlit)

- **`check_balance()`**
  - Displays current account information
  - Shows account holder name and balance
  - Returns: None (CLI) or String (Streamlit)

## 🎯 How It Works

1. **Account Creation**: User enters their name, and the system generates a unique account number
2. **Menu Selection**: Choose from deposit, withdraw, check balance, or exit
3. **Transaction Processing**: All inputs are validated before processing
4. **Balance Management**: Real-time balance updates with each transaction
5. **Session Management**: (Streamlit only) Maintains state throughout the session

## 🌐 Deployment

### Local Deployment
- Run directly with Python for CLI version
- Use Streamlit for web interface: `streamlit run app.py`

### Google Colab Deployment
1. Upload the notebook to Google Colab
2. Run the installation cells
3. Execute the Streamlit app cell
4. Use localtunnel for public access
5. Copy the generated URL to access your app

### Cloud Deployment Options
- **Streamlit Cloud**: Deploy directly from GitHub
- **Heroku**: Use with requirements.txt
- **Render**: Simple deployment with automatic builds

## 🛡️ Security Features

- Input validation for all user inputs
- Amount validation (no negative values)
- Insufficient funds protection
- Error handling for invalid operations
- Session state management (Streamlit)

## 🎨 User Interface

### Command Line Interface
- Clean, menu-driven design
- Clear prompts and feedback
- Error messages for invalid inputs
- Continuous operation loop

### Streamlit Web Interface
- Modern, responsive design
- Interactive forms and buttons
- Real-time balance display
- Visual feedback with colors and animations
- Session management

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Future Enhancements

- [ ] Multiple account support
- [ ] Transaction history tracking
- [ ] Account-to-account transfers
- [ ] Interest calculation
- [ ] Data persistence with database
- [ ] User authentication
- [ ] Transaction receipts
- [ ] Account statements

## 🐛 Known Issues

- Session state resets on page refresh (Streamlit version)
- No data persistence between sessions
- Single account per session limitation

## 📞 Support

For support, email your-email@example.com or create an issue in the repository.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

**Made with ❤️ by [Your Name]**

*Happy Banking! 🏦*
