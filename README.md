# Testing website SauceDemo
[https://www.saucedemo.com/](https://www.saucedemo.com/)

## Tech Stack
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=Selenium&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=Jenkins&logoColor=white)
![Allure](https://img.shields.io/badge/Allure-FF4A36?style=for-the-badge)
![PyCharm](https://img.shields.io/badge/PyCharm-000000?style=for-the-badge&logo=pycharm&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

### Setup

Before running tests, you need to configure environment variables:

1. Create `.env` file in the project root
2. Add your Selenoid credentials:
```bash
SELENOID_LOGIN=user1
SELENOID_PASSWORD=1234
SELENOID_URL=selenoid.autotests.cloud
```

*The .env file is included in .gitignore to prevent accidentally committing credentials.*

### Test Run Commands

```bash
# Run all tests with Allure reporting
pytest tests/ --alluredir=allure-results -v

# Run specific test file
pytest tests/test_simple_po.py -v

# Run single test
pytest tests/test_simple_po.py::test_successful_login -v

# View Allure report
allure serve allure-results
```

## 📋 Test Scenarios

1) Successful Login - Verify user can log in with valid credentials

2) Add Item to Cart - Add specific product to cart and verify counter

3) Navigation - Open About page and verify navigation works

4) Logout - Successful user logout

5) Failed Login - Error handling for invalid credentials

### Report Examples


#### Jenkins Build
![Jenkins Build](readme_media/jenkins_build.png)

#### Allure Overview  
![Allure Report](readme_media/allure_overview.png)

#### Test Details
![Test Details](readme_media/test_details.png)

#### Telegram Notification
![Telegram](readme_media/telegram_notification.png)
