Learn GeoJSON (and build cool collaborative datasets!)
=============

Learn GeoJSON is a project to learn about the GeoJSON data format using git, GitHub, and geojson.io. It can be taught as a standalone exercise, or can be used to build real live collaborative datasets! There are a few in here to get you started.

The following sections are intended for absolute beginners. If you'e an intermediate or advanced user, great! Skip to the section where you're having trouble or need instructions.

## About

### What is this project?

The goal of this project is to build an awesome, collaborative map, showing off cool places, generated by the people who live in those places... but really it's an accessible way to learn about git, GitHub, and GeoJSON. It uses git for version control, GitHub to house the data, and provides editing examples using [geojson.io](http://geojson.io), a great tool for editing GeoJSON files.

### What this is:

- A tool to teach about GeoJSON, git, and GitHub in an easy and accessible way.
- A way to learn about git and GitHub without using the command line.
- A collaboration technique for building crowd-sourced geographic datasets.
- A gentle introduction to GitHub for beginners.

### What this is not:

- A git tutorial. 
- An overview of how to use git in the command line.
- Comprehensive.
- Scalable.
- A silver bullet.

## Background Knowledge

### What is GeoJSON?

[GeoJSON](http://geojson.org/geojson-spec.html) is an open and popular geographic data format commonly used in web applications. It is an extension of a format called [JSON](http://json.org), which stands for *JavaScript Object Notation*. Basically, JSON is a table turned on its side. GeoJSON extends JSON by adding a section called "geometry" such that you can define coordinates for the particular object (point, line, polygon, multi-polygon, etc). A point in a GeoJSON file might look like this:

    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [
          -122.65335738658904,
          45.512083676585156
        ]
      },
      "properties": {
        "name": "Hungry Heart Cupcakes",
        "address": "1212 SE Hawthorne Boulevard",
        "website": "http://www.hungryheartcupcakes.com",
        "gluten free": "no"
      }
    }
    
GeoJSON files have to have both a `"geometry"` section and a `"properties"` section. The `"geometry"` section houses the geographic information of the feature (its location and type) and the `"properties"` section houses all of the descriptive information about the feature (like fields in an attribute table).

### What are git and GitHub?

