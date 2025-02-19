# 📌 Web Scraping Projects  

This repository contains Python-based **web scraping** projects designed to **automate data collection** from online sources. Using **BeautifulSoup** and **requests**, these projects efficiently extract and process relevant information.  

## 1️⃣ Price Drop Notifier 📉📧  
The **Price Drop Notifier** is a web scraper that tracks product prices on **eBay** and **sends an email alert** when the price drops below a user-defined target. This tool is useful for **bargain hunters** looking to purchase items at the best possible price.  

### 🔹 Features  
- ✅ **Extracts real-time price data from eBay**  
- ✅ **Compares price with a set target**  
- ✅ **Sends an email notification when the price drops**  
- ✅ **Secures email credentials using environment variables**  

---

## 2️⃣ Billboard Hot 100 Fetcher 🎶🔥  
The **Billboard Hot 100 Fetcher** scrapes the latest **Billboard Hot 100 chart** to keep track of trending music. It retrieves song rankings, artist names, and other relevant details, making it an excellent tool for **music lovers** and **data analysts**.  

### 🔹 Features  
- 🎵 **Fetches real-time Billboard Hot 100 chart rankings**  
- 🎤 **Extracts song titles & artist names**  
- 📊 **Useful for trend analysis & music tracking**  
- ⚡ **Fast & efficient data retrieval using BeautifulSoup**  

Both projects demonstrate how web scraping can be leveraged for **automation, data collection, and real-time notifications**. 🚀  

---

# 1️⃣ 🛒 eBay Price Notifer with Email Alerts

