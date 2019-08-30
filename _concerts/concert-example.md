---
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
---

Add a short description or credit the poster artist here.