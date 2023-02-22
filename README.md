# pytest-playwright

---

## UI autotest using Pytest and Playwright

---

Tools used:

+ [Python 3.11.2](https://www.python.org/downloads/)
+ [requests 2.28.2](https://pypi.org/project/requests/)
+ [playwright 1.30.0](https://pypi.org/project/playwright/)
+ [pytest 7.2.1](https://pypi.org/project/pytest/)

---

## How to use this project

1. Install [Google Chrome browser](https://www.google.com/chrome/)
2. Install requirements

+ If you use Windows install requirements with the following command:
```
pip install -r requirements.txt
```

+ If you use Linux install requirements with the following command:
```
+ pip3 install -r requirements.txt
```

2. Registrate on Qase.io TMS (Test Management System)
+ [Modern TestOps platform](https://qase.io/)

3. Create new project GoogleSearch
<img src="img/GS_Qase.png" width="300" height="300" alt="creation of project on the platform">

4. Create new suite Index Page
<img src="img/Create_suite.png" width="300" height="300" alt="creation of test suite">

5. Test suite Index Page is a representation of the main Google page
<img src="img/Google_page.png" width="300" height="200" alt="google main page">

+ [Google](https://www.google.com/)

6. Lets check that main search button have the text Google Search
+ Create test case in the Index Page suite
<img src="img/testCaseGS.png" width="600" height="200" alt="creation of test case">
+ Use the following command to download new browsers:

```
playwright install
```

+ Use the following command to run autotests:

```
pytest .
```

+ You can find the locator for the 1st test case on the index page
  + Use F12 button to open DevTools
  + <img src="img/main_button_devtools.png" width="200" height="200" alt="usin dev tools on the button">
  + <img src="img/button_html.png" width="800" height="100" alt="button html code">
  + We need to find locator for the button
  + CSS: 
  ```
  [data-ved="0ahUKEwj-7OLupaf9AhV4Q_EDHQPUDysQ4dUDCBA"]
  ```
  + XPATH: 
  ```
  //div[@class='FPdoLc lJ9FBc']//input[@name='btnK']
  ```