## 📖 Table of Contents
- [Project Overview](#-project-overview)
- [✨ Features](#-features)
- [⚙️ Requirements](#️-requirements)
- [📌 Variables](#-variables)
- [🚀 Setup](#-setup)
- [▶️ Usage](#️-usage)
- [📬 Email Alert Screenshot](#-email-alert-screenshot)
- [🔍 Observations](#-observations)
- [💡 Recommendations](#-recommendations)
- [🏁 Conclusions](#-conclusions)

---
## 📌 Project Overview
This project allows users to track the price of an eBay product. If the price drops to or below a user-defined target price, the system will send an email alert. 📩

### 🛠️ Technologies Used:
- **Python** 🐍: The programming language for the script.
- **BeautifulSoup** 🕵️‍♂️: For web scraping and parsing the HTML content of eBay product pages.
- **requests** 🌐: For making HTTP requests to fetch webpage content.
- **smtplib** 📧: For sending email alerts.
- **dotenv** 🔒: For securely managing environment variables (e.g., email credentials).

---
## ✨ Features
✅ **Track eBay product prices**: Monitor the price of a product from a specific eBay listing.

✅ **Email alerts**: Receive an email notification when the price drops to or below your target price.

✅ **Secure handling of email credentials**: Using environment variables to store sensitive information securely.

---
## ⚙️ Requirements
To use this project, you will need the following:
- **Python 3.x** 🐍
- Install the required libraries:
  ```bash
  pip install requests beautifulsoup4 python-dotenv
  ```

---
## 📌 Variables

| Variable Name  | Description | Example Value |
|---------------|------------|--------------|
| `SENDER_EMAIL` | The email address used to send notifications when the price drops. Stored securely using environment variables. | `youremail@example.com` |
| `RECEIVER_EMAIL` | The email address that will receive notifications when the price drops. Stored securely using environment variables. | `receiver@example.com` |
| `PASSWORD` | The password or app-specific password for the sender email. Stored securely using environment variables. | `yourpassword` |
| `PRODUCT_URL` | The URL of the eBay product you are tracking. | `https://www.ebay.com/itm/your-product-id` |
| `TARGET_PRICE` | The target price at which you want to receive an alert. If the product price drops to or below this value, you will be notified. | `700` |

---
## 🚀 Setup

### 1️⃣ Clone the repository
```bash
git clone https://github.com/yourusername/ebay-price-tracker.git
cd ebay-price-tracker
```

### 2️⃣ Create a `.env` file
In the root directory of the project, create a `.env` file to store your email credentials securely. Add the following details:
```ini
SENDER_EMAIL=your-email@example.com
RECEIVER_EMAIL=receiver-email@example.com
EMAIL_PASSWORD=your-email-password
```

### 3️⃣ Modify the product URL and target price
In the Python script, set the `PRODUCT_URL` to the eBay product URL you want to track and set your `TARGET_PRICE`:
```python
PRODUCT_URL = "https://www.ebay.com/itm/your-product-id"
TARGET_PRICE = 700  # Set your target price here
```

---
## ▶️ Usage

### 1️⃣ Run the script
```bash
python price_tracker.py
```

### 2️⃣ Email alerts
The script will fetch the product price from the eBay page and compare it to your target price. If the price drops to or below the target, you will receive an email notification. 📩

---
## 📬 Email Alert Screenshot
Here's a screenshot of the email alert you will receive when the price drops! 📉💰


<img width="960" alt="Price Drop Alert" src="https://github.com/user-attachments/assets/38a83247-9b4b-4503-8de2-84a5a25190a3" />


---
## 🔍 Observations
📌 **Web Scraping**: Web scraping is mainly dependent on the website structure, and any changes to eBay's page layout or class names might break the script. It’s recommended to test the script periodically to ensure it still works as expected.

📌 **Email Configuration**: The script uses Gmail's SMTP server. If you're using Gmail, ensure you enable "Less secure apps" or create an app-specific password if 2-factor authentication is enabled.

---
## 💡 Recommendations
💡 **Error Handling**: The script can be enhanced by adding more comprehensive error handling, especially to manage unexpected changes in the HTML structure, network errors, or email delivery failures.

💡 **Regular Checks**: Set up a task scheduler to run the script at regular intervals to ensure it checks the price periodically.

💡 **Multiple Product Support**: The script can be expanded to handle multiple products, allowing users to track prices for various items at once by accepting a list of product URLs and target prices.

---
## 🏁 Conclusions
The **eBay Price Tracker** 🛒 is a simple yet powerful tool that can help users monitor product prices on eBay and be alerted when prices drop below their target. By using **Python** 🐍 and **web scraping** 🕵️‍♂️, along with secure handling of email credentials 🔒, this script provides an easy-to-use solution for price tracking.

✨ **Future enhancements** could include additional features like supporting multiple products and improving error handling.

---
🚀 Happy Tracking! 🎯



---

# 2️⃣ Billboard Hot 100 Fetcher 🎶🔥  

## 📌 Table of Contents  

- [📖 Project Overview](#-project-overview)  
- [📌 Features](#-features)  
- [🚀 Setup](#-setup)  
  - [1️⃣ Clone the repository](#1️⃣-clone-the-repository)  
  - [2️⃣ Install dependencies](#2️⃣-install-dependencies)  
- [🎯 Usage](#-usage)  
  - [🔹 Example Output](#-example-output)  
  - [📝 Data Saved](#-data-saved)  
- [🔍 Observations](#-observations)  
- [📌 Conclusion](#-conclusion)  
- [🛠️ Troubleshooting](#️-troubleshooting)  
--- 


## 📌 Project Overview
🚀 This project scrapes the **Top 10 songs** from the **Billboard 200** chart for a given date using web scraping techniques. It allows users to select a date or use the latest chart and saves the data to a CSV file.

---

## 📌 **Features**
✔️ Fetch **Top 10 songs** from Billboard 200 🎵  
✔️ Allows users to **choose a date** 📅  
✔️ **Saves data** to CSV for future reference 📂  
✔️ Uses **BeautifulSoup** for web scraping 🕵️  
✔️ Handles **missing data & errors** gracefully ⚠️  

---

## 🚀 **Setup**

### 1️⃣ **Clone the repository**
```bash
git clone https://github.com/yourusername/billboard-hot-10-fetcher.git
cd billboard-hot-10-fetcher
```

### 2️⃣ **Install dependencies**
```bash
pip install requests beautifulsoup4 pandas
```

---

## 🎯 **Usage**
### Run the script:
```bash
python billboard_hot_10.py
```

### **🔹 Example Output**
```
📅 Available recent Billboard chart dates:
1. 2025-02-10
2. 2025-02-03
3. 2025-01-27
...

Enter a date (YYYY-MM-DD) or select from above (1-5), or press Enter for the latest chart: 2

🔗 Fetching data from: https://www.billboard.com/charts/billboard-200/2025-02-03/

🎵 Billboard Hot 10 Chart for 2025-02-03 🎶
   Rank         Song Title            Artist
1     1       Song Name 1          Artist 1
2     2       Song Name 2          Artist 2
...
```

### **📝 Data Saved**
The data is automatically saved as a CSV file:
```
Billboard_Top_10_2025-02-03.csv
```

---

## 🔍 **Observations**
- The script successfully extracts **Billboard Hot 10 songs** for any given date.
- If **Billboard's website changes**, the scraping method may need adjustments.
- Handling **incorrect or missing data** ensures smooth execution.

---

## 📌 **Conclusion**
This project demonstrates how **web scraping** can be used to fetch and analyze Billboard charts dynamically. By leveraging **BeautifulSoup and Pandas**, users can collect and save historical music trends effortlessly.

---

## 🛠️ **Troubleshooting**
🔹 **Website changed?** Billboard may update its structure, so check if `h3#title-of-a-story` still exists.  
🔹 **Blocked requests?** Try using a different `User-Agent`.  
🔹 **Wrong date format?** Ensure dates are entered in **YYYY-MM-DD** format.  

---


💡 Want to Improve It?
🚀 Feel free to fork the repo, suggest enhancements, or report any issues! Contributions are welcome! 😊









