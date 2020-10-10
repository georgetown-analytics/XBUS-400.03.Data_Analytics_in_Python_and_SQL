# Module 3 Week 1 Graded Lab directions

### Using pandas

1. Use a pandas's convenience function to grab the table of the host cities for the Olympics from https://en.wikipedia.org/wiki/List_of_Olympic_Games_host_cities as a DataFrame.

2. Use the DataFrame API to complete the following queries.
---
1. What years were the Olympics hosted in 
	- a) the United States? 
	- b) Japan? 
	- c) France?

2. How many times were the Olympics hosted in
	- a) Europe?
	- b) Asia?
	- c) South America?

3. How many times were the Olympics hosted in
- a) the United States before 1990? After 1990?
- b) the United Kingdom before 1990? After 1990?
- c) Italy before 1990? After 1990?
---
### Using BeautifulSoup

3. Use BeautifulSoup to create a soup for the HTML document in `data.html`. (You will need to read in the string from the file, for example using [Python's open function](https://docs.python.org/3/library/functions.html#open).)

4. Select *all* the divs with the `data-item` class.

5. Use a for loop to loop through all of those divs and print out the content of their *one* p tag.

6. Use requests to grab the `text` of the response from the URL "https://forecast.weather.gov/MapClick.php?lat=38.882715000000076&lon=-76.99675499999995#.X4EDD5NKjDI" (should be a string of the HTML document at that URL).

7. Use BeautifulSoup to create a soup with the HTML.

8. Select the *one* element that has id `seven-day-forecast`.

9. Use a for loop to iterate through each weather forecast panel -- identifiable from the class `forecast-tombstone` -- from the element in (8), and print out the text from selecting one each of the elements in that panel that match the `period-name`, `short-desc`, and `temp` classes, respectively.

10. Instantiate an empty list before your for loop, and append a list of the values obtained in the body of each for loop iteration to it. At the end, use the list of lists to create a DataFrame and show the head of the DataFrame. (See lecture slide 32 for an example).