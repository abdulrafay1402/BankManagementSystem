# 🏦 Bank Management System

[![Assembly](https://img.shields.io/badge/Assembly-x86-blue.svg)](https://en.wikipedia.org/wiki/X86_assembly_language)
[![MASM](https://img.shields.io/badge/MASM-32bit-green.svg)](https://www.masm32.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A comprehensive banking management system developed in x86 Assembly language (MASM32) with a user-friendly console interface. This project demonstrates low-level programming capabilities for managing bank accounts, transactions, and administrative operations.

## 📋 Table of Contents

- [Features](#-features)
- [System Requirements](#-system-requirements)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Technical Details](#-technical-details)
- [Screenshots](#-screenshots)
- [Team Members](#-team-members)
- [Contributing](#-contributing)
- [License](#-license)

## ✨ Features

### 👨‍💼 Administrator Panel
- **Account Management**
  - Create new customer accounts with unique account numbers
  - View detailed account information
  - Delete existing accounts with confirmation
  - Display all accounts in the system
  
- **Transaction Operations**
  - Deposit funds to customer accounts
  - Withdraw funds from accounts
  - Comprehensive transaction validation

### 👤 Customer Panel
- **Account Operations**
  - Secure PIN-based authentication
  - Check account balance
  - Withdraw money with balance verification
  - Transfer funds between accounts
  - Change account PIN

### 🎨 User Interface Features
- Animated loading screens with progress bars
- Color-coded menus and messages
- Error handling and validation
- Clear status messages and prompts
- Professional console-based UI

### 💾 Data Management
- Persistent storage using file system
- Account data structure with proper alignment
- Support for up to 10 concurrent accounts
- Real-time data synchronization

## 🖥️ System Requirements

- **Operating System:** Windows (32-bit or 64-bit)
- **Assembler:** MASM32 (Microsoft Macro Assembler)
- **Libraries:** Irvine32 Library
- **Processor:** x86 compatible processor
- **Memory:** Minimum 512 MB RAM
- **Storage:** 10 MB free disk space

## 🚀 Installation

### Prerequisites

1. **Install MASM32**
   ```
   Download and install MASM32 from: http://www.masm32.com/
   ```

2. **Install Irvine32 Library**
   ```
   Ensure Irvine32.inc and Irvine32.lib are in your MASM32 include/lib directories
   ```

### Build Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/abdulrafay1402/BankManagementSystem.git
   cd BankManagementSystem
   ```

2. **Assemble and Link**
   ```bash
   ml /c /coff Bank_Management_System.asm
   link /subsystem:console Bank_Management_System.obj
   ```

   Or use a batch file:
   ```batch
   @echo off
   ml /c /coff /Zi Bank_Management_System.asm
   link /subsystem:console /debug Bank_Management_System.obj
   pause
   ```

3. **Run the executable**
   ```bash
   Bank_Management_System.exe
   ```

## 📖 Usage

### Administrator Login
- **Default Credentials:**
  - ID: `admin`
  - Password: `1234`

### Customer Login
- Use your assigned account number and 4-digit PIN
- PIN range: 1000-9999

### Navigation
1. Launch the application
2. Select from Main Menu:
   - Option 1: Administrator Login
   - Option 2: Customer Login
   - Option 3: Exit System
3. Follow on-screen prompts for various operations

### Sample Workflow

**Creating a New Account (Admin):**
1. Login as administrator
2. Select "Create New Account"
3. Enter account number (unique positive integer)
4. Enter 4-digit PIN (1000-9999)
5. Enter initial balance

**Transferring Funds (Customer):**
1. Login with your account number and PIN
2. Select "Transfer Funds"
3. Enter recipient account number
4. Enter transfer amount
5. Confirm transaction

## 📁 Project Structure

```
BankManagementSystem/
│
├── Bank_Management_System.asm    # Main assembly source code
├── accounts.dat                  # Account data file (auto-generated)
├── README.md                     # Project documentation
└── build.bat                     # Build script (optional)
```

## 🔧 Technical Details

### Architecture
- **Platform:** x86 Assembly (32-bit)
- **Model:** Flat memory model
- **Stack Size:** 4096 bytes

### Data Structures

**Account Structure:**
```assembly
Account STRUCT
    accountNum   DWORD   0      ; Unique account identifier
    pin          DWORD   0      ; 4-digit PIN
    balance      DWORD   0      ; Account balance in dollars
    active       BYTE    1      ; Active status (1=Active, 0=Inactive)
    BYTE 3 DUP(?)              ; Padding for alignment
Account ENDS
```

### Key Features Implementation
- **File I/O:** Binary file operations for persistent storage
- **Memory Management:** Efficient struct-based account storage
- **Security:** PIN-based authentication with validation
- **UI/UX:** ANSI color codes for enhanced visual experience
- **Error Handling:** Comprehensive validation and error messages

### Color Scheme
- **Main Interface:** White on Black
- **Admin Panel:** Light Green
- **Customer Panel:** Light Magenta
- **Success Messages:** Light Green
- **Error Messages:** Light Red
- **Loading Animation:** Light Blue to Green gradient

## 📸 Screenshots

### Main Menu
```
========================================
         BANK MANAGEMENT SYSTEM        
         Secure Banking Solution       
========================================

            MAIN MENU
          --------------

      1) Administrator Login
      2) Customer Login
      3) Exit System
```

### Loading Screen
```
[████████████████████] 100%

Complete! Press any key to continue...
```

## 👥 Team Members

This project was developed by:

- **[Abdul Rafay](https://github.com/abdulrafay1402)** - Developer
- **[Bisma Shahid](https://github.com/Bisma-404)** - Developer
- **[Afshal Liaquat](https://github.com/afshalliaquat)** - Developer

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines
- Follow consistent code formatting
- Add comments for complex logic
- Test all features before submitting
- Update documentation as needed

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Irvine32 Library** - For providing essential I/O procedures
- **MASM32** - For the assembly development environment
- **Microsoft** - For x86 architecture documentation

## 📞 Contact

For questions, suggestions, or issues, please:
- Open an issue on GitHub
- Contact the team members via their GitHub profiles

---

<div align="center">
  <p>Made with ❤️ using x86 Assembly</p>
  <p>© 2026 Bank Management System Team</p>
</div>
