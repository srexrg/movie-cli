# 🎬 Movie CLI

A beautiful and interactive command-line tool for searching and streaming movies using TMDB (The Movie Database) and vidsrc.net. Built with pure Bash for maximum compatibility.

https://github.com/user-attachments/assets/46888faf-b75e-41ef-b5e6-84f5fa103285

## ✨ Features

- 🔍 **Smart Movie Search**: Search movies using TMDB's extensive database
- 🎭 **Interactive Selection**: Beautiful movie selection menu with descriptions and release dates
- 🚀 **Fast Mode**: Skip IMDB ID fetching for quicker streaming
- 🎨 **Colorful Interface**: Rich colored output with emojis and progress indicators

## 🚀 Installation

### Prerequisites

Make sure you have the following installed:

```bash
# Ubuntu/Debian
sudo apt install curl jq

# CentOS/RHEL/Fedora
sudo dnf install curl jq  # or sudo yum install curl jq

# macOS
brew install curl jq

# Arch Linux
sudo pacman -S curl jq
```

### Setup

1. **Clone or download the script**:
   ```bash
   wget https://raw.githubusercontent.com/srexrg/movie-cli/main/movie-cli
   chmod +x movie-cli
   ```

2. **Get your TMDB API token**:
   - Go to [The Movie Database](https://www.themoviedb.org/)
   - Create a free account
   - Navigate to Settings → API
   - Copy the **API Read Access Token** (not the API Key)

3. **Set up your API token**:
   ```bash
   export TMDB_API_TOKEN="your_token_here"
   
   # For permanent setup, add to your shell profile:
   echo 'export TMDB_API_TOKEN="your_token_here"' >> ~/.bashrc
   source ~/.bashrc
   ```

## 🎯 Usage

### Basic Usage

```bash
# Search and play a movie
./movie-cli "Inception"

# Interactive mode (enter movie name when prompted)
./movie-cli
```

### Advanced Options

```bash

# Fast mode (skip IMDB ID fetch)
./movie-cli --fast "Avengers Endgame"

# Show help
./movie-cli --help

# Show version
./movie-cli --version

# Setup API key guide
./movie-cli --setup
```

### Environment Variables

```bash

# Set TMDB API token
export TMDB_API_TOKEN="eyJhbGciOiJIUzI1NiJ9..."
```


## 📖 Examples

```bash
# Quick search without IMDB ID lookup
./movie-cli --fast "Dune"

./movie-cli "Top Gun Maverick"
```

## 🎨 Features in Detail

### Interactive Movie Selection
- Displays up to 10 search results
- Shows movie title, release date, and description
- Numbered selection menu with colorful formatting
- Option to quit at any time

### Smart ID Resolution
- Searches TMDB database for accurate results
- Attempts to fetch IMDB IDs for better streaming compatibility
- Falls back gracefully if IMDB ID is not available
- Fast mode skips IMDB lookup for quicker results

### Robust Error Handling
- Comprehensive dependency checking
- Network timeout handling
- API error detection and reporting
- Graceful fallbacks for missing data

## 🛠️ Troubleshooting

### Common Issues

**"Missing dependencies" error**:
```bash
# Install required packages
sudo apt install curl jq  # Ubuntu/Debian
```

**"TMDB API Read Access Token not found" error**:
```bash
# Set up your API token
export TMDB_API_TOKEN="your_token_here"
./movie-cli --setup  # For detailed setup instructions
```


## 🤝 Contributing

Contributions are welcome! Here are some ways you can help:

- 🐛 Report bugs
- 💡 Suggest new features
- 🔧 Submit pull requests
- 📖 Improve documentation
- 🎨 Enhance the UI/UX


## ⚠️ Disclaimer

This tool is for educational purposes only. Please respect copyright laws and use legal streaming services when possible. The developers are not responsible for any misuse of this tool.

## 🙏 Acknowledgments

- [The Movie Database (TMDB)](https://www.themoviedb.org/) for providing the movie search API
- [vidsrc.net](https://vidsrc.net/) for streaming sources
- The open-source community for the tools that make this possible

---

**Made with ❤️ for movie lovers everywhere**

*If you find this tool useful, please ⭐ star the repository!*
