# Installation Guide

This guide provides step-by-step instructions for installing and setting up AWS Q MicroManager.

## Prerequisites

- AWS Q Developer extension installed in VSCode
- Access to your AWS Q saved prompts directory

## Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/aws-q-micromanager.git
cd aws-q-micromanager
```

### 2. Install Prompt Files

Copy the prompt files to your AWS Q saved prompts directory:

**macOS/Linux:**
```bash
cp prompts/* ~/.aws/amazonq/prompts/
```

**Windows:**
```powershell
Copy-Item -Path .\prompts\* -Destination $env:USERPROFILE\.aws\amazonq\prompts\
```

### 3. Verify Installation

1. Open VSCode with the AWS Q Developer extension
2. In the AWS Q chat, type `@prompt MicroManager`
3. If the prompt loads correctly, you should see the MicroManager response

## Troubleshooting

If you encounter issues:

1. Ensure AWS Q Developer extension is up to date
2. Verify that the prompt files were copied to the correct location
3. Check that the prompt files have the correct permissions
4. Restart VSCode after installing the prompts

## Updates

To update to the latest version:

```bash
git pull
cp prompts/* ~/.aws/amazonq/prompts/
```