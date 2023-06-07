# THE NEST
> Frontend Repository! Includes cool animations and very cool features like weather analyzer and binary convertor!
## About our Project!
Our project is mainly run on another device, a CrowPi, which we have connected to from our backend. Our project involves a binary convertor and a weather analyser which analyzes any city's weather and returns it to you. With the bianry code you can enter any number from the backend which will send that response to the crowpi and print it on the display screen. The weather feature uses an API. The user enters a city name or zipcode of any city/area around the world, after they enter it, it get the data accordingly from the API and sends the response back to the user in the form of a table. The location name is sent to the CrowPi and displayed on the LCD.


## About Us!
Our teams consists of two sophomores from Del Norte High School.
Meet the team: Haseeb Beg and Ananya Gaurav. 
The main reason we wanted to do this project was because we wanted to challenge ourseleves with something new. Working with a CrowPi was defienlty a challenge but it did teach us many things and it was really fun seeing the CrowPi get the data from the backend and display it on the screen. The binary convertor is Haseeb's feature while the weather feature is Ananya's. 

## What inspired us?
### Haseeb:
 Many things inspired me to develop this project. For one, in the future, I plan to use my CS experience to code hardware, and I figured this was a great entryway. I felt as if by taking on this hardware-based project, I was getting closer to my dreams and aspirations with CS, and that made me properly excited. Unlike other projects I've done in and out of school, this seemed to really pique my interest because it was something I was actually interested and passionate about. In other words, it was right up my alley.  Additionally, I chose this project because I wanted to work on something that not many other people were even thinking about. I wanted to create a Night at the Museum project that would make spectators go "WOW!" I thought about how in the future, I want to develop an innovative product that when shown off in a keynote or tech expo, people would write headlines about. 

### Ananya: 
 When I first saw my partner, Haseeb, with the CrowPi device, I was immediately intrigued, because it was a machine I had never seen  before. What shocked me more was that it was capable of being controlled remotely from different locations. The various devices and features, like the speakers and display board, also  really fascinated me. So when I got the chance to work with Haseeb I got excited as I knew it was a lot different compared to what other people in CSP were doing. The feature itself was really fun to do, I really love traveling and wish to travel around the world more when I grow up, so I thought a weather feature would be really cool to do as it involves learning about the different weather patterns in different parts of the world.  Additonally, as someone aspiring to pursue a career in computer science, this experience allowed me to explore beyond coding and learn about different aspects of technology. Working with APIs and the CrowPi was a cool opportunity to really explore and learn new things. It raised my interest in CS a lot more as I realized CS has more than just code code code, it heightened my interest in computer science even more and im excited to pursue a future in CS, where I can continue to explore new things.


## Here are some other links that will be helpful for you!
Backend: https://github.com/h4seeb-cmd/CRPiBackend
Themes: https://jekyllthemes.io/q
Weather API: https://rapidapi.com/apininjas/api/weather-by-api-ninjas/
Binary 1: https://github.com/nighthawkcoders/APCSP/blob/master/_posts/2022-11-14-AP-binary_logic.md
Binary 2: https://github.com/nighthawkcoders/APCSP/blob/master/_posts/2022-07-07-PBL-binary.md


# How to use the project.
You can use this project any way you want! Somethings to do with this is maybe adding more to the weather api. The api also works with country and state names, so you could integrate that into the code and make the output a little different, maybe it could read out the data from the CrowPi? For the binary code maybe change or add a little more to the code so it lights bulbs on the CrowPi.



## Usage
Follow these steps to get this repository!

1. Midnight Theme. Use the GitHub Pages [Midnight Theme](https://github.com/pages-themes/midnight/blob/master/README.md) as a resource.  This project started with customization of _layouts/default.html from the Midnight Theme.  If you wanted to use a different [GitHub Pages Themes](https://pages.github.com/themes/), you would similarly change `_layouts/default.html` from repo used to support that theme.  Observe comment at top of _layouts/default.html ...

```html
<!-- 
  _layouts/default.html
  customization to original Midnight theme 
  found through GitHub Pages Themes
 -->
```

2. Preview Site (Option A) - [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll).  This instruction provides instructions for ruby `Gemfile`,`bundle install`.  As an addition add `.gitignore` to avoid seeing build files in commit.   After pre-requisites run this command to obtain prompt for web server ...

```bash
bundle exec jekyll serve -H 0.0.0.0 -P 4001 # -H and -P are optional
```
3. Install Nix and run using a Nix shell (Option B).  This should be quicker than Docker and more reliable than previous.

```bash
sh <(curl -L https://nixos.org/nix/install) # installs nix requires root password

# restart terminal as shell is updated, then cd ~/vscode/project-dir assuming you have it cloned

nix-shell # start shell, aka nix os virtual environment
code . # activate VSCode in current directory

# open vscode terminal

bundle install # only need to run once, first time. If this command doesn't work, delete your github repo, and reclone it. 

bundle exec jekyll serve # run server

bundle exec jekyll serve --livereload --force_polling # if you are on WSL/windows and the above command doesn't work, try this.

```

4. Preview Site (Option C) - [GitHub Pages Ruby Gem](https://github.com/github/pages-gem) has additional information on making a local server.  Ruby requirements are the same: `Gemfile`,`bundle install`.   This README looks like basis of FastPages `make server` as it uses Docker and shows how to setup a `Makefile`.

5. Customizing style (CSS).  This project uses `/assets/css/style.scss` as the location to customize your CSS. To avoid warnings in VSCode make sure you install `SCSS IntelliSense` plugin.  To understand default style, make sure you ***Preview Site*** and refer to build generated `_site/assets/css/style.css` (this is worth 1000 lectures).  For the reunion site `gallery.md` uses custom style from `assets/css/style.css` to support 3 images per row.  Observe file and position of import and custom CSS, order is important as clarified in Midnight Theme readme. ...

```css
---
---

@import "{{ site.theme }}";

/* "row style" is flexible size and aligns pictures in center */
.row {
    align-items: center;
    display: flex;
  }
  
  /* "column style" is one-third of the width with padding */
  .column {
    flex: 33.33%;
    padding: 5px;
  }
```

