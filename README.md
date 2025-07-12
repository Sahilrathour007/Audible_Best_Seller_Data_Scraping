# 📚 Audible India Bestseller Scraper

This Python project uses **Selenium** to scrape bestseller audiobook data from [Audible India](https://www.audible.in/charts). The data includes title, author, length, and price, and is saved to a CSV file.

## 🚀 Features

- Scrapes all pages of the Audible bestseller chart
- Extracts:
  - Book Title
  - Author Name
  - Length (Duration)
  - Price (₹ INR)
- Saves data to `Bestseller_books.csv`

## 🧰 Requirements

- Python 3.7+
- Google Chrome
- ChromeDriver

## 🧪 Libraries Used

- `selenium`
- `pandas`
- `time`

Install required packages using:

```bash
pip install selenium panda

## ⚠️ Common Issues & Tips

While working on this project, here are some key issues I faced and suggestions to overcome them:

1. **XPath Issues**  
   - Identifying the right XPath can be tricky.
   - Always inspect elements in Chrome Developer Tools and test your XPath using browser console (`$x("your_xpath_here")`) to make sure it matches what you expect.
   - Avoid overly specific or dynamic classes that may change.

2. **Timeout Errors**  
   - Web elements can take time to load, especially on slower networks.
   - Use both `explicit waits` (`WebDriverWait`) and `implicit waits` (`time.sleep(seconds)`) to ensure your script handles delays gracefully.
   - Avoid `time.sleep()` unless absolutely needed.

3. **Use `try-except` Blocks**  
   - Not all books have complete data (e.g., missing price or author).
   - Wrapping element lookups in `try-except` ensures your code doesn’t break and helps track where things fail.

4. **Print Feedback After Major Steps**  
   - Adding `print()` statements after every critical block helps debug faster.
   - For example: `"Page X scraped successfully"` or `"Price missing for one entry"` can give real-time feedback.

These tips can save hours of debugging and make your scraper more robust and maintainable.
