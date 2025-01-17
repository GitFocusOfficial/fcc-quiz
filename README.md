# Learn Accessibility by Building a Quiz

Accessibility is making your webpage easy for all people to use – even people with disabilities.

In this course, you'll build a quiz webpage. You'll learn accessibility tools such as keyboard shortcuts, ARIA attributes, and design best practices.

## Step 1

Welcome to the first part of the Accessibility Quiz. As you are becoming a seasoned HTML and CSS developer, we have started you off with the basic boilerplate.

Start this accessibility journey by providing a lang attribute to your html element. This will assist screen readers in identifying the language of the page.

## Step 2

You may be familiar with the meta element already; it is used to specify information about the page, such as the title, description, keywords, and author.

Give your page a meta element with an appropriate charset value.

The charset attribute specifies the character encoding of the page, and, nowadays, UTF-8 is the only encoding supported by most browsers.

## Step 3

Continuing with the meta elements, a viewport definition tells the browser how to render the page. Including one betters visual accessibility on mobile, and improves SEO (search engine optimization).

Add a viewport definition with a content attribute detailing the width and initial-scale of the page.

## Step 4

Another important meta element for accessibility and SEO is the description definition. The value of the content attribute is used by search engines to provide a description of your page.

Add a meta element with the name attribute set to description, and give it a useful content attribute.

## Step 5

Lastly in the head, the title element is useful for screen readers to understand the content of a page. Furthermore, it is an important part of SEO.

Give your page a title that is descriptive and concise.

## Step 6

Navigation is a core part of accessibility, and screen readers rely on you to provide the structure of your page. This is accomplished with semantic HTML elements.

Add a header and a main element to your page.

The header element will be used to introduce the page, as well as provide a navigation menu.

The main element will contain the core content of your page.

## Step 7

Within the header, provide context about the page by nesting one img, h1, and nav element.

The img should point to https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg, have an id of logo, and have an alt text of freeCodeCamp.

The h1 should contain the text HTML/CSS Quiz.

## Step 8

A useful property of an SVG (scalable vector graphics) is that it contains a path attribute which allows the image to be scaled without affecting the resolution of the resultant image.

Currently, the img is assuming its default size, which is too large. CSS has a max function which returns the largest of a set of comma-separated values. For example:

Example Code

```img
img {
  width: max(250px, 25vw);
}
```

In the above example, the width of the image will be 250px if the viewport width is less than 1000 pixels. If the viewport width is greater than 1000 pixels, the width of the image will be 25vw. This is because 25vw is equal to 25% of the viewport width.

Scale the image using its id as a selector, and setting the width to be the maximum of 10rem or 18vw.

## Step 9

As described in the freeCodeCamp Style Guide, the logo should retain an aspect ratio of 35 / 4, and have padding around the text.

First, change the background-color to #0a0a23 so you can see the logo. Then, use the aspect-ratio property to set the desired aspect ratio to 35 / 4. Finally, add a padding of 0.4rem all around.

## Step 10

Make the header take up the full width of its parent container, set its height to 50px, and set the background-color to #1b1b32. Then, set the display to use Flexbox.

## Step 11

Change the h1 font color to #f1be32, and set the font size to min(5vw, 1.2em).

## Step 12

To enable navigation on the page, add an unordered list with the following three list items:

- INFO
- HTML
- CSS
  
The list items text should be wrapped in anchor tags.

## Step 13

The child combinator selector > is used between selectors to target only elements that match the second selector and are a direct child of the first selector.

This can be helpful when you have deeply nested elements and want to control the scope of your styling.

Use the > selector to target the unordered list elements within the nav elements, and use Flexbox to evenly space the children.

## Step 14

As this is a quiz, you will need a form for users to submit answers. You can semantically separate the content within the form using section elements.

Within the main element, create a form with three nested section elements. Then, make the form submit to https://freecodecamp.org/practice-project/accessibility-quiz, using the correct method.

## Step 15

To increase the page accessibility, the role attribute can be used to indicate the purpose behind an element on the page to assistive technologies. The role attribute is a part of the Web Accessibility Initiative (WAI), and accepts preset values.

Give each of the section elements the region role.

## Step 16

Every region role requires a label, which helps screen reader users understand the purpose of the region. One method for adding a label is to add a heading element inside the region and then reference it with the aria-labelledby attribute.

Add the following aria-labelledby attributes to the section elements:

- student-info
- html-questions
- css-questions

Then, within each section element, nest one h2 element with an id matching the corresponding aria-labelledby attribute. Give each h2 suitable text content.

## Step 17

Typeface plays an important role in the accessibility of a page. Some fonts are easier to read than others, and this is especially true on low-resolution screens.

Change the font for both the h1 and h2 elements to Verdana, and use another web-safe font in the sans-serif family as a fallback.

Also, add a border-bottom of 4px solid #dfdfe2 to h2 elements to make the sections distinct.

## Step 18

To be able to navigate within the page, give each anchor element an href corresponding to the id of the h2 elements.

## Step 19

Filling out the content of the quiz, below #student-info, add three div elements with a class of info.

Then, within each div nest one label element, and one input element.

## Step 20

It is important to link each input to the corresponding label element. This provides assistive technology users with a visual reference to the input.

This is done by giving the label a for attribute, which contains the id of the input.

This section will take a student's name, email address, and date of birth. Give the label elements appropriate for attributes, as well as text content. Then, link the input elements to the corresponding label elements.