# EdTech Metaphor Generator

[![](metaphor-screen.jpg "Generator sample screen with some kind of reference to puppies")](https://cogdog.github.io/edtechaphors/)


[A Mashup generator originally made for Martin Weller](http://blog.edtechie.net/edtech/ed-tech-metaphor-generator/). Check it out! It's a practical stick. eh?

https://cogdog.github.io/edtechaphors/

Learn more about this little experiment in [A Generator for Martin](https://cogdogblog.com/2019/09/generator-for-martin/)

## Fork and Roll

Make your own! Change out the background image and modify the structure of generated phrases. Here are ones I know of


* Open Education Metaphors by Martin Weller (featuring Teilo with a big stick!) http://metaphor.edtechie.net/
* Modified version by John Johnston (pulling the content from a google sheet, that's neat!) http://git.johnj.info/edtechaphors/?id=1Tk-IUE8OG_InI6KjZ4GAFMm4IyJl1PoZQYzHCbm4fN8
* Open Degree Metaphors by Martin Weller http://opendegree.edtechie.net/
* EdTech Pitch Machine by (again) Martin Weller https://edtechie.net/edtechpitch/

You can easily download this repo make your own copy, and hoist to your own web server or any place you can publish HTML to the web. That's your own generator, which is nice.

But these ones are part of this repo, so you can actually **contribute** to them by forking a copy (or just going to the index.html in any and click the edit button, this will generate a copy). Push the changes my way, please, make my day! Your additions will make these generators more interesting!

* Original (Extra Crispy?) EdTech Metaphors https://cogdog.github.io/edtechaphors/
* A Generator Generator (Alan goes meta) https://cogdog.github.io/edtechaphors/meta
* Creative Prompt Machine https://cogdog.github.io/edtechaphors/create
* Remix It Up in the H5P Kitchen https://cogdog.github.io/edtechaphors/h5p

## Hardly Passing For Documentation

You will need a bit of HTML knowledge to change the title, initial prompt, and adjust credits for the background image. All of the generating magic is done in JavaScript. Create arrays for all sets of phrases you want to have mixed up, this is the setup for the [original EdTech Metaphors one](https://cogdog.github.io/edtechaphors/)

       // array of metaphors- 
	  let metaphor = [
	      'baking a cake', 'a houseplant', 'running a marathon', 'raising a puppy', 
	      'quantum physics', 'visiting an unknown country',
	      'the history of porcelain manufacture',
	      'the development of New York graffiti styles','the Corn Laws',
	      'the Loch Ness monster myth','the CB radio craze of the 70s',
	      'the Gargoyles of the Notre Dame','an all you can eat “Around the world” buffet',
	      'the growth of interest in vinyl records','a comfortable old coat',
	      'knitting','Homers The Iliad','gardening','the ecosystem of a small island',
	      'your favourite film','the structure of a typical horror film', 
	      'chasing a cat', 'finding a big stick', 'a local castle', 'real hockey'
	    ];
  
  	  // array of technologies
	  let tech = [
	      'learning analytics', 'VLE', 'blockchain', 'OER', 'MOOCs', 
	      'personalised learning','Artificial Intelligence','open textbooks',
	      'automated assessment','MCQs','digital natives','connectivism',
	      'blogging','plagiarism detection sites','lecture capture',
	      'Flipped Learning','Facebook','academics use of Twitter',
	      'open access publishing','mobile learning','learning styles',
	      'LMS','e-portfolios','Wikipedia','student-generated content'
	];

You can rename these and make up new ones. That is one level or randomization, think of these as placeholders that can be mixed up.

The second level of randomness is done by creating a set of different sentences that will make sense using a random element from any of the arrays. This set needs to be enclosed in back tick characters for the variable to work -- `${metaphor[random(metaphor)]}` will provide a random metaphor from the first array above.

      	 let options = [
	  	   `Use ${metaphor[random(metaphor)]} as a metaphor for ${tech[random(tech)]}.`, 
		   `How is ${metaphor[random(metaphor)]} an analogy for ${tech[random(tech)]}?`, 
		   `What does ${metaphor[random(metaphor)]} tell us about ${tech[random(tech)]}?`,
		];
The more of these you make, the more random your generator becomes (3 is a minimum, 5 or more is better, 10 is just wildly fantastic).

## As if Versioning Happens by Magic

* Oct26, 2021: Updated Bootstrap, jQuery, Backstretch.js versions, tweet code extracts URL from HTML href links in a generated message, re-organized code and fitted with more descriptive comments, created 2 more demos
* Oct 19, 2021: Just for fun (and to test that links work) made a generator that generates generators
* Jan 27, 2021: Added randomized button names, and a tweet this button
* Sep 25, 2019: First version started up



