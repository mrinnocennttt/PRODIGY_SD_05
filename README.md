# PRODIGY_SD_05

import requests
from bs4 import BeautifulSoup

url = "https://example.com"
page = requests.get(url)

soup = BeautifulSoup(page.text, "html.parser")

titles = soup.find_all("h1")

for t in titles:
    print(t.text)
