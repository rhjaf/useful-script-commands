Handling Exceptions
```python
raise Exception("this is exception")
```
Logging and Debugging
```python
import traceback
errorFile = open("errors.txt","a")
errorFile.write(traceback.format_exc())
errorFile.close()
assert "red" in "hel
```
More advanced logging
```python
import logging
logging.basicConfig(level=logging.DEBUG, format=' %(asctime)s -%(levelname)s - %(message)s') # add filename='myProgramLog.txt' if you want to output logs to a file
logging.info('Some debugging details.')
logging.debug('Some debugging details.'
```
**dunder variables**: `__f__` is global variable that will be set by python when running python programs

Sending Requests
```python
import requests
requests.get()
equests.status()
request.get().iter_count(10000)
```
Parsing HTML
```python
import bs4
import requests
res = request.get("ff.com")
soup =  bs 4.BeautifulSoup(res.txt,"html.parser")
soup.select("")[0].text().strip()# returns list css selector
```
Web automation with selenium
```python
from selenium import webdriver
browser = webdriver.Firefox()
browser.get("google.com")
elem = browser.find_element_by_css_selector("") # or elements
elem.click()
elem.send_keys('') # fill form fields
elem.submit()
elem.text
browser.quit().refresh().back().forward()# controlling browser
```
