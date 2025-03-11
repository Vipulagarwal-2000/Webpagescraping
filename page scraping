import requests
from bs4 import BeautifulSoup

# Paste the URL you want to scrape
url = "URl"



# Send an HTTP GET request
response = requests.get(url)

# Check if request was successful
if response.status_code == 200:
    # Parse the HTML content
    soup = BeautifulSoup(response.text, "html.parser")
    
    # Extract title
    title = soup.title.text if soup.title else "No title found"
    
    # Extract all links
    #links = [a['href'] for a in soup.find_all('a', href=True)]

    # Extract text from paragraphs
    paragraphs = [p.get_text(strip=True) for p in soup.find_all('p')]

    # Join and display content
    content = "\n".join(paragraphs)
    
    
    print(f"Page Title: {title}\n")
    print("Page Content:\n", content)
   # print("Links Found:")
   # for link in links:
   #     print(link)
else:
    print(f"Failed to retrieve page. Status code: {response.status_code}")
