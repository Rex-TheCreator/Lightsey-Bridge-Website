## Tools/Languages Used:
- Astro         (Site structure)
- Tailwind CSS  (Site Styling)
- HTML/CSS/JS   (Programming Languages)
As a word of precaution, If you do not know these tools/languages and have not programmed before, do not modify the site structure beyond the components and other text/images

Any and all changes that make the information here invalid should be accounted for(change the documentation if you change the site structurally)

# Project Structure
You'll see the following folders and files:

```text
/
├── public/
│   └── staffpictures/
|       └── (all Lightsey staff photos)
│   └── (all other photos used on the website)
├── src
│   ├── assets
│   │   └── (not used)
│   ├── components
│   │   └── (all components used in the website)
│   ├── layouts
│   │   └── defaultLayout.astro
│   └── pages
│       └── aboutus.astro
|       └── bridgeresources.astro
|       └── index.astro
|       └── lightseyinfo.astro
|       └── moveinout.astro
|       └── needhelp.astro
|       └── styles/
|           └── global.css
└── package.json
```
## Individual Structure Documentation
#### defaultLayout.astro
Is the footer and header of the site. Is used for all pages of the site. All pages of the site "slot inside" this structure

relevant components used:
- Link - a uniform, stylized button. These are the buttons inside the header
    - "href" - insert the address of where to take the user once clicked.
- Alert - a banner like element that spans the width of the page with critically important information
    - "show" - insert "{true}" or "{false}" to show or not show the element, respectively
    - the text to show is to go inside the tags "<Alert></Alert>"
- Reminder - a banner like element that spans the width of the page with "good to know/consider" information
    - "show" - insert "{true}" or "{false}" to show or not show the element, respectively
    - the text to show is to go inside the tags "<Reminder></Reminder>"
- Divider - this is a colorful divider that spans the entirety of the page

#### aboutus.astro
a page on the website dedicated to the current Lightsey Bridge Staff

relevant components used:
- Layout - this is the "defaultLayout.astro" structure
- LtCard - this is the structure that showcases an individual of the leadership staff
    - "name" - insert name of staff member here
    - "position" - insert staff position here
    - "imageSrc" - insert source of image to be displayed. Staff images should be in the "staffpictures/" directory and images should try to keep a similar aspect ratio to the ones currently used.
- RCMCard - this is the structure that showcases an individual of the RCM staff
    - "RCMName" - insert name of staff member here
    - "RCMBuildingNumber" - insert RCM building number here
    - "visibleApartments" - insert "{true}" or "{false}" to show or not show specific apartment ranges
    - "apartments" - insert specific apartment ranges. dependent on "visibleApartments"
    - "visibleBandLink" - insert "{true}" or "{false}" to show or not show groupchat link
    - "bandLink" - insert groupchat link. dependent on "visibleBandLink"
    - "imageSrc" - insert source of image to be displayed. Staff images should be in the "staffpictures/" directory and images
- RCLCard - this is the structure that showcases an individual of the RCL staff.
    - "RCLName" - insert name of staff member here
    - "RCMBuildingNumber" - insert RCM building number here
    - "visibleApartments" - insert "{true}" or "{false}" to show or not show specific apartment ranges
    - "apartments" - insert specific apartment ranges. dependent on "visibleApartments"
    - "visibleBandLink" - insert "{true}" or "{false}" to show or not show groupchat link
    - "bandLink" - insert groupchat link. dependent on "visibleBandLink"
    - "imageSrc" - insert source of image to be displayed. Staff images should be in the "staffpictures/" directory and images

#### bridgeresources.astro
a page on the website dedicated to specific information tailored to Bridge students

relevant components used:
- Layout - this is the "defaultLayout.astro" structure
- Hoverelement - this is a "big button" that has a visual effect when hovered over.
    - "href" - insert the address of where to take the user once clicked.
    - the text to go inside the button goes inside the tags "<Hoverelement></Hoverelement>"

#### index.astro
homepage of the website. Is to have current events and other forms of outreach.

relevant components used:
- Layout - this is the "defaultLayout.astro" structure
- Instagram - this contains the embed code in an easy to use compnent
    - "link" - insert link of instagram post to be shown

other important page info:
- there is an image element that showcases an eventflyer of choice
    - "src" - has special code for the base of the website(details below). Simply put the event flyer image in the existing quotations

#### lightseyinfo.astro
a page on the website containing general information about the Lightsey Bridge community area

