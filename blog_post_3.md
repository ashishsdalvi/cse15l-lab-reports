# Welcome to Blog Post 2: Researching commands

[Blogs](https://ashishsdalvi.github.io/cse15l-lab-reports/testing)


## Researching Grep

**-c flag**
The first option for using grep that I found was using the ```-c``` flag. This flag
prints the count for the number of lines that match the pattern.

Here is an example where we are working in ```-written_2/travel_guides/berlitz1/IntroJapan.txt``` 

Input: ```-grep -c "Japan" written_2/travel_guides/berlitz1/IntroJapan.txt``` 
Output: ```-50```

This example would tell us the number of lines the pattern "Japan" appears in the IntroJapan.txt file. 

We can also type ```-grep -r -c "fight"  written_2/non-fiction/OUP/```, to
recursively search for the pattern "fight" in all the files in the OUP directory. 
The output would look like the following:
![grep output](https://ashishsdalvi.github.io/cse15l-lab-reports/grep_output.png)

The following commands are useful when you only want to see the counts rather than
the full sentence and files in which the pattern appears. 

**-i flag**
The ```-i``` flag is useful for a case insensitive search of a pattern in a file.
For example, the ```tree``` and ```Tree``` patterns would return the same result
when using the ```-i``` flag. 

Here is an example: 
Input: ```-grep -i "tree" written_2/travel_guides/berlitz1/WhereToJapan.txt``` 

Output (shortened for visibility): 
```pines, plum trees, canary palms, and soft green cryptomeria japonica.
Over the treetops you catch an occasional glimpse of the skyscrapers of
good place for cheaper snacks than you’ll find in the street-level
opened here in 1903. Before long, the streets and alleys around the
their pillars made from 1,700-year-old cypress trees.
the oldies on enormous boomboxes. Street food, body paint, in-your-face
greenhouse, for its flowering cherry trees in April, and for its
of it survive on the road east of town, where many of the 13,000 trees
with a motifs from nature: pine and plum trees, birds of the field, and
trees, and a cool, rushing stream. The tomb itself, a miniature bronze
trunk of a single Judas tree...```


Here is another example but this time with the -c flag to only output counts.

Input: ```grep -c -i "wine" written_2/travel_guides/berlitz1/WhereToFrance.txt```

Output: ```33```

The examples above demonstrate how to use the -i flag when you don't care about
case sensitivity which may be important when you just want to check substring counts
for example. 

**-w flag**
The ```-w``` flag is useful for only finding words rather than just substrings. Perhaps
you can use this when looking for specific words in a text rather than just substrings.


Take a look at the following example that uses the -i and -c flags without the -w flag.

Input: ```grep -i -c "tree" written_2/travel_guides/berlitz1/WhereToJapan.txt```

Output: ```50```

Input: ```grep -i -w -c "tree" written_2/travel_guides/berlitz1/WhereToJapan.txt```

Output: ```5```

In turns out that the actual word "tree" only shows up in the text 5 times. The rest of 
the times are just when tree is a substring such as in the word "street".


Here is another example of the -w flag. 

Input: ```grep -w -c "food"  written_2/travel_guides/berlitz1/WhereToFrance.txt```

Output: ```5```

In the example above, it turns out the word food only appears 5 times in the text. 


**-l flag**
The ```-l``` flag is when you want to see the files in which the pattern appears.
This is important for example if you were investigating where certain words of interest
appear so you could dig deeper into files. For example, if you wanted to learn more about
bread, you could use the -w and -l flags to find all the files where the word "bread" appears
and look into these files. 

Take a look at this example using the -l, -r and -w flags. This file recursively searches
berlitz1 for files containing the word "rope" and outputs files containing this word.

Input: ```grep -r  -l -w "rope" written_2/travel_guides/berlitz1/```

Output: ```
written_2/travel_guides/berlitz1/HandRJamaica.txt
written_2/travel_guides/berlitz1/WhatToEdinburgh.txt
written_2/travel_guides/berlitz1/WhatToJamaica.txt
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt ``` 

Here is another example.

Input: ```grep -r -l -w "money" written_2/non-fiction/OUP/Castro/```

Output: ```written_2/non-fiction/OUP/Castro/chL.txt
written_2/non-fiction/OUP/Castro/chP.txt```

This example recursively searches the Castro directory for files
containing the word "money" and outputs them.


All in all, flags are powerful additions to the grep command and can make searching for patterns
much easier. I hope you learnt something new from this post! 
