---
sidebar_position: 3
title: Resources
---

# Resources

Resources are similar to Experiments, but serve a different purpose: listing and organizing *things* that are used in Experiments.

Many of the options on the Resource entry are the same as those for an Experiment entry.

Resources Categories can be defined at the team level from the "Resources Categories" page available in the Resources dropdown menu. You can for example have such categories:

* Antibodies
* Microscopes
* Plasmids
* Drugs
* Chemicals
* Equipment
* Projects

Once you have Resources Categories (which are simply composed of the name and a color), you can create a Resource Template with that category assigned. This allows you to have several Resources Templates for a given Category.

For instance, in the Resource Category "Antibodies", you might want to have a Resource Template for "Primary Antibody" and one for "Secondary Antibody". It's also fine to keep a one-to-one relationship between Resources Templates and Resources Categories.

Resources' default permissions allow anyone from the Team to edit them, but you are free to configure them differently from their Template.

Look at the :ref:`importing-data` section to learn how to import your Resources from a spreadsheet file or through the API.

Once you have your Resources present, you can mention them in your Experiments by typing `#` and their title, and selecting the proposed autocompletion, or use directly the Link system to link them to an Experiment.

Furthermore, Resources can be made bookable, see section below.

## Booking Resources

It is possible to use the scheduler (calendar) present on the Scheduler page to book Resources.

## Making a Resource bookable

In order to book a Resource, it needs to be bookable (they are not by default). To do that, go to the Resource, and click "Modify booking parameters" from the top right menu with three vertical dots:

<figure>
  <img src="/img/modify-booking-menu.png" alt="modify booking menu" />
  <figcaption>Modify booking menu.</figcaption>
</figure>

This will show a modal window with various settings:

<figure>
  <img src="/img/modify-booking-modal.png" alt="modify-booking-modal" />
  <figcaption>Modify booking modal.</figcaption>
</figure>

### Settings description

| Setting                                             | Description |
|----------------------------------------------------|------------|
| Allow booking this Resource                        | This is a general toggle to allow booking of the Resource |
| Allow overlapping slots                            | Control whether it is allowed to have more than one booking slot at the same time |
| Maximum slot time (in minutes)                     | Maximum number of minutes allowed for a single booking slot |
| Maximum per-User future slot allowed               | Number of future slots allowed for a particular User/Resource couple |
| Allow cancelling a booking slot                    | Control whether Users are allowed to cancel a booking |
| Minimum time before a slot can be cancelled (in minutes) | If "now" is closer than this number of minutes to the start of the event, it will not be possible to cancel it |


## Adjusting permissions

When a Resource is bookable, a new permission appears: "Can book":

<figure>
  <img src="/img/can-book-setting.png" alt="can book settings" />
  <figcaption>Modify booking permissions.</figcaption>
</figure>

By default, it will match who can read the entry, but it can be adjusted to fine tune who exactly has access to this Resource for booking it.

## Archiving and deleting resources

Resources can be archived or deleted just like experiments. The behavior is exactly the same.

## Using the scheduler

Once all is set, Users can click the "Book item" button in the toolbar, or select it from the Scheduler page, and click the calendar to drag a booking slot.

<figure>
  <img src="/img/book-item-button.png" alt="book-item-button" />
  <figcaption>Booking in item button.</figcaption>
</figure>

Clicking an existing slot will display a modal window allowing several options such as binding the slot to an Experiment or another Resource, or cancel booking, with or without sending a notification to Users.

<figure>
  <img src="/img/book-edit-modal.png" alt="book-edit-modal" />
  <figcaption>Booking a resource modal window.</figcaption>
</figure>

Note: "Past and future Users who booked this Resource" means all Users who booked the Resource in the past two months and the ones who booked it in the upcoming month.
