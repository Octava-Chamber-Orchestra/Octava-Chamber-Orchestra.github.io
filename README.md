# The Octava Chamber Orchestra Website

The official website for The Octava Chamber Orchestra: <http://OctavaChamberOrchestra.com>

The website can be viewed at <https://octava-chamber-orchestra.github.io>.

## Basics

This website is hosted using Github pages and is built automatically by Github using the templating tool [Jekyll](https://jekyllrb.com/docs/). Every time a commit (which may be empty) is recieved on the master branch, Github will rebuild the website.

## Naming Files

Files exposed to the end user in Jekyll converts spaces filenames with dashes, so it's a good idea if we stick with the convention.

## Assets

Miscellaneous files such as images, forms, or stylesheets should be put in the `assets` folder. For certain well-structured data such as musicians or concerts, assets for them will reside along with the associated pages.

## Data

Data for various parts of the site are stored in [_data](_data/). See the data files for commented documentation.

## Collections

Collections are a feature of Jekyll that are used extensively in this website. Collections are groups of related pages that have special metadata in their front matter to help provide unique functionality. The metadata schema for each collection is described here.

### Main Pages

The main pages for the website are located in the [_main_pages](_main_pages/) folder. Each main page has an entry on the main navigation menu. To facilitate this, some metadata must be included in the front matter of each main page. The `menu_title` property specifies the text that will be dispalyed in the menu entry. `menu_order` is a number that specifies the sort order for the page's place in the menu. Higher numbers appear later in the menu.

### Sub Pages

Any miscellaneous page that should not be in the menu bar and isn't some other specific type should reside in the [_sub_pages](_sub_pages/) folder. URLs for those pages will appear in the root directory of the site. They don't have any special metadata.

### Musicians

Bios for musicians live in the [_musicians](_musicians/) folder. See the [musician example](_musicians/musician-example.md) for specifying metadata (view the source, not the rendered document).

### Concerts

Concert info pages are in the [_concerts](_concerts/) folder. See the [concert example](_concerts/concert-example.md) for specifying metadata (view the source, not the rendered document).