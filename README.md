webdev_fuji
===========
The goal of this redesign was to implement several performance enhancing techniques that would improve DOMContentLoaded and load times.

Results
===========
First I want to address that a few additional performance improvements were not used to maintain code readability - minification and obfuscation. Additionally, the tests were performed on Chrome using the Chrome Developer Tools with the cache disabled. The results are an average of a set of 10 page refreshes both on the original site and my own. Note that although some assets were removed from the original in constructing the redesign, I believe that the impact on the final numbers is not particularly significant.

original oh-fuji.com/en/:
===========
62 GET requests, 8.1 MB transferred
1) 27.59s (load: 27.60s, DOMContentLoaded: 3.04s)
2) 24.51s (load: 24.52s, DOM: 4.99s)
3) 19.92s (load: 19.92s, DOM: 943ms)
4) 21.77s (load: 21.77s, DOM: 984ms)
5) 19.11s (load: 19.12s, DOM: 943ms)
6) 20.37s (load: 20.37s, DOM: 1.34s)
7) 21.52s (load: 21.52s, DOM: 1.03s)
8) 19.55s (load: 19.56s, DOM: 985ms)
9) 20.35s (load: 20.36s, DOM: 967ms)
10) 22.57s (load: 22.57s, DOM: 1.07s)
Average: 21.762s (load: 21.731s, DOM: 1.629s)
	

redesigned oh-fuji.com/en/:
===========
39 GET requests, 1.7 MB transferred
1) 2.54s (load: 2.54s, DOM: 882ms) 
2) 2.53s (load: 2.53s, DOM: 878ms)
3) 2.53s (load: 2.53s, DOM: 905ms)
4) 2.86s (load: 2.86s, DOM: 1.22s)
5) 3.94s (load: 3.94s, DOM: 1.21s)
6) 2.52s (load: 2.52s, DOM: 858s)
7) 2.65s (load: 2.66s, DOM: 865ms)
8) 2.58s (load: 2.58s, DOM: 868ms)
9) 2.73s (load: 2.73s, DOM: 871ms)
10) 2.70s (load: 2.71s, DOM: 1.20s)
Average: 2.758s (load: 2.76s, DOM: 976ms)

