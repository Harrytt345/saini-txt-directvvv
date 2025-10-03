# SAINI DRM Bot - Telegram Text Downloader Bot

## Overview
This is a Telegram bot that can extract videos and PDFs from text files and upload them to Telegram. It includes DRM support with a minimum quality of 360p and features a Flask web interface.

## Project Structure
- **Flask Web App (Frontend)**: Runs on port 5000, displays bot information
- **Telegram Bot (Backend)**: Processes text files, downloads videos/PDFs, handles user interactions
- **modules/**: Contains all bot logic and handlers
  - `main.py`: Main bot entry point
  - `text_handler.py`: Handles text file processing
  - `html_handler.py`: HTML conversion features
  - `drm_handler.py`: DRM video handling
  - `youtube_handler.py`: YouTube download functionality
  - `commands.py`, `features.py`, `settings.py`, etc.

## Setup Instructions

### 1. Environment Variables
You need to set up the following environment variables in the Replit Secrets:

- **API_ID**: Get from https://my.telegram.org/apps
- **API_HASH**: Get from https://my.telegram.org/apps
- **BOT_TOKEN**: Get from @BotFather on Telegram
- **OWNER**: Your Telegram user ID (numeric)
- **CREDIT**: Your name/credit to display
- **AUTH_USERS**: Comma-separated list of authorized user IDs
- **TOTAL_USERS**: Comma-separated list of all users

### 2. Getting Your Credentials

#### Telegram API Credentials:
1. Go to https://my.telegram.org/apps
2. Log in with your phone number
3. Create a new application
4. Copy the **API_ID** and **API_HASH**

#### Bot Token:
1. Open Telegram and search for @BotFather
2. Send `/newbot` and follow the instructions
3. Copy the bot token provided

#### Your User ID:
1. Search for @userinfobot on Telegram
2. Send `/start` to get your user ID

### 3. Current Status
- ✅ Python 3.12 installed
- ✅ System dependencies installed (ffmpeg, aria2)
- ✅ All Python dependencies installed
- ✅ Flask app configured for port 5000
- ✅ Workflow created to run both Flask and bot
- ✅ Environment variables configured
- ✅ **Bot is running and connected to Telegram**

### 4. Using the Bot
Your Telegram bot is now live! Here's how to use it:
1. Open Telegram and search for your bot
2. Send `/start` to begin
3. All features (including premium features) are enabled for your user ID
4. Upload text files with video/PDF links to download them
5. Use the various commands listed above for different features

## Features
- Text file processing and video extraction
- PDF download support
- DRM-protected video download (min 360p)
- YouTube video/audio download
- Text to HTML conversion
- User authorization system
- Broadcast messaging
- Settings management

## Bot Commands
- `/start` - Start the bot
- `/stop` - Stop ongoing process
- `/id` - Get your Telegram ID
- `/info` - Check your information
- `/cookies` - Upload YouTube cookies
- `/y2t` - YouTube to .txt converter
- `/ytm` - YouTube to .mp3 downloader
- `/t2t` - Text to .txt generator
- `/t2h` - .txt to .html converter
- `/logs` - View bot activity (owner only)

## Technical Details
- **Language**: Python 3.12
- **Frameworks**: Pyrogram (Telegram), Flask (Web)
- **Dependencies**: See requirements.txt
- **System Tools**: FFmpeg, aria2, mp4decrypt (Bento4)

## Architecture
The application runs both:
1. Flask web server on 0.0.0.0:5000 (public-facing)
2. Telegram bot (background worker)

Both processes are managed by a single workflow using `start.sh`.

## Recent Changes
- 2025-10-03: Initial setup in Replit environment
  - Installed all dependencies
  - Created workflow for combined Flask + Bot execution
  - Configured Flask to bind to 0.0.0.0:5000
  - Created .env.example and documentation
