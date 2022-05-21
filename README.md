# webscrapping-data
# web scrapping

"""---------Using Beautiful Soup package to scrape the data from web"""
from bs4 import BeautifulSoup
import requests
url ="https://www.netflix.com"
response = requests.get(url)
html=response.text
print(html)
soup = BeautifulSoup(html)

#Create a soup object
print(soup.prettify())  #preetify the content of the soup object

#extracting the information
from bs4 import BeautifulSoup
import requests
url = "https://www.netflix.com"
response =requests.get(url)
html= response.text
soup = BeautifulSoup(html,"html.parser")

#Create a soup object

print(soup.title)  #prints title

print(soup.get_text()) #print text

a_tag_hyperlinks = soup.find_all('a')

# finds all a tags

for link in a_tag_hyperlinks: 
    print(link.get("href")) #print all the URLS
