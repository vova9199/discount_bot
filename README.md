# README

This is a Python project for collecting and displaying information about discounted products. The project consists of two main parts: data collection and a Telegram bot for user interaction.

## Prerequisites

Before running the project, make sure you have the following prerequisites installed:

- Python (3.7 or higher)
- `requests` library (for making HTTP requests)
- `aiogram` library (for creating a Telegram bot)
- An active Telegram bot and its token

## Project Structure

The project is divided into two main parts:

1. **Data Collection:**
   - The `main.py` file contains functions for collecting data from a specific website, in this case, the Salomon online store.
   - It collects information about discounted products, including their titles, categories, prices, and discount percentages, and stores this data in a JSON file (`result_data.json`).

2. **Telegram Bot:**
   - The `bot.py` file sets up a Telegram bot using the `aiogram` library.
   - The bot can interact with users and display discounted products in response to specific commands.

## Installation

1. Clone this repository to your local machine using Git:
```shell
git clone https://github.com/yourusername/discounted-products.git
```


2. Navigate to the project directory:
```shell
cd discounted-products
```

3. Create a virtual environment (optional but recommended):
```shell
python -m venv venv
```

4. Activate the virtual environment:

- On Windows:

  ```
  venv\Scripts\activate
  ```

- On macOS and Linux:

  ```
  source venv/bin/activate
  ```

5. Install the required Python libraries using pip:
```shell
pip install -r requirements.txt
```


6. Set up a Telegram bot and obtain a bot token from the [BotFather](https://core.telegram.org/bots#botfather).

7. Create a `.env` file in the project directory and add your bot token as follows:
```shell
TOKEN=YOUR_BOT_TOKEN
```
### Data Collection

1. Open the `main.py` file and configure the `headers` dictionary with the necessary HTTP headers for your specific use case.

2. Modify the URL in the `collect_data` function to the website you want to scrape. You can customize the URL parameters to match your requirements.

3. Run the data collection script by executing `python main.py`. This will collect data and store it in a JSON file.

### Telegram Bot

1. Set up a Telegram bot and obtain a bot token from the [BotFather](https://core.telegram.org/bots#botfather).

2. Create a `.env` file and add your bot token as follows:

```shell
TOKEN=YOUR_BOT_TOKEN
```

3. Open the `bot.py` file and customize the commands and responses for your bot as needed.

4. Run the bot script by executing `python bot.py`. Your bot will start listening for commands.

## Telegram Bot Commands

- `/start`: Start the bot and display available product categories.
- `/Кроссовки`: Display discounted sneakers with their details, such as title, category, price, and discount percentage.
