---
# The name for the concert
title: Example Concert

# The YAML formatted date and time of the concert
date: 2020-01-01 19:30

# Setting this to true tells the template to display a poster with the same name as this file, but
# with .jpg as the extension. If no poster is available, simply omit this property.
poster: true

# Set this to give credit to people that worked on the poster.
poster_credit: Poster art by <a href="https://example.com">Artist</a>.

# A description of ticket pricing at the door.
tickets_description: Tickets at the door are $20 for adults, $15 for students/seniors (65 and over); children accompanied by an adult are free!

# A list of tickets available online. Omit this to disable online ticketing.
# This is not displayed on past concerts, so no need to remove this when a concert has passed.
tickets:
  -
    # The name of the ticket.
    type: Adult

    # The online price of the ticket.
    # Be sure to wrap in quotes to ensure it is interpreted as a string.
    price: "18.00"
  -
    type: Student/Senior (65+)
    price: "13.00"

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

    # The composer of the piece. If they exist in the musicians collection, their bio will be linked
    # Thus, to link a bio, you need to use the composer's full name.
    composer: Example Composer

    # A place to indicate the soloist or other details. If none, omit this property.
    details: with soloist Example

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
        name: A Violinist
      -
        name: Another Violinist
      -
        name: Yet Another
        details: Principal Second Violin
  -
    section: Oboes
    people:
      -
        name: Single Oboe
        details: Principal
  -
    # Consider adding a solists section so that links to bios can be generated for the soloists.
    section: Soloists
    people:
      -
        name: A Soloist
        details: Instrument
  -
    # Generate links to conductors too.
    section: Conductors
    people:
      -
        name: A Conductor
        details: A Piece
---