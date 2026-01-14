# 📚 Books Web Scraping Project

A Python-based web scraping project that extracts book information from [books.toscrape.com](http://books.toscrape.com) and performs data cleaning and analysis.

## 📋 Project Overview

This project demonstrates web scraping techniques using Python to collect book data from an online bookstore, clean the extracted data, and prepare it for analysis. The scraper collects information across 50 pages, gathering details about 1000 books.

## 🎯 Features

- **Automated Web Scraping**: Extracts data from multiple pages automatically
- **Data Collection**: Gathers book title, price, availability, and rating information
- **Data Cleaning**: Processes raw data into usable formats
- **CSV Export**: Saves both raw and cleaned data for further analysis

## 🛠️ Technologies Used

- **Python 3.x**
- **Libraries**:
  - `requests` - HTTP requests
  - `BeautifulSoup4` - HTML parsing
  - `pandas` - Data manipulation and analysis

## 📊 Data Collected

For each book, the scraper collects:
- **Title**: Book name
- **Price**: Price in GBP (£)
- **Availability**: Stock status
- **Rating**: Customer rating (1-5 stars)

## 🚀 Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/books-web-scraping.git
cd books-web-scraping
```

2. Install required packages:
```bash
pip install requests beautifulsoup4 pandas
```

## 💻 Usage

1. Open the Jupyter notebook `webscraping.ipynb` or run the Python script
2. The scraper will automatically:
   - Access 50 pages of book listings
   - Extract data from each book
   - Clean and process the data
   - Export results to CSV files

## 📁 Output Files

- `book.csv` - Raw scraped data
- `book_cleaned.csv` - Cleaned and processed data with:
  - Numeric price values
  - Boolean availability status
  - Integer rating values (1-5)

## 🔄 Data Cleaning Process

The cleaning pipeline includes:

1. **Price Cleaning**: Removes currency symbols and converts to float
2. **Rating Conversion**: Maps text ratings (One, Two, etc.) to numeric values (1-5)
3. **Availability Processing**: Converts text status to boolean values
4. **Data Type Optimization**: Ensures proper data types for analysis

## 📈 Sample Analysis Questions

The cleaned data can be used to answer questions like:
- What is the cheapest/most expensive book?
- What is the average price per rating category?
- How many books are in stock vs. out of stock?
- Price distribution across different ratings

## 🗂️ Project Structure

```
books-web-scraping/
│
├── webscraping.ipynb      # Main Jupyter notebook
├── book.csv               # Raw scraped data
├── book_cleaned.csv       # Cleaned data
└── README.md             # Project documentation
```

## ⚠️ Important Notes

- This project is for educational purposes only
- Respects the website's robots.txt and terms of service
- Includes appropriate delays between requests to avoid overloading the server
- The website (books.toscrape.com) is specifically designed for web scraping practice

## 📝 Data Schema

### Raw Data
| Column | Type | Description |
|--------|------|-------------|
| Title | string | Book title |
| Price | string | Price with currency symbol |
| Availability | string | Stock status text |
| Rating | string | Rating as word (One-Five) |

### Cleaned Data
| Column | Type | Description |
|--------|------|-------------|
| Title | string | Book title |
| Price | float | Numeric price value |
| Availability | boolean | True if in stock |
| Rating | integer | Rating from 1-5 |

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## 📜 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

Your Name
- GitHub: [@hamdysaied](https://github.com/hamdysaied)

## 🙏 Acknowledgments

- [books.toscrape.com](http://books.toscrape.com) for providing a safe environment for web scraping practice
- BeautifulSoup and pandas communities for excellent documentation

