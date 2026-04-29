---
sidebar_position: 3
title: Resources
---

# Resources

Resources are similar to Experiments, but serve a different purpose: listing and organizing *things* that are used in Experiments.

Many of the options on the Resource entry are the same as those for an Experiment entry.
<figure>
  <img src="/img/resources-menu.webp" width="550" alt="Resources menu" />
  <figcaption>Resources dropdown menu.</figcaption>
</figure>

## Resource Categories

Resource Categories can be defined at the team level from the "Resource Categories" page available in the Resources dropdown menu. You can, for example, define categories such as:

* Antibodies
* Microscopes
* Plasmids
* Drugs
* Chemicals
* Equipment
* Projects

Once you have Resources Categories (which are simply composed of the name and a color), you can create a Resource Template with that category assigned. This allows you to have several Resource Templates for a given Category.

For instance, in the Resource Category "Antibodies", you might want to have a Resource Template for "Primary Antibody" and one for "Secondary Antibody". It's also fine to keep a one-to-one relationship between Resources Templates and Resources Categories.

Resources default permissions allow anyone from the Team to edit them, but you are free to configure them differently from their Template.

## Imports

Look at the [Importing data](../import-export#importing-data) section to learn how to import your Resources from a spreadsheet file or through the API.

## Links
Once you have your Resources present, you can mention them in your Experiments by typing `#` and their title, and selecting the proposed autocompletion, or use directly the Link system to link them to an Experiment.
See [Links](./experiments#linked-resourcesexperiments) section.

Furthermore, Resources can be made bookable, see section below.

## Booking Resources

It is possible to use the scheduler (calendar) present on the Scheduler page to book Resources.
<figure>
  <img src="/img/scheduler.webp" width="550" alt="Scheduler page" />
  <figcaption>Scheduler page.</figcaption>
</figure>

## Making a Resource bookable

In order to book a Resource, it needs to be bookable. They are not by default.

To make a resource bookable, open its page and click the `Modify booking parameters` button from the toolbar.

<figure>
  <img src="/img/resource-activate-booking.webp" width="500" alt="activate booking parameters" />
  <figcaption>Toolbar: Modify booking parameters.</figcaption>
</figure>

Once this parameter has been activated, clicking this button same will redirect you to the scheduler with the resource selected.
If you wish to edit parameters later on, click on the top right menu with three vertical dots:

<figure>
  <img src="/img/modify-booking-menu.webp" width="300" alt="modify booking menu" />
  <figcaption>Modify booking menu.</figcaption>
</figure>

A modal with various settings opens:

<figure>
  <img src="/img/modify-booking-modal.webp" alt="modify-booking-modal" />
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
