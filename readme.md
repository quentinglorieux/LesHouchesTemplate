# How to use the Hugo - Les Houches template

## Installation

### Clone the git repository

`git clone https://github.com/quentinglorieux/LesHouchesTemplate.git`

### Install Hugo (optional)

If you want to run the website locally, you need to install Hugo.
All infor are at [https://gohugo.io/installation/](https://gohugo.io/installation/)

### Run it locally (optional)

hugo serve

## Edit the content

### To edit the configuration

- Edit `config.yml` file with your infos
- You can set the sections you wanna see on the site and the order of the sections (and names)
- Sponsors are on this setting file too

### To setup the program frame

- Create a google sheet with the program with this template : `https://docs.google.com/spreadsheets/d/1XKBXFj4kCM-Yz2_ooxKrMc7BndZmUIUq8P0KSL2Ur18`
- Fill it
- Publish it to the web (File > Share > Publish to the web) with settings Link, Web page, Entire document.
- Copy the link given something like : `https://docs.google.com/spreadsheets/d/e/2PACX-1vTjnc1gJo4n7BBSMa8jDMq7BS0HrsaNp_Xj6oaGOYgOS3hjNVnSybOcNvQiCMyw0Atqr4ejaD7yIbcR/pubhtml`
- edit data/schedule.yaml with the link
  `url : https://docs.google.com/spreadsheets......`
- if you have a problem of size you could change it in `layouts/partials/schedule_partial.html`



### Data and images

- Images are stored in `static/img/`

- Speakers infos are in data/speakers.yaml
- Topics are in data/topics.yaml

- Other files should not be edited (unless you know what you are doing)

## Setup the registration form

- Create an account on `sheetdb.io` using your google account
- Create a new spreadsheet from JSON using `https://lab.quantumoptics.fr/assets/json/houches.json` ![image](/themes/hugo-conference/assets/json.png)
- Copy the endpoint URL given by sheetdb.io and paste it in the `config.yml` file : `sheetdbEnpointURL:`
- All registrations will be sent to the google sheet.
- Optional : You can use google sheet to send emails to the participants.

## Deploy on a free static hosting (Netlify)

- Create a new repository on GitHub and push the code to it.
- Create an account on Netlify and link it to your GitHub account.
- Connect to Netlify and link your repository to it.
- If needed: set the build command to `hugo` and the publish directory to `public/`



# For Developpers

## How to register  (with Netlify form and Zapier)

- First you need to duplicate the repo
- Then modify it and push to GitHub
- Link it to Netlify : command hugo, directory public
- Check the form ID to collect in Netlify forms (after enabling it)
- Connect to Zapier and link your form to a google sheeet
- Link to your domain:
    - Go to domain management in  Netlify > Site
    - Add a domain alias
    - Do it in OVH (or somewhere else) with a CNAME towards Netlify site adress
    - Go to Netlify Domain > Register the subdomain
    - Ask for a certificate 


## Edit the template

Most of the configuration can be found in the config.yml file.
Edit this to access most of the parameters.



## Run it locally
hugo serve

