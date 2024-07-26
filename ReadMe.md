# Game Competitors Data Extraction

This notebook is designed to extract and compile data about video games from various sources, including Steam and VGInsights, and then output the data into an Excel file.

## Prerequisites

Before running the notebook, ensure you have the following Python packages installed:

- `requests`
- `beautifulsoup4`
- `pandas`
- `xlsxwriter`

You can install them using pip:

```bash
pip install requests beautifulsoup4 pandas xlsxwriter
```

## Notebook Overview

### Setup and Imports

The notebook begins by importing necessary libraries and defining the `get_html_content` function to fetch HTML content from a given URL.

### Google Sheets URL and VGI JWT Token

You'll need to paste the URL of your Google Sheets containing a list of Steam URLs.
Additionally, you'll need to obtain and paste your VGI JWT token. This token can be obtained by creating a free account on VGInsights and finding the authorization header from one of their API calls.

### Extracting Game Details

The `get_game_details` function is defined to extract details about games from Steam pages, including game name, developer, publisher, release date, and price.

### Obtaining JWT Token Instructions

Instructions for obtaining the JWT token from VGInsights using Chrome Developer Tools are provided in detail within the notebook.

### Data Compilation

The notebook compiles the extracted game data and saves it into an Excel file using `pandas` and `xlsxwriter`.

## How to Use

### Prepare Your Google Sheet

Create a Google Sheet with a single column containing the Steam URLs of the games you want to gather data on.

### Obtain Your VGI JWT Token

Follow the instructions provided in the notebook to obtain your VGI JWT token from VGInsights.

### Run the Notebook

1. Ensure all dependencies are installed.
2. Paste your Google Sheets URL and VGI JWT token in the designated cells in the notebook.
3. Run all cells in the notebook to fetch the data and save it into an Excel file.

### Find Your Output

The resulting Excel file will be saved in the same directory as the notebook with the compiled game data.

## Notes

- The JWT token is required for some API calls to VGInsights. If the token is missing, some data may be missing or lead to error code 400.
- Keep your JWT token secure and do not share it publicly.
