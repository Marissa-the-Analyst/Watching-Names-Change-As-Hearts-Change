# Watching-Names-Change-As-Hearts-Change
Evolving from enemies to lovers, Violet Sorrengail and Xaden Riorson of Rebecca Yarros’s Empyrean series navigate a relationship shaped by war, trauma, and inexperience. In this analysis, I examine how Xaden’s changing perception of Violet is reflected through the names he uses for her over time. 



https://github.com/user-attachments/assets/4c385640-d5c2-4ccf-b860-3ca0d7f62cc5



### Finished product ### 

If you’d like to view the dashboard yourself, [click here]() 

### Spoiler Warning ### 

This write up contains spoilers from Fourth Wing -> Onyx Storm 

### Inspiration ### 

I can’t pin down the exact inspiration, but I remember seeing a Tableau viz where a scatter plot was used and every single point represented something specific. When you look at it from a distance, the larger trend became clear. <br> 

On a personal note, I’ve always thought the use of names is a really cool cultural behavior that we don’t talk about enough. They’re a lot like smells in that way; each one means something different to someone else. For some people, calling someone “Mr.” or “Mrs.” is purely formal; for others, only being addressed by their legal first name feels shallow. And, like smells, context matters. Hearing a stranger call someone “Babe” can be uncomfortable, but from a partner it’s perfectly normal. So of course, I jumped at the chance to dig into this idea further with ***The Empyrean***. <br> 

I also just genuinely enjoy ***The Empyrean*** series so far! I relate to the dynamic between Xaden and Violet, where there isn’t a clear “wrong” side, just two people shaped by very different perspectives and upbringings. You want to root for them, but you also know it’s entirely possible, and potentially heartbreaking, that they might not work out. That tension is what keeps me hooked. <br> 

