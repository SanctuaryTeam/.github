# Running Diablo4Trade Project on Windows

This guide provides instructions for setting up and running the Diablo4Trade project on a Windows system.

## Setup

1. **Enable Virtualization in BIOS:**
   Ensure that hardware virtualization is enabled in your computer's BIOS settings.

2. **Enable Hyper-V:**
   Enable Hyper-V feature in Windows by navigating to "Turn Windows features on or off" settings.

3. **Install WSL (Windows Subsystem for Linux):**
   Install Windows Subsystem for Linux by following the official documentation.

4. **Make sure Docker is installed.**
   ```bash
   docker --version
   ```


## Cloning Repositories and Installing Packages

1. **Open WSL Terminal:**
   Open a Windows Subsystem for Linux terminal on your Windows system.

2. **Change Directory to Home:**
   Navigate to your home directory by entering in the terminal.
   ```bash
   cd ~
   ```

4. **Create a Directory for Repos:**
   Create a directory to store repositories then navigate to the created directory by entering
   ```bash
   mkdir ~/sanctuaryteam && cd ~/sanctuaryteam
   ```

6. **Clone Repositories:**
   Clone the repositories into the newly created directory.
 `~\sanctuaryteam`


7. **Generate GitHub Personal Access Token:**
   Create a [new GitHub personal access token](https://github.com/settings/tokens/new) with the following scopes:
    ```
    read:packages
    ```

8. **Update .env Files:**
   For each repository, run `cp .env.example .env` to create a new `.env` file.
   Update the new `.env` file with `SANCTUARYTEAM_AUTH_TOKEN=YOUR_NEW_TOKEN`.  see __Editing on Windows__

9. **Navigate to Repo:**
   Navigate to the repository you want to contribute to, e.g., `~/sanctuaryteam/diablo4trading-xx`.

10. **Run Docker Compose:**
   Run `docker compose up` in the repository directory to install dependencies and start the development server.

11. **Verify Setup:**
   For a fresh setup, it's recommended to run in both frontend and backend repositories to verify the setup.
```bash
docker compose up
```

## Editing on Windows

1. **Install WSL Extension in Visual Studio Code:**
   Install the WSL extension for Visual Studio Code. [WSL for VSCode Docs](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl).

2. **Navigate to Repo:**
   Navigate to the repository you want to contribute to using WSL, e.g., `~/diablo4Trade/diablo4trading-fe`.

3. **Open in Visual Studio Code:**
   Use the command `code .` to open the repository in Visual Studio Code.

4. **Create a WSL Workspace for Full Stack Development:**
   You can set up a comprehensive workspace for full-stack development by including all three project folders: frontend, backend, and shared. Here's how:

   - Open Visual Studio Code.
   - Go to "File" > "Add Folder to Workspace...".
   - Select the front end folder of your project.
   - Repeat the above step, but this time select the backend folder.
   - Repeat again and select the shared folder.
   - Now you have all three folders open in your workspace, allowing you to work seamlessly on both the frontend and backend components.
