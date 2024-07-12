# Cultural Cookbook - A Spark-Y project
Website for the Spark-Y cultural cookbook project. The farm is located on WeFarm property in Minnesota.

## Table of contents
- [Todo](#Todo)
- [How is this project being created/maintained?](#how-is-this-project-being-createdmaintained)
	- [Post creation process](#post-creation-process)
 	- [Why cant i just change XYZ?](#Why-cant-i-just-change-XYZ-its-just-a-simple-google-formspreadsheet)
  	- [How does a google form submission become a post on a website?](#How-does-a-google-form-submission-become-a-post-on-a-website)
- [Steps to produce a recipe](#Steps-to-produce-a-recipe)
- [Examples of recipe format](#examples)

## How is this project being created/maintained?
I have opted for a simple pipeline that takes submissions from a google form since i am mainly working with non-technical people on this project. i am also coding simplistic code generators since i may be dealing with 100+ submissions which each need to have a page on the website.

### Post creation process:
1. Google Form (relying on the form to do the most basic data validation by imposing things like a minimum charecter limit)
2. the form submissions are then automatically entered into a google spreadsheet in specific cells.
3. spreadsheet then manipulates the data of the submission to be of a suitable format. (using simple formulas)
4. the manipulated data is then picked up by an advanced formula i wrote that essentially acts as a code generator and it constructs valid hugo style code for the submission.
5. Post each submissions unique code manually or automatically

### Why cant i just change XYZ? its just a simple google form/spreadsheet?
```mermaid
flowchart TD
    A[Change in Google Form questions/layout] -->
    B[Change in Google Spreadsheet layout] -->
    C[Change in Code Generator references] -->
    D[Change in Code Generator Output] -->
    E[Change in Code posted to site]
```
As you can see, a change to any one tool in the pipeline results in changing everything that follows.

**How does a google form submission become a post on a website?**
```mermaid
flowchart TD
    A[Chef submits recipe using google forms] -->
    B[Google spreadsheer] -->
    C[Formulas adjusts the data] -->
    D[Code Generator] -->
    E[Code generator output] -->
    F[Code posted to site]
```

## Todo (Simplified)
- [x] Create ReadMe
- [x] setup hugo site
- [x] install the Roxo theme
- [x] rewrite website code
- [x] fork the theme to change the section names and color scheme
- [x] write basic content to complete later
- [x] create example content
- [x] fix the crap i broke by forking the theme (could i have done this without formking the theme?)
- [x] fix annoying homepage title text
- [x] create pages for each cultures farming techniques
- [x] fix list and single item code for farm category
- [x] create google form
- [ ] embed google form into website? (this would be nice because then the project would continue to be updated with new recipes etc) only pay the original submissions though
- [ ] setup github action to auto create the submissions markdown file from the spreadsheet code generator


## Steps to produce a recipe
1. Type out the recipe and story
2. make the video telling the story and following the recipe
3. upload the video to IPFS/YouTube
4. embed the video within the recipe
5. upload the recipe to IPFS/Github
	1. Create a pull request for based.cooking?
6. produce shareable message (for emails, QR codes, etc)
7. Generate QR Code with sharable message (Likely using MailTo: format)

## Examples

### Example Recipe QR Code:
<img align="center" src="Docs/QR-Example.png" alt="alifelivedfully" height="500" width="500" />

### Example Recipe QR code data:
```
Za'atar Chicken Bulghur Bowls, by Joel.

This recipe has been passed down for 3 generations in my family and was made using traditional ojibwe gardening and cooking techniques.

Recipe: https://based.cooking/zaatar-chicken-bulgur-bowls/

Video: https://www.youtube.com/watch?v=dQw4w9WgXcQ

Donate: https://www.paypal.com/alifelivedfully

---

Spark-y has backed up the recipe to the InterPlanetary File System (IPFS) to ensure its access for future generations!

Local IPFS: 
http://localhost:8080/ipfs/QmcniBv7UQ4gGPQQW2BwbD4ZZHzN3o3tPuNLZCbBchd1zh

Online Gateway: 
https://ipfs.io/ipfs/QmcniBv7UQ4gGPQQW2BwbD4ZZHzN3o3tPuNLZCbBchd1zh

Monero:
4AdhfxUfFbPd11epEKsuDqBm4jJEapK9UUhgFH8ss7aSAhtox1Li4B6LZwoEuZ6W8BJUCpRynUXFCWcDUzKUd7Cr99kk4tM
```

### Example of a simplified Recipe: 
```
# Za'atar Chicken Bulghur Bowls

- ⏲️ Prep time: 10 min
- 🍳 Cook time: 20 min
- 🍽️ Servings: 4

## Ingredients

- 4 Chicken Breasts
- 1 cup Bulghur Wheat
- 1 oz Mixed Olives, drained
- 4 oz Baby Spinach, chopped
- 2 Tbsp Za’atar Spice Blend
- 2 Roma Tomatoes
- 1 Lemon
- 1/2 cup Feta Cheese, crumbled
- 2 Garlic Cloves, minced/grated
- 2 Tbsp White Vinegar
- 1 tsp Sugar
- Oil

## Video
![](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

## Story
This recipe has been passed down for 3 generations in my family and was made using traditional ojibwe gardening and cooking techniques. This recipe has been passed down for 3 generations in my family and was made using traditional ojibwe gardening and cooking techniques. This recipe has been passed down for 3 generations in my family and was made using traditional ojibwe gardening and cooking techniques. This recipe has been passed down for 3 generations in my family and was made using traditional ojibwe gardening and cooking techniques.

## Directions

1. Preheat oven to 450F. Add 1 1/2 cup water and 1/4 tsp salt to a medium pot. Cover and bring to a boil over high heat. While water comes to a boil, cut tomato into 1/4" pieces. Zest and juice the lemon.
2. Add garlic and bulghur to the boiling water. Stir to combine, remove pot from heat, cover, and let stand until bulghur is tender and liquid is absorbed (15 mins).
3. While bulghur rehydrates, pat chicken dry and season with Za’atar spice blend, salt, and pepper. Heat a large non-stick pan over medium-high heat. Add 1/2 tsp oil, then the chicken. Sear until golden-brown. Transfer chicken to a sheet and bake on the middle rack in the oven until chicken is cooked through (10-12 mins)
4. Meanwhile, whisk together vinegar, lemon juice, lemon zest, 1 tsp oil, and 1/2 tsp salt in a small bowl. Set aside.
5. When bulghur is done, fluff with a fork. Add olives, spinach, tomatoes, and half the dressing to the pot. Season with salt and pepper, then stir to combine.
6. Thinly slice chicken. Divide bulghur salad between plates, then top with chicken. Sprinkle with feta and drizzle remaining dressing over top.

## Contributor(s)

1. Joel Maxuel
	1. Github: https://github.com/joelmaxuel
	2. monero: `4AdhfxUfFbPd11epEKsuDqBm4jJEapK9UUhgFH8ss7aSAhtox1Li4B6LZwoEuZ6W8BJUCpRynUXFCWcDUzKUd7Cr99kk4tM`
	3. Bitcoin: `bc1qvpj4juacefyl6v7f6f7helggsmmxn97s7h6yzd`
```

### Example of recipe video:
![](https://www.youtube.com/watch?v=dQw4w9WgXcQ)