relevant components used:
- Layout - this is the "defaultLayout.astro" structure
- Leftinfocard - this is a structure containg a hoverable, clickable image and information on the left that spans the page width
    - "title" - insert the title
    - "imageLink" - insert link that will be opened when clicked
    - "image" - insert the link of the image to be displayed
    - all text to be shown under "title" is to be put in the "<Leftinfocard></Leftinfocard>" tags
- Rightinfocard - this is a structure containg a hoverable, clickable image and information on the right that spans the page width
    - "title" - insert the title
    - "imageLink" - insert link that will be opened when clicked
    - "image" - insert the link of the image to be displayed
    - all text to be shown under "title" is to be put in the "<Rightinfocard></Rightinfocard>" tags
- Hoverelement - this is a "big button" that has a visual effect when hovered over.
    - "href" - insert the address of where to take the user once clicked.
    - the text to go inside the button goes inside the tags "<Hoverelement></Hoverelement>"

#### moveinout.astro
a page on the website containing information about moving in and out for residents

relevant components used:
- Layout - this is the "defaultLayout.astro" structure
- Reminder - a banner like element that spans the width of the page with "good to know/consider" information
    - "show" - insert "{true}" or "{false}" to show or not show the element, respectively
    - the text to show is to go inside the tags "<Reminder></Reminder>"
- Instructioncontainer - a page-spanning structure that has a title and should include an ordered list
    - "title" - insert the title for the structure
    - if you add an ordered list, do so between the tags "<Instructioncontainer></Instructioncontainer>". Look at pre-existing Instructioncontainer structures on guidance for making these
- Simplelink - makes given text a stylized and a link
    - "href" - insert the address of where to take the user once clicked.
    - text to be made a Simplelink should go in the tags "<Simplelink></Simplelink>"
- Reminder - a banner like element that spans the width of the page with "good to know/consider" information

#### needhelp.astro
a page on the website containing quick-help information

relevant components used:
- Layout - this is the "defaultLayout.astro" structure
- Alert - a banner like element that spans the width of the page with critically important information
    - "show" - insert "{true}" or "{false}" to show or not show the element, respectively
    - the text to show is to go inside the tags "<Alert></Alert>"
- Helpcard - a structure that contains a title and information section
    - "header" - insert title
    - text goes in between the tags "<Helpcard></Helpcard>"
- Simplelink - makes given text a stylized and a link
    - "href" - insert the address of where to take the user once clicked.
    - text to be made a Simplelink should go in the tags "<Simplelink></Simplelink>"

#### global.css
a non-veiwable page that contains specific Clemson color schemes

## General Info
- This site was made using VS Code as an IDE, Node.js for a local runtime, Git and GitHub as repository technologioes, and GitHub Pages for a deployment
    - extensions used in VS Code: Astro(https://marketplace.visualstudio.com/items?itemName=astro-build.astro-vscode) and Tailwind CSS Intellisense(https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)
    - because this site was deployed on GitHub pages for free, all local links must include the base "/Lightsey-Bridge-Website/" which can be imported with "const BASE = import.meta.env.PUBLIC_BASE;" from the .env file or simply added to a local link
        - some components automatically have this and some don't
    - components can be imported to pages that don't already have them with "import [component name] from "../components/[component name].astro"
        - WARNING: not all components are drag and drop and may need the encasing tags that act as containers which are present in current instances

## Changes and updates to the website
The following is how I would go about modifying the website if I had to start the process over. If you don't know how to program feel free to change the text, images, and use of simple components on the website. If you do know what you're doing, change away but remember to document any and all changes that make the information above invalid.

- I reccommend using what I used to maske the website, which is VS Code with the extensions mentioned in general info
    - install VS code and install the extensions outlined
    - install Node.js
    - install Git
        - initialize Git and connect to GitHub
        - You'll need to have access to the repository on GitHub to initiate changes on online repository and not just your local instance
- Open/Create a folder that you want the project to "live in" while you modify the website
- Open Git Bash in the directory(folder you just made/opened)
- "git init"
- "git clone https://github.com/Rex-TheCreator/Lightsey-Bridge-Website.git"
- "code ."
    - opens VS Code in the current directory
    - make your changes
- "npm install" installs the website dependencies(Astro, Tailwind, etc.) so you can run your local instance on your own machine
- "npm run dev -- --host" hosts the website on your machine
    - you can access your local instance from any device connected to the same network with the full link given
    - you can terminate the hosting with Ctrl + C on Windows
- "git status" - to see which files have been modified
- "git add ." - to stage all files for an update
- "git commit -m "[message describing changes]"" - to make the changes an update for the local instance
- "git push" - to send the update to the online repository/deployment
