# The Octava Chamber Orchestra Website

The official website for The Octava Chamber Orchestra: OctavaChamberOrchestra.com

## Basics

This website is hosted using Github pages and is built automatically by Github using the templating tool [Jekyll](https://jekyllrb.com/docs/). Every time a commit (which may be empty) is recieved on the master branch, Github will rebuild the website.

## Assets

Miscellaneous files such as images, forms, or stylesheets should be put in the `assets` folder. For certain well-structured data such as musicians or concerts, assets for them will reside along with the associated pages.

## Settings

Data for various parts of the site is stored in [_data/settings.yml](_data/settings.yml). The active concert date and list of heading sponsors are stored there. See the file for further documentation.

## Main Pages

The main pages for the website are located in the [_main_pages](_main_pages/) folder. Each main page has an entry on the main navigation menu. To facilitate this, some metadata must be included in the front matter of each main page. The `menu_title` property specifies the text that will be dispalyed in the menu entry. `menu_order` is a number that specifies the sort order for the page's place in the menu. Higher numbers appear later in the menu.

### [concerts.html](_main_pages/concerts.html)

This page automatically lists concerts based off data in the concert pages and the dates specified in them.

### [musicians.html](_main_pages/musicians.html)

This page automatically lists all the musicians that have bios on the website.

## Musician Pages

Bios for musicians live in the [_musicians](_musicians/) folder. Bios must adhere to the proper file structure in order for the templates to work properly. Each musician entry should be its own subfolder. The main bio must be in a file named `bio.md`. If a photo is provided, it must be named `photo.jpg`.

The front matter properties for `bio.md` are as follows:

`title`: The title for the page and the name of the musician.

`role`: The role that the musician takes in Octava (E.g. Composer, Violist, Concertmaster).

`priority`: A number indicating the sort order for the musician on the musicians page. Lower numbers appear first, and it can be negative. Musicians with the same priority are sorted alphabetically by file name (so it is important that the folder that `bio.md` resides in reflect their name). Additionally,
any musician with a priority of 0 or higher will be marked as *Guest artist* on the musicians page.

## Concert Pages

Concert info pages are in the [_concerts](concerts/) folder. They are formatted automatically depending on whether they are in the past or future. The front matter data is as follows:

`title`: The title of the page and concert

`date`: The ISO formatted date and time of the concert. Do note that times are 24 hour.

`location`: The name of the concert venue.

`location_url`: The website for the concert venue.

`address`: The address of the concert venue.

`phone`: The phone number of the concert venue.

`poster artist`: The artist that designed the poster for the concert. This property is optional and if omitted will simply not display a poster for the concert. To display a poster but not credit an artist, set the value to "anonymous". If this property is present, a file named `poster.jpg` depicting the poster must be present in the same folder as the page.

`poster_artist_url`: The website of the poster artist. If ommitted, when displaying the artist's name, it will not link to anything.

## Sub Pages

Any miscellaneous page that should not be in the menu bar and isn't some other specific type should reside in the [_sub_pages](_sub_pages/) folder. URLs for those pages will appear in the root directory of the site.