Back on the data side, during my gum gum dataset project, I stumbled onto [Brittany Rosenau’s tutorial for creating an overlay](https://brittanyrosenau.medium.com/create-a-dashboard-overlay-entirely-in-tableau-a8e9543979e5). I immediately realized it would be **perfect** for what I wanted to do here. 

 

### Programs Used ### 

- Excel for Data Collection and Cleaning 

- Tableau for Data Visualization 

- Microsoft Word and Krita for minor graphical adjustments 

### Scope of Work ### 

**Deliverables** <br> 

- A dataset with every instance of Xaden referring to Violet *excludes Xaden Chapters 

- A Dashboard exploring the levels of formality and how they change with impactful moments across the series “Timeline” 

### Goals ### 

I wanted to see the change over time visualized. I also wanted to nail a Valentines Viz that had a clear data story and wasn’t too complicated. Something I learned in my gumgum project was that going into a data story just to “see what happens” can be a bit tricky to explain to a general audience. Because instead of saying 1 + 1 = 2, you’re saying 1 + 1 might equal 2 in these circumstances, but did you know 1 + 2 also equals 3? By not having a narrow enough scope, the audience is left overwhelmed by all the findings.  

So, my goal was to keep it simple, try a new chart style, and try out that annotation overlay! 

### Data Source and Collection ### 

After finishing Onyx Storm and seeing Xaden call Violet, “Love” (my heart!), I knew I wanted to better visualize that. I decided to do a light re-read and check for every instance of the different name references in each chapter. Using that, and a combination of CTRL-F. I flew through the 3 books. I decided to exclude chapters where he’s the main character since he’s primarily just thinking about her. I remembered to make an additional table that contained each book and listed all the chapters whether he referred to her or not so I could build a chapter timeline easier. Finally, I had an “important moments” tab to help me include important plot points that would impact their relationship or the overall plot. 

### Viz Design and Creation ### 

I stumbled into creating this viz correctly. It was one of those rare moments where I half followed a few tutorials and came out the other side with exactly what I wanted in like 3 hours instead of 12 hours lol. My first attempt looked like this: 

<img width="745" height="633" alt="image" src="https://github.com/user-attachments/assets/f192225f-221a-43e8-83af-02ebc07d66e4" />


I don’t know what's going on here, but I think it was the result of overcomplicating a few things and trying to get the chapters in the right order... Sometimes it’s just easier to start again on a new sheet. <br> 

<img width="993" height="696" alt="image" src="https://github.com/user-attachments/assets/fc087eb3-9b96-4994-aab8-b67ebb27e2df" />

This is the main sheet with the star of the show, the jitter calculation. The Jitter calc is what assigns the name values random spacing along the y axis of the viz. Using the size mark, we get the variations in size based on usage frequency per chapter.  <br> 

I drafted the hearts in Microsoft Word and used Krita to recolor them to the darker pink using the hex code from the original color palette, marking the highest form of endearment. I did the custom axes for each book’s varying chapter lengths by assigning the range to custom and “independent” endings but fixed starts a 0. I’ve also been enjoying expanding on using tool tips to aid the user and eliminate any ambiguity that may cause confusion. <br> 

The highlighter was the first time I used dashboard highlight actions and felt like they worked well! Plus, I was able to add the overall name counts which is just helpful to view the overall distribution of names. <br> 

<img width="700" height="708" alt="image" src="https://github.com/user-attachments/assets/f7b64f0e-10dc-4acd-8625-c5c3c2eb0cda" />


The overlay was made following the tutorial Brittany provided. None of the annotations were built on the sheet but instead, they were built on the dash itself. It was also another instance of the importance of container/floating container management/usage. I was having trouble seeing my tool tips on the timeline above the invisible floating container, even though it was hidden. It turns out this was because the Show/Hide button was “below” the floating container’s hierarchy. <br> 

<img width="223" height="326" alt="image" src="https://github.com/user-attachments/assets/c35d68bb-4631-4100-b170-74c6490e9a3f" />


By moving it above, things worked again! This troubleshooting is just a small example of how practice and doing can help cement those fundamentals that aren’t always explicitly clear when you learn them the first 20 times lol. <br> 

Also, I used point annotations at first for each circle, but then I realized the Random Jitter changes the placement of the points every time the viz is loaded 🙁. This meant using Area annotation was more appropriate for capturing all of the points from that chapter. But it was a lot more work for me. <br> 

Playing with color and fonts in this viz very straightforward! I knew I wanted to use a Times New Roman font to match the “book” style. And the color scheme was simple since it was meant to be romantic. <br> 

I did struggle a bit with the color scheme overlay though. I needed the container to be clearly represented as “on” and the annotations to be visible/readable but not too “in the way”. I also took the opportunity during my annotation to rework from points to areas, to color code the events based on vibes. Positive relationship events were denoted with a pink and white, lighter color scheme. Plot points and trust damaging situations were denoted with darker colors. <br> 

It also took a few iterations to come up with the person speaking with the heart coming out of their mouth icon. Xaden, as a fictional character, is going to look different for everyone, and I didn’t want to shatter that illusion. I spent a lot of time looking on Flat Icon for a good example of someone in love and speaking, but I wasn’t really happy with any of the options. I drafted the image in Word using the shape tools and then removed the background for seamless integration into the dashboard.  

### Opportunities ### 

This Viz is meant to be simple. It took an effort to keep it that way. I wanted to include the average amount of times he referred to her per book, but there wasn’t a clean way to include it. Additionally, I think having the name counts on the highlight change and allowing the user to select the book title to highlight that book/filter, could’ve been a way to take the visualization further. But to avoid overcomplicating things, I kept it simple.  

### Reflection ### 

This project filled me with a lot of confidence. It came together quickly after the gum gum project, and I couldn't help but grin ear-to-ear while building it. Mainly because for once, the viz I had in my mind matched the viz I actually built! I definitely want to continue it into the other books in the series. I’m really proud of this one.  
