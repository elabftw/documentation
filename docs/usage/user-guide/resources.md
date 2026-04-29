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

Once this parameter has been activated, clicking this same button will redirect you to the scheduler with the resource selected.
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
  <img src="/img/can-book-setting.webp" width='400' alt="can book settings" />
  <figcaption>Modify booking permissions.</figcaption>
</figure>

By default, it will match the `Visibility` permission of the entry, but it can be adjusted to fine-tune who exactly has access to this Resource for booking it.

## Archiving and deleting resources

Resources can be archived or deleted just like experiments. The behavior is the exact same. See [Archival](./experiments#archival) section.

## Scheduler

Once all is set, Users can click the `Book item` button in the toolbar, or select it from the Scheduler page, and click the calendar to drag a booking slot.
<figure>
  <img src="/img/book-item-button.webp" width='300' alt="book-item-button" />
  <figcaption>Booking in item button.</figcaption>
</figure>

The scheduler page loads with the selected item:
<figure>
  <img src="/img/scheduler-selected-item.webp" width='300' alt="scheduler selected item" />
  <figcaption>Selected item in the scheduler page.</figcaption>
</figure>

You can now drag-and-drop a slot, confirm the "Title" of the event and click the `Create event(s)` button. You can select multiple resources to create many events at the same time.
<figure>
  <img src="/img/scheduler-create-events.webp" width='500' alt="scheduler create events modal" />
  <figcaption>Modal to confirm creation of events.</figcaption>
</figure>

Once created, you will be able to see a list of your scheduled bookings in the main page (dashboard).
<figure>
  <img src="/img/scheduled-bookings.webp" width='500' alt="scheduled bookings in dashboard" />
  <figcaption>Scheduled bookings in the dashboard.</figcaption>
</figure>

## Events

On the scheduler page, the items listed are called Events. Clicking an existing slot displays a modal window with different information:
<figure>
  <img src="/img/scheduler-event.webp" width="300" alt="scheduler events" />
  <figcaption>Events in the scheduler.</figcaption>
</figure>

<figure>
  <img src="/img/scheduler-event-view.webp" width="700" alt="modal view of an event" />
  <figcaption>Viewing an event.</figcaption>
</figure>

The first line indicates the Title (or Comment) of the event. It is defined by the user when creating or editing the event.

Below, the date of the event, the time-slot and duration in minutes.

### Bindings

You can bind the slot to an experiment or a resource. Start typing on the "Search" textbox and select the entry you wish to relate to this event.
<figure>
  <img src="/img/scheduler-bind-experiment.webp" width="700" alt="Bind an experiment to an event." />
  <figcaption>Binding an experiment to the event.</figcaption>
</figure>

You can then view or unbind the entry.
<figure>
  <img src="/img/scheduler-binded.webp" width="700" alt="View or unbind" />
  <figcaption>View or unbind an experiment.</figcaption>
</figure>

### Edit an event

Click the `Edit` button to edit an event. You can modify its title and starting/ending hours.

<figure>
  <img src="/img/scheduler-edit-event.webp" width="700" alt="Edit an event" />
  <figcaption>Edit an event.</figcaption>
</figure>

In the scheduler page, you can update an event with the following actions:

- Drag-and-drop: Move the event to the desired start time.
- Drag (by the end): Move only the ending hour of the event.

<figure>
  <img src="/img/scheduler-event-actions.gif" alt="Edit an event" />
  <figcaption>Different actions on an event.</figcaption>
</figure>

### Cancel an event

Click the `Cancel` button to cancel an event.

<figure>
  <img src="/img/scheduler-delete-event.webp" width="700" alt="Delete an event" />
  <figcaption>Delete an event.</figcaption>
</figure>

You can add a custom message to inform the team members who are connected to this event. You can either send to **Members of the team** or to a list of users who booked this resource in a specific time range.

### Browse events

You can use the filters to reduce clutter on the scheduler view and look for specific events.

<figure>
  <img src="/img/scheduler-filters-category.webp" alt="filtering by category" />
  <figcaption>Filtering by category.</figcaption>
</figure>

<figure>
  <img src="/img/scheduler-filters-owner.webp" alt="filtering by owner" />
  <figcaption>Filtering by owner.</figcaption>
</figure>
