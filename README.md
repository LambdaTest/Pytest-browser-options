# How to set browser specific options in Pytest on [LambdaTest](https://www.lambdatest.com/?utm_source=github&utm_medium=repo&utm_campaign=Pytest-browser-options)

If you want to set browser specific options for an automation test in Pytest on Lambdatest, you can use the following steps. You can refer to sample test repo [here](https://github.com/LambdaTest/pytest-selenium-sample).

# Steps:

You can specify the various browser specific options when defining the browser function. The following is are examples on how to set options for Chrome:

 ```
import pytest
@pytest.fixture
def chrome_options(chrome_options):
    chrome_options.binary_location = '/path/to/chrome'
    chrome_options.add_extension('/path/to/extension.crx')
    chrome_options.add_argument('--kiosk')
    return chrome_options
 ```
* The different options available for Chrome can be referred to [here](https://seleniumhq.github.io/selenium/docs/api/py/webdriver_chrome/selenium.webdriver.chrome.options.html).

Firefox:

```
import pytest
@pytest.fixture
def firefox_options(firefox_options):
    firefox_options.binary = '/path/to/firefox-bin'
    firefox_options.add_argument('-foreground')
    firefox_options.set_preference('browser.anchor_color', '#FF0000')
    return firefox_options
```
* The different options available for Firefox can be referred to [here](https://seleniumhq.github.io/selenium/docs/api/py/webdriver_firefox/selenium.webdriver.firefox.options.html).

* Full documentation for browser configuration [Pytest](https://pytest-selenium.readthedocs.io/en/latest/user_guide.html?highlight=desired#configuration-1).

# Links:

[LambdaTest Community](http://community.lambdatest.com/)

