# pytrader 🤖💰

[![Build Status](https://travis-ci.org/owocki/pytrader.svg?branch=master)](https://travis-ci.org/owocki/pytrader)
[![Gitcoin](https://gitcoin.co/funding/embed?repo=https://github.com/owocki/pytrader)](https://gitcoin.co/explorer?q=)

## Overview 🌟

**pytrader** is a _cryptocurrency trading robot_ designed to predict _price movements_ using _machine learning_, and execute trades based on its predictions. It was developed for use with the [poloniex.com cryptocurrency platform](http://poloniex.com).

### Demo ⚡

> Here’s a quick demonstration of what it looks like in action:

![pytrader in action](http://f.cl.ly/items/2m0p373L030F2y0U0I3p/9d7D_f-maxage-0.gif)

---

## Status 🚨

- __3/20/2017__: This project has been paused. Let us know if you want to help revive it! [Issue #80](https://github.com/owocki/pytrader/issues/80)
- __3/26/2016__: After 23,413 trades, the test portfolio went from 1 BTC to 0.955 BTC, incurring 2.486 BTC in fees. [A strategy is being developed](https://github.com/owocki/pytrader/issues/1).
- __3/27/2016__: Join the [pytrader Slack](https://github.com/owocki/pytrader/issues/23).

---

## Key Features 🔑

- 🤖 **Machine Learning Powered**: Uses pybrain and sklearn to make trading decisions.
- 📊 **Multiple Classifiers**: Includes decision trees, random forests, SVMs, and more.
- 📈 **Real-Time Trading**: Executes trades based on predictions for cryptocurrency pairs.
- 💻 **Django Admin**: Manage trades, monitor portfolio profitability, and debug trades via a graphical interface.

---

## How It Works ⚙️

**pytrader** uses various classifiers to decide whether to buy, sell, or hold based on historical price movements.

### 1. Classifiers 🧠

The system uses the following sklearn classifiers:

- Nearest Neighbors
- Linear SVM
- RBF SVM
- Decision Tree
- Random Forest
- AdaBoost
- Naive Bayes
- Linear Discriminant Analysis
- Quadratic Discriminant Analysis

#### Example: Decision Tree Classifier 📉

Here’s how a *Decision Tree* classifier makes decisions on the [BTC_ETH](https://www.poloniex.com/exchange#btc_eth) pair:

![Decision Tree](http://bits.owocki.com/1l3K0W3P1g0A/211224.png)

#### Example: Naive Bayes Classifier 📈

Similarly, a *Naive Bayes* classifier works on the [USDT_BTC](https://www.poloniex.com/exchange#usdt_btc) pair:

![Naive Bayes](http://bits.owocki.com/3f2E38052p0J/238365.png)

### 2. Neural Networks 🤖💡

Pybrain neural networks are also used for predicting price movements. These networks are tuned to find the best parameters for predicting price directionality.

---

## How to Get Started 🚀

### 1. Clone the Repository

```bash
git clone https://github.com/owocki/pytrader.git
```

### 2. Install Dependencies 📦

```bash
pip install -r requirements.txt
```

### 3. Configure Local Settings ⚙️

Create a `pypolo/local_settings.py` file with your settings. Example:

```python
API_KEY = "<POLO_API_KEY>"
API_SECRET = "<POLO_SECRET>"
MAKE_TRADES = True
ALERT_EMAIL = '<your_email>'
SMTP_USERNAME = '<smtp_user>'
SMTP_HOST = '<smtp_host>'
SMTP_PASSWORD = '<smtp_pass>'
```

---

## Features in Django Admin 🛠️

Admin dashboard allows you to:

- View **trade histories** and **portfolio profitability**.
- Graphical **debugging of trade decisions**.
- **Tuning of prediction tests** to improve decision accuracy.

![Admin Dashboard](https://d3vv6lp55qjaqc.cloudfront.net/items/0Q2O3l2J362K1P0Y3F1V/download.png)

---

## Why Open Source? 🌍

While **pytrader** can predict price movements with reasonable accuracy, it hasn't proven profitable *after fees*. The goal is to refine it and find a strategy that works. [Join the discussion here](https://github.com/owocki/pytrader/issues/1).

---

## Deployment 📦

Once you clone the repository:

1. Create the `local_settings.py` file.
2. Install dependencies: `pip install -r requirements.txt`.
3. Configure your database (PostgreSQL or SQLite).
4. Run migrations: 

```bash
./manage.py migrate
```

5. Install the cron jobs:

```bash
crontab scripts/crontab.txt
```

---

## Docker Setup 🐳

1. Install [Docker](https://docs.docker.com/engine/installation/) and [docker-compose](https://docs.docker.com/compose/install/).
2. Initialize the environment:

```bash
cp docker-compose.yml.example docker-compose.yml
cp docker/env.example docker/env
cp pypolo/local_settings.py.example pypolo/local_settings.py
```

3. Build the Docker image:

```bash
docker-compose build
```

4. Run the containers:

```bash
docker-compose up
```

---

## Additional Resources 📚

- **How to trade with pytrader**: [Trading Guide](https://github.com/owocki/pytrader/blob/master/howto_trade.md).
- **Seed database of prices**: [Download here](https://github.com/owocki/pytrader/issues/2).

---

### Support & Contact 📬

- Join our [Slack Channel](https://github.com/owocki/pytrader/issues/23).
- File an [Issue](https://github.com/owocki/pytrader/issues).

---

## Analytics 📊

We use Google Analytics to track usage:

<img src='https://ga-beacon.appspot.com/UA-1014419-15/owocki/pytrader' style='width:1px; height:1px;' >

```

### Key Enhancements:
- **Icons and Emojis**: Added visual elements like rockets 🚀, money 💰, and graphs 📈 for clarity and engagement.
- **Animated GIF**: Included an example animation of pytrader in action to make it more interactive.
- **Clear Sections**: Organized content into well-defined sections for better navigation.
- **Django Admin Screenshots**: Provided a visual representation of the Django admin interface for easier understanding.

This version improves readability, engagement, and provides a clear path for users to interact with the project.
