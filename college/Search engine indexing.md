- A web crawler is a piece of software that systematically visits webpages to index them
	- when it finds the header of the page it will look for meta tags and other information specifically left for it 
	- it then moves to the main body of the page where it;
		- looks for the keywords within a page 
		- looks for where those words were found
		- finds and follows links in the page 
- A meta tag is a piece of information attached to a website about what is in the website 
- indexing is the process of cataloguing websites for a search engine to then give to a user 
- Boolean operators can be used to narrow down a search e.i. the user can remove a certain phrase or keyword by searching with NOT 
- Search engine companies have to continually improve their algorithms to prevent websites from learning the algorithm too well and always appearing at the top of the results as this may worsen the user experience and turn potential users away from the search engine, this helps them to stay competitive 
### The index

- Stored as a weighted directed graph 
	- pages are nodes 
	- hyperlinks are edges 
	- Weightings are calculated by page rank 
- Search provider stores the links in a database along with their page rank 
- when searching the internet you are searching the search providers database

### PageRank
- googles pagerank algorithm is used to determine the order webpages are shown to the user 
- Ranking determines how good a website is 
- This is needed to ensure that the user has a good experience and to stop people from filling a site with keywords to always appear at the top of a search 
$$
PR(A) = (1-d) + \frac{d(PR)}{C(PR)}
$$
d = damping factor, the probability that the user will click another link from your site, usually 0.85


## SEO - Search Engine Optimisation 
- quality content 
- update site regularly 
- mobile friendly 
- quick to load and responsive 
- fix broken links 
- add alt text to images 
- Use H1 and H2 
- group similar pages in directories 
- 