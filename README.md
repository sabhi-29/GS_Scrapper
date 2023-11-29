# Google Scholar Scraper Python Library

![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg)

Welcome to the Google Scholar Scraper Python Library! This library is designed to help researchers retrieve citation information from Google Scholar legally and efficiently. The primary aim is to assist fellow researchers in obtaining citation data for their papers of interest without relying on expensive platforms.

## Features

### 1. `check_captcha()`
- **Description**: This function inspects the Google Scholar page visited by the `scrape()` function and detects the presence of a captcha. If a captcha is detected, the execution pauses until the user manually solves the captcha.

### 2. `get_paper_url(pubmed_id)`
- **Description**: This function should be called first by the user. It takes a PubMed ID as input and retrieves the Google Scholar URL for the corresponding paper.

### 3. `pause_for_one_minute()`
- **Description**: This function pauses the execution of the program for a random time between 5 to 10 seconds. This randomization helps avoid triggering Google Scholar's bot checker.

### 4. `scrape()`
- **Description**: The main function of the library. It returns the number of citations that the specified paper has on Google Scholar.

## Getting Started

To use this library, follow these steps:

1. Install the library using `pip install google_scholar_scraper`.
2. Import the library in your Python script.
3. Use the functions described above to retrieve citation data.

```python
from google_scholar_scraper import check_captcha, get_paper_url, pause_for_one_minute, scrape

# Example Usage
pubmed_id = "12345678"
paper_url = get_paper_url(pubmed_id)
check_captcha()
pause_for_one_minute()
citations = scrape(paper_url)
print(f"The paper with PubMed ID {pubmed_id} has {citations} citations on Google Scholar.")
```

## Version

This is the first version of the library. We are committed to making it more useful by integrating additional features. If you have suggestions or encounter any issues, please feel free to open an issue on GitHub.

## Contribution

We welcome contributions to enhance the functionality of this library. If you have ideas for new features or improvements, don't hesitate to open a pull request.

## License

This library is licensed under the MIT License - see the LICENSE.md file for details.

Happy researching!