[Git](http://git-scm.org) is a tool that allows multiple people to work on the same files at the same time without overwriting each other’s changes. This general concept is called *version control*, and git is a *version control system*. There are several other version control systems out there, but git is popular because it does its job more efficiently than many (if not all) of the others.

In order for multiple people to work on a project, the data has to live in a place where multiple people can access it. [GitHub](http://github.com) is one of those places: the site houses thousands and thousands of projects, in individual workspaces called *repositories*, or *repos*, that multiple people can access, copy, edit, and update using the tools available via git. (Guess what: You're inside of a repo right now!) These repositories also have a tracking element; when someone makes a change to a project, or a *commit*, information is stored about the user, the time, the exact changes that were made (all the way down to the individual line inside the file!), and a unique ID that allows the project owner to restore back to that particular moment.

### Why are we using GitHub and GeoJSON?

[Tom MacWright](http://www.mapbox.com/about/team/#tom-macwright) over at [MapBox](http://mapbox.com) has built an amazing, browser-based tool for editing GeoJSON files called [geojson.io](http://geojson.io). Using some of the great tools available via [MapBox.js](http://www.mapbox.com/mapbox.js/api/v1.3.1/), [Leaflet](http://leafletjs.com), and some [internal GitHub functionality](https://github.com/blog/1528-there-s-a-map-for-that), geojson.io allows users to easily edit and create geographic data in the browser.

## The Basics

### Awesome! How do I contribute?

There are a few things that are required for you to contribute to this dataset. First of all, you need to make yourself a GitHub account, if you don't have one already. It's free and easy to set up, and should take less than five minutes.

I would also advise downloading [git](http://git-scm.org). Click the link and download the recommended version.

Beyond that, there are two main ways to contribute to this dataset: one is to **edit existing files** by adding points to them. The other is to **add your own files** to the repository and make them available for editing. There are step-by-step instructions for doing each of these, below.

## Editing Existing Files

These are the files that are currently in the repository and can be edited:

  - [pdxplaces.geojson](https://github.com/lyzidiamond/learn-geojson/blob/master/geojson/pdxplaces.geojson): Cool places in Portland (dummy dataset for practice)

1. If you haven't done so yet, get yourself a [GitHub](http://github.com) account and download [git](http://git-scm.org). (These instructions don't use git on the command line, but many of these principles can be used and mirrored with git in the command line.)
2. If you're using the Chrome browser, download the [geojson.io Chrome extension](https://chrome.google.com/webstore/detail/geojsonio/oibjgofbhldcajfamjganpeacipebckp). This will allow you to click through directly from your GeoJSON file to geojson.io.
3. Once you're all logged in to your GitHub account, navigate over to the [learn-geojson](http://github.com/lyzidiamond/learn-geojson) repo and press the button at the top that says Fork. *Forking* a repo makes a copy of it that is all yours. Head on over to github.com/[yourusername]/learn-geojson. This is your copy of the repo!
4. In *your* copy, click through to the file you want to edit. You should see a nice little map showing the points in the dataset. Just for fun, click on one of the points. A popup appears with attribute information for the point! Neat, huh?
5. **If you're using the Chrome extension**, you will see a little button that says geojson.io. Click on it. The GeoJSON file is now open and editable in geojson.io. **If you're not using the Chrome extension**, head on over to [geojson.io](http://geojson.io). Click Open on the top, click GitHub on the top, navigate through to the GeoJSON file you want to edit, and press Open. The GeoJSON file is now open and editable in geojson.io.
6. Add a point. Add some attributes for that point.
7. Notice that above your "attribute table" there's a little button that says "</> JSON" on it. Go ahead and click on that.
8. This is GeoJSON! Take a look at the last point in the list. It's the one you just created! Each of your attributes is in the "properties" section, and there are coordinates for where you placed the point housed in the "geometry" section. You can edit the properties and geometry directly in the GeoJSON view. If you edit the GeoJSON directly and make a mistake, use [GeoJSONLint](http://geojsonlint.com/) to find errors. What you're doing is adding some lines of code to a .geojson file! This will be important later.
9. Add as many more points as you want. Seriously. Go to town.
10. When you're done adding points, click Save on the top bar. A small box appears asking for a "Commit message." Type in a short description of the points you added and press Commit.
11. Once you've done that, a little box pops up in the same area that says, "Changes committed to GitHub:" followed by a series of numbers and letters. Click on the numbers/letters.
12. This is a list of all of the commits for the repository. This list will include not only the commits you've made, but also all of the commits that were made to the dataset before you forked it.
13. Click on the number/letter combination for your most recent commit.
14. This is why git is so neat: GitHub is showing you the exact lines that were changed in the GeoJSON file with a nice little comparison between the line you changed before you committed, and the line after.
15. Click back out to your version of the repo. In the right column, click Pull Requests.
16. A [pull request](https://help.github.com/articles/using-pull-requests) allows the user of a forked repo to push her changes back up to the original repo. For collaborating on datasets, it's a pretty cool tool! Click the green button that says "New pull request" at the top.
17. A screen pops up showing any commits you've made to the repository since you forked it and any changes you may have made to any files in the repository. This is to show you what you're asking the owner of the repo to change and/or include. If it all looks good, click the link at the top that says "Click to create a pull request for this comparison."
18. Give your request a title (something along the lines of "Adding Jessica's places!") and a short description of what you added. When you're ready, click the green "Send pull request" button.
19. Once the repo owner has approved your pull request, GitHub will tell you that your request was merged. Then your changes will be reflected in the parent dataset!
20. Click back over to the repo you forked from, click through to the geojson file you edited, and take a look. Your points will have been added to the original dataset. Congratulations!

## Still to do

These are the things that haven't been written/completed yet:

- Instructions for adding a new geojson file.
- An example using a GitHub gist.
- Settling on a desired schema for datasets.
- A tutorial for using this data in custom maps.
