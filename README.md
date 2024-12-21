# MakePrivate - Securely Hide Your Files

MakePrivate is a batch script that locks and hides a folder named "Private" on Windows systems. It provides an efficient way to secure sensitive data without the need for third-party tools. The script includes password protection and ensures that unauthorized users cannot access the hidden files.

## Features
- **Folder Locking**: Renames and hides the "Private" folder by converting it into a system-protected directory.
- **Password Protection**: Prevents unauthorized access to the locked folder.
- **User Prompts**: Includes confirmation dialogs and password input.
- **Reversible Process**: Unlock and access your files using the correct password.

## How It Works
1. **Locking the Folder**:
   - The "Private" folder is renamed to `Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}` and marked with hidden and system attributes.
   - The folder becomes invisible and inaccessible to users.
2. **Unlocking the Folder**:
   - Users are prompted to enter a password.
   - If the password matches, the folder is renamed back to "Private" and its attributes are removed.
3. **Creating the Folder**:
   - If the "Private" folder does not exist, the script creates it automatically.

## Getting Started

### Prerequisites
- A Windows system.

### Installation
1. Download the `MakePrivate.bat` file.
2. Place it in the directory where you want to secure your files.

### Usage
1. Double-click `MakePrivate.bat` to run the script.
2. Follow the on-screen prompts:
   - **To lock the folder**: Confirm by typing `Y` or `N` when prompted.
   - **To unlock the folder**: Enter the correct password when prompted.

### Default Password
The default password is `Paassword`. You can change it by editing the script. Replace `Paassword` in the `UNLOCK` section with your desired password.

## Example Commands
- Lock the folder:
  ```cmd
  ren Private "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
  attrib +h +s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
  ```
- Unlock the folder:
  ```cmd
  attrib -h -s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
  ren "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" Private
  ```

## Notes
- Make sure to remember your password. Without it, you cannot access your hidden files.
- Avoid renaming the script file or the "Private" folder manually to prevent errors.
- Test with non-critical files before using it for important data.

## Contributing
Contributions are welcome! Feel free to fork this repository, submit pull requests, or suggest improvements via issues.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Disclaimer
MakePrivate is for educational and personal use only. Use it responsibly. The creator is not liable for any misuse, data loss, or damages caused by this script.

