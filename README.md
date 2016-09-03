# Basic-scraper
## A python script that scrapes restaurant health inspection data from the King County government website.
### Data is returned in the following format for a single location:
```
{'': ['SEATTLE, WA 98117', 'SEATTLE, WA 98117'],
'Phone': ['(206) 318-1575', '(206) 318-1575'],
'Latitude': ['47.7019242696', '47.7019242696'],
'Longitude': ['122.3636914535', '122.3636914535'],
'Business Name': ['STARBUCKS COFFEE #3346', 'STARBUCKS COFFEE #3346'],
'Business Category': ['Seating 13-50 - Risk Category II', 'Seating 13-50 - Risk Category II'],
'Address': ['9999 HOLMAN RD NW', '9999 HOLMAN RD NW']} 
 {'Total Inspections': 1, 'Average Score': 30.0, 'High Score': 30} 
 ```
### To run a test version, using a static html (src/inspection_page.html):
```
$python scraper.py test
```
### To use an API call:
```
$python scraper.py

### The parameters for the search are at the bottom of scraper.py and can be adjusted:
```
if __name__ == "__main__":
    kwargs = {
        'Inspection_Start': '1/1/2013',
        'Inspection_End': '1/10/2013',
        'City': 'Seattle',
        'Zip_code': '98108'
    }
```
### sources:
* https://codefellows.github.io/sea-python-401d4/assignments/tutorials/scraper.html