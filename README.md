# Grant Proposal Generator

This repository contains a Python script that generates grant proposals using GPT-3.5 Turbo from OpenAI. The script utilizes various libraries for web scraping, XML parsing, and PDF handling. Below is an overview of the key components and functionalities of the project:

## Project Components

### 1. Libraries Used
- `requests`: Used for making HTTP requests to retrieve web content.
- `BeautifulSoup`: Employed for parsing HTML content from web pages.
- `pandas`: Utilized for data manipulation and handling DataFrames.
- `xml.etree.ElementTree`: Used for parsing XML data.
- `PyPDF2`: Used for extracting text from PDF documents.
- `openai`: Integrated for making API calls to GPT-3.5 Turbo.
- `configparser`: Used for reading API keys from a configuration file.
- `os`: Utilized for basic file operations.
- `fpdf`: Employed for generating PDF documents.

### 2. Configuration
- The project reads API keys and configuration settings from a `config.ini` file, ensuring secure API key management.

### 3. Data Parsing
- The script parses XML data from a file (`Grants_may18_xml.xml`) into a DataFrame.
- Entries with a "CloseDate" earlier than the current date are removed from the DataFrame.
- Entries with invalid or non-standard URLs are filtered out.

### 4. Web Scraping
- The script extracts text content from web pages linked in the DataFrame. It supports both HTML and PDF formats.
- Retrieved text content is saved to a file (`extracted_text.txt`).

### 5. Grant Proposal Generation
- Using GPT-3.5 Turbo, the script generates a grant proposal based on the extracted text content.
- The generated grant proposal is saved to a PDF file (`grant_proposal.pdf`) for easy distribution and sharing.

## Usage
1. Set up your OpenAI GPT-3.5 Turbo API key in the `config.ini` file.

2. Run the script to generate grant proposals based on the provided data.

## Example Output
The generated grant proposal will be displayed in the console and saved as a PDF file for your convenience.

Feel free to customize and adapt this project for your specific use case. It provides a foundation for automating grant proposal generation using GPT-3.5 Turbo and handling data from XML sources.
