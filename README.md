# Getting Started with Git and GitHub

## 1. Installing Git on Windows

First, let's check if you already have Git installed:

- Open your command prompt or terminal and type:
```
git --version
```
If you see a version number, great! You have Git installed. Otherwise, follow the steps below:

- Visit the [official Git website](https://git-scm.com/)
- Click on "Download" for Windows.
- Run the downloaded installer and follow the prompts. Accept the default settings for the easiest setup.

## 2. Setting up Git

If you've just installed Git or haven't configured it yet, it's time to set it up:

- Open the Git Bash terminal (which should come with Git).
- Set up your Git identity with the following commands:
```
git config --global user.name "Your Full Name"
git config --global user.email "your-email@example.com"
```

## 3. Configuring SSH for GitHub on Windows

If you've already set up SSH before, you can skip this step. Otherwise, here's how:

### a. Generate SSH Key

- In your Git Bash terminal, enter:
```
ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
```
Just press `Enter` to save the key in the default location.

### b. Start the ssh-agent in the background
```
eval $(ssh-agent -s)
```
### c. Add your SSH key to the ssh-agent
```
ssh-add ~/.ssh/id_rsa
```
### d. Copy the SSH key to your clipboard
```
clip < ~/.ssh/id_rsa.pub
```

### e. Now, navigate to [your GitHub settings](https://github.com/settings/keys). Click "New SSH Key", paste your key, and save.

## 4. Important Git Commands

- **Clone a Repository**:
  - Use this to copy a repository from GitHub to your local machine.
```
git clone [repository_url]
```
- **Add**:
  - Tells Git which changes you'd like to include in the next commit.
```
git add [filename] # For a specific file
git add . # For all files in the directory
```
- **Commit**:
  - Save the staged changes along with a message describing what you did.
```
git commit -m "Your descriptive commit message here"
```
- **Push**:
  - Send your commits to a remote repository on GitHub.
```
git push [remote_name] [branch_name] # Typically: git push origin main
```
- **Pull**:
  - Update your local project with commits from a remote repository.
```
git pull [remote_name] [branch_name] # Typically: git pull origin main
```

