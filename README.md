# MakePrivate

A lightweight batch script for hiding files and folders on Windows systems using built-in commands. This repository provides a simple and efficient solution without requiring third-party tools.

## Features
- **Hide Files and Folders**: Mark files or folders as "hidden" and "system" using the `attrib` command.
- **Optional Password Protection**: Add a password prompt for extra security.
- **Stealthy**: The script can be disguised with a different name or icon.
- **Reversible**: Easily unhide files using the same script or manual commands.

## How It Works
1. **Hiding Files**: The script applies `+h` (hidden) and `+s` (system) attributes to make files or folders invisible in File Explorer.
2. **Revealing Files**: The script removes `+h` and `+s` attributes to make files visible again.
3. **Password Protection** (Optional): Modify the script to prompt for a password during execution.

## Getting Started

### Prerequisites
- A Windows system.

### Installation
1. Clone the repository or download the `.bat` file.
2. Open the script in a text editor to review or customize it.

### Usage
1. Run the `.bat` file by double-clicking it.
2. Follow the prompts to hide or unhide files and folders.

### Example Commands
- **Hide a file**:
  ```cmd
  attrib +h +s "C:\path\to\file"
  ```
- **Unhide a file**:
  ```cmd
  attrib -h -s "C:\path\to\file"
  ```

## Contributing
Contributions are welcome! Feel free to fork this repository, submit pull requests, or suggest improvements via issues.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Disclaimer
This script is provided for educational and personal use only. Use it responsibly. The creator is not liable for any misuse, data loss, or damages caused by this script.

