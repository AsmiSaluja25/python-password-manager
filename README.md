# Password Manager

A simple and secure command-line password manager application.

## Table of Contents

- [Description](#description)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Security](#security)
- [Contributing](#contributing)
- [License](#license)

## Description

This password manager allows you to securely store and retrieve your passwords using a command-line interface. It uses strong encryption to protect your sensitive data.

## Features

-   **Secure Password Storage:** Encrypts passwords using Fernet encryption.
-   **Command-Line Interface (CLI):** Easy to use from the terminal.
-   **Database Storage:** Stores encrypted passwords in a database (e.g., MySQL).
-   **Master Password:** Uses a master password to derive the encryption key.
-   **Configuration:** Simple setup and deletion of configurations.
-   **Password Generation:** (Optional: If you add password generation) Generates strong, random passwords.

## Installation

1.  **Clone the repository:**

    ```bash
    git clone <repository_url>
    cd password-manager
    ```

2.  **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

3.  **Set up the database:**

    -   Ensure you have a MySQL server running.
    -   Update the `utils/dbconfig.py` file with your database credentials.

4.  **Configure the password manager:**

    ```bash
    python config.py make
    ```

    -   Follow the prompts to set up your master password.

## Usage

### Command-Line Interface (CLI)

-   **Add a password:**

    ```bash
    python pm.py a
    ```

    -   Follow the prompts to enter the website, username, and password.

-   **Retrieve a password:**

    ```bash
    python pm.py r -s <sitename>
    ```

    -   Replace `<sitename>` with the name of the website.
    -   Use the `--copy` flag to copy the password to your clipboard.

-   **Delete a password:**

    ```bash
    python pm.py d -s <sitename>
    ```

-   **List all passwords:**

    ```bash
    python pm.py l
    ```

-   **Configure the password manager:**

    ```bash
    python config.py <make/delete/remake>
    ```

## Security

-   **Master Password:** The security of your passwords depends on the strength of your master password. Choose a strong, unique password.
-   **Encryption:** Passwords are encrypted using Fernet encryption.
-   **Database Security:** Ensure your database is properly secured.
-   **Never store unencrypted passwords.**

## Contributing

Contributions are welcome! Please follow these steps:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Make your changes and commit them.
4.  Push your changes to your fork.
5.  Submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
special thanks to Tech Raj for explaining the code step by step.
