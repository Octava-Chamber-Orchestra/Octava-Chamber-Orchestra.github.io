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

Bios for musicians live in the [_musicians](_musicians/) folder. Here is an example frontmatter for a musician bio:

```YAML
# The name of the musician
title: Example Musician

# Their role / instrument in Octava
role: Composer

# Set this to true to show a photo with the same file name, but with the `.jpg` extension.
# If no photo is available, then omit this property.
photo: true

# Set this to true to show this musician on the guest artist page. Otherwise omit.
guest_artist: true

# Set this to true to show this musician on the musicians page. Otherwise omit.
octava_musician: true

# The order of this musian on the musicians page. Lower values appear earlier. If octava_musician is
# not set to true, then this should be omitted.
order: 0
```

### Concerts

Concert info pages are in the [_concerts](_concerts/) folder. The markdown content can cotain a short description of the concert or credit a poster artist. Here is an example frontmatter for a concert:

```YAML
# The name for the concert
title: Example Concert

# The YAML formatted date and time of the concert
date: 2000-01-01 19:30

# Setting this to true tells the template to display a poster with the same name as this file, but
# with .jpg as the extension. If no poster is available, simply omit this property.
poster: true

# An object describing the venue of the concert
venue:
  # The name of the concert venue
  name: A Venue

  # The address of the venue
  address: 12345 S 6th St, Example, EX 9876

  # The venue's website (This may be omitted)
  url: http://example.com

  # The phone number of the venue
  phone: (123) 456-7890

# A list of the pieces played at the concert
program:

  # The first entry in the program
  -
    # The title of the piece
    title: Piece No. 1

    # The full name of the composer of the piece. If there's a bio available, it will be linked.
    composer: Full Name

    # A place to indicate the soloist or other details. If none, omit this property.
    details: Solo by Example

    # A list of movements in the piece. If not available, simply omit this property.
    movements:
      - I. Allegro
      - II. Adagio

  # The second entry in the program, with only the minimum information declared.
  -
    title: Piece No. 54
    composer: Example Two

# The list of musicians playing in the concert, grouped by instrument.

roster:

  # A section
  -
    # The name of the section
    section: Violins

    # The list of people that play the instrument
    people:
      -
        # Name of the player
        name: The Concertmaster

        # Indicate special details here, or omit.
        details: Concertmaster
      -
        name: The Second in Command
      -
        name: Second Chair
      -
        name: Yet Another
        details: Principal Second Violin
  -
    section: Oboes
    people:
      -
        name: Single Oboe
        details: Principal
```