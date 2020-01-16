## Methodology and Data

### Research Methods

In this project, I use k-means clustering to find groups of postal code prefixes that are similar based on the most popular types of venues that are near the postal code prefixes locations. I experiment with different values for k because if k is too low, there won’t be much differentiation between different postal codes, but if k is too large, each postal code would be in a cluster by itself. The best value of k will provide at least one cluster that contain postal codes from both cities, and it will provide clusters that are significantly different from other clusters.

*Note:* I use the word "postal code prefix" to mean either a 3-character string or to mean the area on a map that has addresses that use that 3-character prefix. I believe the reader will be able to differentiate between the two meanings.

Another way of doing this analysis would be to consider each postal code prefix in Montreal, and then find the postal code prefix in Toronto that is the most similar. The biggest potential problem with this is that it might find a match for a Montreal postal code prefix that was actually not very similar. This difficulty could be overcome by setting a minimum similarity score so that no match would be returned if the most similar neighborhood had a score that was too low. Another potential problem is that many postal codes in Montreal would match up with the same postal code in Toronto. If this happened, the pool of potential business to be recruited would be small because many other similar neighborhoods in Toronto would be left out. This difficulty could be overcome by finding the best N matches for each neighborhood in Montreal, but then we would have to find the optimal value of N. This could be an interesting way of solving the problem if using k-means clustering does not solve it.

### Data

By using the information in the Introduction as well as information contained in the Literature Review section, one can make a table containing all of the postal code prefixes that have land in Ville Marie. The following table contains the postal code prefixes that contain neighborhoods in Ville Marie prefixes, the descriptions of the postal code prefixes’s areas from https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_H, and names of other neighborhoods that are in those postal code prefixes based on Google Maps and the Wikipedia pages about Montreal and Ville Marie.

<<< insert table here >>>

The coordinates of the postal code prefixes were critical for this study. I got them by googling "coordinates of XXX" where XXX was a postal code. If there were no legal or practical prohibitions, I think I could have scraped the coordinates from the result page in Python. However, the previous labs provided CSV files with the location data, so I decided not to try to scrape Google pages in my Python code. I copied the coordinates from the Google results and put them into a CSV. My Python code converts the strings of characters from Google into numerical coordinates that can be used with FourSquare and Folium.

<<< insert table here >>>

In addition to the above, I used FourSquare to get information about venues near the postal code prefixes’ locations.



