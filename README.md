# Web Dev Starter Code

## Overview

For this project, we were presented with a fictional nature site displaying a "factual" article about bears. As it stood, it had a number of accessibility issues — our task was to explore the existing site and fix them to the best of our abilities while answering the questions given below in the section for Accessibility Lab Answers.

## Sources and Credits

Here I utilized sources provided by the Professor for reading along with resources for testing color contrast, tables in general, hiding a text label, differentiation between visible and nonvisible labels, and making the website accessible with tab and enter features.

Below is the list of resources used for this project:

- Color Contrast Tester: https://webaim.org/resources/contrastchecker/
- Tables: https://www.w3schools.com/html/html_tables.asp
- Hiding A Text Label: https://www.w3.org/WAI/tutorials/forms/labels/#hiding-label-text
- Visible and Nonvisible Labels: https://dequeuniversity.com/rules/axe/3.5/label-title-only
- All Provided Readings: https://developer.mozilla.org/en-US/docs/Learn/Accessibility/What_is_accessibility
- Connect Button to Tab and Enter: https://www.google.com/search?q=The+show%2Fhide+comment+control+button+is+not+currently+keyboard-accessible.+Can+you+make+it+keyboard-accessible%2C+both+in+terms+of+focusing+it+using+the+tab+key+and+activating+it+using+the+return+key%3F&rlz=1C1GCEA_enUS1072US1072&oq=The+show%2Fhide+comment+control+button+is+not+currently+keyboard-accessible.+Can+you+make+it+keyboard-accessible%2C+both+in+terms+of+focusing+it+using+the+tab+key+and+activating+it+using+the+return+key%3F&gs_lcrp=EgZjaHJvbWUyBggAEEUYOdIBBzQxOGowajeoAgiwAgE&sourceid=chrome&ie=UTF-8


## Accessibility Lab Answers

# Color
I ultilized a tool (above in the sources) for color contrast in which when I tested the text and background color against each other (green and a black), I got a Contrast Ratio of 2.79:1 which failed the Normal Test WCAG AA and AAA tests and the Large Text WCAG AA and AAA tests. 

So I changed the background color to white and then did another test. The contrast ratio came back at 14.35:1 in which passed both the Normal Test WCAG AA and AAA tests and the Large Text WCAG AA and AAA tests.

# Semantic HTML
When I try accessing the website using the keyboard I can hope around to all the different sections in the navigation panel, the links to other articles on the right, and then traverse the audio file at the bottom. If I want to click into any of these things, I have to use the space bar which does allow my to play and pause the audio through the use of that. Other than that, there isn't much other interaction that I can do with the website.

To update the article text, I:
Replaced font[size="6"] with h1 class="articleheadcomm" in both HTML and CSS
Replaced font[size="7"] with h1 class="websiteheader" in both HTML and CSS
Put <p></p> tags around the individual sections of text
Replaced font[size="5"] with h2 in both HTML and CSS

Instead of using the div[class="nav"], I replaced it with the nav semantic element for this section to make it clearer exactly what that component is.

# The Images
Yes, so the way I fixed this was to add alt attribute describing the picture in case it doesn't show up it provides the jist of the picture. Then I added a title attribute which allows me to place a description on the screen if the user hovers over the picture.

# The Audio Player
If the person is hearing impaired(deaf), I was able to add a transcript that they can access so even though they can't hear the audio they can still read it. Here i utilized alot from the transcript example done in the reading.

Since the audio player isn't accessible to them because they are using older browsers, I'd add a link directly to the audio so that they could still listening to it.

# The Forms
Replaced font[size="6"] with h1 class="articleheadcomm" in both HTML and CSS and Added <label> tags around Your comment: and Your name: with appropriate values for connecting the label to the visual text labels.

I was able to add a label to the Search button at the top by adding an aria-label="Search" so that is conveys the control function however it is not displayed to for the visual user. So this supports screen readers without disrupting from the visual user.

I was able to add a label for="name" and label for="comment" to the your name and your comment text labels binding their visual text labels to their labels themselves.

# The Show/Hide Comment Control
In order to get this to work, I needed to add into the HTML on the div class="show-hide" another attribute called tabindex="0" in which case allows tab to me used to access the element. Then I went into the Java script and created an addEventListener function that when a key is pushed down created an event and when that event.key is equal to the "Enter" button it would activate the comments panel revealing the comments panel.

# The Table
For the table I changed the elements under the first tr to th scope="col" that way the table would display them as header columns. I also added th scope="row" to the first element in the following two rows to display the different types of bear in bold as well. I also added a table summary describing the table.

# Other Considerations
Another component to make this website more accessible would be to create your own controls for the audio file as it did in the reading. This would give your user more control over the audio when to stop and pause, fast forward or backward and so forth. 

Another improvement would be adding some highlights to the navigation panel to distinguish which section your on or going to click. The same with the Related articles panel. I actually implemented a both which as you hover over the navigation you can see a blue background specify where you are in the panel. Also the related the underline disappears if you hover over it.
