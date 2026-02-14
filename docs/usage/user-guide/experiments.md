---
sidebar_position: 2
title: Experiments
---

# Experiments

## Listing experiments

Experiment entries are the core of the eLabFTW lab notebook. Select "Experiments" from the menu bar at the top of the page to access the Experiments index.

<figure>
  <img src="/img/user-experiments-menu.png" alt="eLabFTW experiments menu" />
  <figcaption>eLabFTW experiments menu.</figcaption>
</figure>

This menu contains several entries for listing Experiments with different Scopes, by Category or accessing Templates, Experiments Categories or Experiments Status.

<figure>
  <img src="/img/user-experiments-menu-opened.png" alt="eLabFTW experiments menu opened" />
  <figcaption>eLabFTW experiments menu opened.</figcaption>
</figure>

<figure>
  <img src="/img/user-show-mode.png" alt="eLabFTW experiments listing" />
  <figcaption>eLabFTW experiments listing.</figcaption>
</figure>

You can change the page layout by clicking the **Layout** button on the top right of the experiments list:

<figure>
  <img src="/img/user-switch-layout.png" alt="switch layout" />
  <figcaption>Change layout button.</figcaption>
</figure>

To make the entries appear like this:

<figure>
  <img src="/img/user-alt-layout.png" alt="switched layout" />
  <figcaption>Alternate layout.</figcaption>
</figure>


## Creating your first experiment

You can create an Experiment by clicking the `Create` button on the top right of the screen:

<figure>
  <img src="/img/user-create-experiment.png" alt="create experiment button" />
  <figcaption>Create an Experiment.</figcaption>
</figure>

A modal window appears, allowing you to enter a title and optionally select an existing Template.

<figure>
  <img src="/img/user-create-modal.webp" alt="create entry modal" />
  <figcaption>Creating an entry.</figcaption>
</figure>

:::note
This modal window will select the type of entry (Experiment/Resource and their Templates) depending on which page it was clicked from. You can still change it manually afterwards.
:::

## Editing your first experiment

You will then be presented with a new Experiment entry. Experiment entries have two different modes: 'edit' and 'view'. By default, when an Experiment is created it will appear in 'edit' mode (you can see 'mode=edit' in the URL).

An Experiment entry can include many different types of information, such as:

* A title
* ID and custom ID numbers
* A Category
* A Status
* Tags
* Permissions
* The main text, which can include images, tables, and links
* Extra fields
* Steps
* Links to other Experiments or Resources
* Attachments (uploaded files)

The only required information is the title.

All fields are automatically saved upon change. Only the main text needs to be manually saved by clicking the Save button below the Main Text editor. An autosave is triggered 7 seconds after you stopped typing.

## Archival

### Archiving an experiment

Experiments can be archived to keep your workspace organized. To archive an experiment, open the entry and click on the "More options" button on the top-right corner of the toolbar and click "Archive":

<figure>
  <img src="/img/experiments-archive.png" alt="experiment archive" />
  <figcaption>Archive an experiment.</figcaption>
</figure>

Once archived, an experiment will no longer appear in the default search results or be included in exported data.

### Viewing Archived Experiments

To display archived experiments:

1. Navigate to the Experiments list.

2. Click on the Show more filters button:

<figure>
  <img src="/img/experiments-show-more-filters.png" alt="experiments show more filters" />
  <figcaption>Show more filters.</figcaption>
</figure>

3. Use the Select state filter and choose Archived.

Archived experiments will now appear in the list, indicated by a small archive icon.

### Working with Archived Experiments

While archived experiments remain viewable, they are read-only. To edit it again, you must first unarchive the experiment.

You can multiselect experiments to unarchive them in bulk:

<figure>
  <img src="/img/archived-experiments-multiselect.png" alt="experiments multiselect" />
  <figcaption>Show multiple experiments to perform bulk actions.</figcaption>
</figure>

Alternatively, you can open an individual archived experiment to review its content. If you decide to restore it, click on the "More options" button located at the top-right corner of the toolbar.

<figure>
  <img src="/img/archived-experiment-more-options.png" alt="experiment more options" />
  <figcaption>More options > unarchive.</figcaption>
</figure>

Once unarchived, the experiment will return to the active list and be fully editable again.

## Deleting an experiment

Experiments can be deleted when they are no longer relevant. Once deleted, an experiment is removed from the active list and placed in the trash. Deleted experiments are not included in searches or exports. The soft-delete mechanism prevents actual removal of data.

## Viewing Deleted Experiments

To list deleted experiments, select Deleted state, similarly to what is described above for Archived entries.

Deleted experiments will now appear in the list, indicated by a trash bin icon.

## Working with Deleted Experiments

Deleted experiments can still be accessed and restored, but they remain read-only until restored.

You can multiselect deleted experiments to restore them in bulk:

<figure>
  <img src="/img/deleted-experiments-multiselect.png" alt="deleted experiments multiselect" />
  <figcaption>Select multiple deleted experiments.</figcaption>
</figure>

Alternatively, open an individual deleted experiment to review its content. To restore it, click on the "Restore entry" button.

<figure>
  <img src="/img/deleted-experiment-restore-entry.png" alt="experiment restore" />
  <figcaption>Restore a deleted experiment.</figcaption>
</figure>

Once restored, the experiment will return to the active list and become editable and exportable again.

## Toolbar

For both Experiment and Resource entries, the top part of the page displays a toolbar with several available actions, as described below.

<figure>
  <img src="/img/user-view-toolbar.png" alt="user toolbar" />
  <figcaption>Main toolbar.</figcaption>
</figure>

1. Go back
^^^^^^^^^^
Go back to the index page.

2. Mode
^^^^^^^
Switch between "edit" mode and "view" mode.

3. Duplicate entry
^^^^^^^^^^^^^^^^^^
Create a new entry with the same Title, Tags, text, and links, but with today's date and the Status set as "Running". A pop-up message will ask if you would like to copy the attached files to the duplicated entry. An «I» character is added to the title to indicate that it is a duplicate.

4. Add signature
^^^^^^^^^^^^^^^^
Add a signature to prove that this entry has been approved by a referenced human. See :ref:`Signatures documentation <signatures>`.

5. Timestamp
^^^^^^^^^^^^
When you click this button, a timestamp archive is created. This is a signed, legally binding snapshot of the entry that is stored alongside the attached files in an immutable archive. Timestamping an entry involves generating a full JSON export of the entry and creating a cryptographic hash of that data. This hash is then sent to a trusted third party: the TimeStamping Authority (TSA).

The TSA acknowledges the existence of the data and sends back a signed token, which serves as proof that the data existed at that specific time. This process follows the :rfc:`3161` standard for Trusted Timestamping.

The timestamped data and corresponding token are then saved in the "Attached Files" section of the entry as a zip file. This file is initially in an "Archived" state, meaning it is hidden from view by default. To view archived files, click the "Show Archived" button on the right side of the "Uploaded Files" section in edit mode:

<figure>
  <img src="/img/show-archived-uploads.png" alt="show archived uploads" />
  <figcaption>Show archived attachments.</figcaption>
</figure>

This timestamp archive is immutable and cannot be modified or deleted.

<figure>
  <img src="/img/timestamp-archive.png" alt="timestamp archive" />
  <figcaption>The archived ZIP file.</figcaption>
</figure>

## Verifying the timestamp

To verify locally the validity of the timestamp, you can use `openssl` with a command similar to:

~~~bash
openssl ts -verify -CAfile /etc/ssl/cert.pem -data /path/to/X-timestamped.json -in /path/to/X-timestamped.asn1 -text
~~~

If it was signed with a certificate trusted on your system, it should output "Verification: OK". You can also check the token content directly with:

~~~bash
openssl ts -reply -in /path/to/X-timestamped.asn1 -text
~~~

The output should look like:

~~~console
Using configuration from /etc/ssl/openssl.cnf
Status info:
Status: Granted.
Status description: Operation Okay
Failure info: unspecified

TST info:
Version: 1
Policy OID: 1.3.6.1.4.1.22177.300.22.1
Hash Algorithm: sha256
Message data:
    0000 - 5a 58 7b 86 c3 a6 79 27-35 b8 4d 57 bc 5a 7e 80   ZX{...y'5.MW.Z~.
    0010 - 52 89 92 60 0b 8d 03 d4-f2 9e 4a 4c 6d ec 91 a4   R..`......JLm...
Serial number: 0xCDAB07382DF7B1BBE0CC970E93A7625B63F4DB7A
Time stamp: Jul 16 23:07:34 2025 GMT
Accuracy: unspecified
Ordering: no
Nonce: unspecified
TSA: unspecified
Extensions:
~~~

The "Time stamp" line gives you the timestamp time. The "Hash Algorithm" and "Message data" should correspond to the digest of the data file (the .json). Compare it with: `openssl dgst -sha256 /path/to/X-timestamped.json`



6. Blockchain timestamp
^^^^^^^^^^^^^^^^^^^^^^^
This button will perform the same action as a timestamp, except it will use blockchain technology and the service provided by the Bloxberg consortium. You can learn more about it here: [Bloxberg website](https://bloxberg.org/discover/mission/).

7. Export button
^^^^^^^^^^^^^^^^

<figure>
  <img src="/img/export-options.png" alt="export options" />
  <figcaption>List of available exports.</figcaption>
</figure>

The Export menu allows you to save the entry in different file formats.

The ELN format is a new file format based on RO-Crate specification. It contains a special file (in JSON-LD) describing the contents of the dataset (one or several Experiments). It is designed and promoted by The ELN Consortium, an association of several ELN vendors that agreed on an interchange format for export/import of datasets. Learn more about it here: [TheELNConsortium on GitHub](https://github.com/TheELNConsortium/).


8. Pin entry
^^^^^^^^^^^^
Clicking this icon will make this entry appear on top of the list on the main page (pin entry). Use this to easily access frequently used entries.

9. Lock/unlock entry
^^^^^^^^^^^^^^^^^^^^
Use this to lock the entry and prevent further editing. Only an Admin or the user who locked an experiment can unlock it.

10. Request action
^^^^^^^^^^^^^^^^^^
Request another user to perform an action on a given entry.

   - Archive
   - Lock
   - Review
   - Sign
   - Timestamp
   - Unarchive

11. Ellipsis menu
^^^^^^^^^^^^^^^^^

   - Transfer ownership: For entries you created, you can transfer ownership to a different user
   - See revisions: View revisions to the main text of the entry
   - See changelog: View the changelog for the entry
   - Archive/Unarchive: Archiving removes the entry from the default list and adds it to the list of archived entries
   - Delete entry: Perform a :ref:`soft-delete <soft-delete>` of the entry


### Date (started on)
The date is set to today's date by default. You can edit it as you wish. The effective creation timestamp is stored in the backend database in another (read-only) attribute.


### ID
This attribute is not editable and corresponds to the unique (to that instance) immutable ID of the entry.

### Custom ID
This attribute (`null` by default) can be set as a number after a Category is selected. Custom ID numbers will then be automatically assigned in an incremental fashion when new Experiments with that Category are created. One can also click the "Get next" button to fetch the next available Custom ID for entries of that Category. The Custom ID is displayed before the title.

### Title
This is the title of the Experiment. A duplicated Experiment will have a «I» character appended to the title upon creation.

### Category
You can assign a "Category" to each Experiment. Only an Admin can define the categories that are available for your team to use. Categories can correspond to projects, types of Experiments, and other strategies for grouping Experiment entries. You can easily browse groups of Experiments by Category from the main Experiment page.

### Status
This feature lets you set the 'Status' of an Experiment. The default status options are:

- Running
- Needs to be redone
- Success
- Fail

These Status options can be modified by an admin via the admin panel.

### Tags
Tags allow users to easily group and sort Experiment entries. You can think of them as folders, but they are more powerful because each Experiment can have many different Tags. The Tag system thus enables efficient cross-searching.
You can list all Experiments with a given Tag by clicking on the Tag or searching for it in the Tag search bar. To add a Tag to an Experiment entry, type the name of the tag in the Tag input field and press Enter or click anywhere outside the input field. You can add an unlimited number of Tags. Click on an existing Tag to launch a prompt that will allow you to remove it (in edit mode). Tags are common to each team. Autocompletion favors the reuse of existing Tags.


## Permissions
The "Visibility" and "Can write" menus allow you to control who can access and change a given entry. Click the `Edit` button to view, add, or remove permissions.

## Main text
This is the space to freely describe your experimental setting, procedure, results, and any other information you wish to include about your research. In this rich text editor, you can add text with various formatting options, create tables, and add images, links, etc…

   .. figure:: img/tinymce-editor.png
      :align: center
      :alt: Tinymce editor

      Tinymce editor

### Inserting an image

To insert an image into the main text, simply drag and drop it into the text editor. You can also insert an uploaded image by clicking on the ellipsis menu on the file icon in the "Attached Files" section (three vertical dots on top right) and selecting "Insert in the text at cursor position".

### Inserting templates

From the Insert menu in the text editor, you can select "Insert template" to import the contents of the text editor from an existing Experiment template. This allows you to combine content from multiple templates.

### Using Markdown

<figure>
  <img src="/img/markdown-editor.png" alt="markdown editor" />
  <figcaption>Markdown editor.</figcaption>
</figure>

You can also use Markdown to create the main text. You can switch to Markdown by clicking the "Switch editor" button at the bottom right of the main text box. If you'd like Markdown to be the default option, go to Settings and select "Disable the rich text editor and write Markdown directly".

### Tables
If you add tables to the text editor you might want to dynamically sort the contained data. Don't worry, eLabFTW has you covered. Sort icons are displayed in "view" mode when "header cells" (`<th>`) are defined and a table is set as sortable. The table should have column names in the top row. You can select the top row by clicking the left mouse button with the cursor over the leftmost cell, and while keeping the mouse button pressed, move the cursor to the rightmost cell. Release the mouse button. The top row should be highlighted now. Next, from the text editor menu select «Table» → «Cell» → «Cell properties». In the dialog change the «Cell type» from «Cell» (`<td>`) to «Header cell» (`<th>`). Finally, you can activate sorting by clicking the «sortable table» icon (|sortable-table-icon|) in the tool bar. The icon will also indicate whether a selected table is sortable. After you have saved the changes (see "Saving your changes), you can go to "view" mode and dynamically sort the table. The changed order is not stored in eLabFTW. Merged cells in the top/header row (colspan) and in columns (rowspan) are not supported.

<figure>
  <img src="/img/sortable-table-icon.png" alt="sortable table icon" />
  <figcaption>Icon to sort tables.</figcaption>
</figure>

### Using LaTeX

It is possible to express mathematical/chemical notation in eLabFTW, and formulas are rendered in both "view" mode and pdf exports.

To do this, eLabFTW uses Mathjax with the ams extension.

Try the Mathjax expression below (make sure it is not pasted between `<pre>` Tags!):

~~~latex
$$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$$
~~~

<figure>
  <img src="/img/tinymce-editor-paragraph.png" alt="tinymce paragraph" />
  <figcaption>Change `<pre>` tag into a paragraph.</figcaption>
</figure>

Use one `$` for inline mode and `$$` for block mode.

### Miscellaneous

You can use basic text editor shortcuts and code snippets in the text editor to add highlighting, special characters, horizontal lines, etc...

For a list of text shortcuts see this link: https://www.tiny.cloud/docs/tinymce/latest/keyboard-shortcuts/

Examples:

- ctrl+shift+d : add date/time at cursor
- ctrl+= : subscript
- ctrl+shift+= : superscript

### Steps

You can use steps to list actions that need to be taken in connection with a given Experiment or Resource. When a task has been completed, you can click on the corresponding checkbox to indicate that that step is done. The "Next step" for each Experiment or Resource will be shown on the main Experiments or Resources page (index list) under the title for that entry. This lets you easily view the next step for each entry. You can also view the next steps for your Experiments and Resources by clicking on the "To-Do List" icon at the top left side of the main page.

<figure>
  <img src="/img/steps-on-experiment.webp" alt="steps on experiment" />
  <figcaption>Steps on an experiment.</figcaption>
</figure>

You can also add steps when creating a template, and choose to lock them. When a new Experiment or Resource is created from that template, the locked steps will appear as read-only and cannot be modified or deleted.

<figure>
  <img src="/img/steps-on-template.webp" alt="steps on template" />
  <figcaption>Steps on a template with lock toggle.</figcaption>
</figure>

## Spreadsheet Editor

With version 5.3 comes a new spreadsheet editor, present in the edit page of an entry. It lets users display and manipulate tabular data directly inside eLabFTW, with support for common spreadsheet operations and formula calculations (e.g. CSV / XLSX import-export, cell arithmetic, SUM, ROW, etc.).

<figure>
  <img src="/img/spreadsheet-editor.png" alt="spreadsheet editor" />
  <figcaption>Editing tabular data within eLabFTW.</figcaption>
</figure>

### General formula support

The spreadsheet editor supports common spreadsheet formulas and operators, allowing users to perform calculations directly in cells. Formulas are parsed when expressions start with the `=` character.

When cells referenced by a formula change, all dependent formulas are recalculated automatically (reactive updates). Copy, paste, and drag-fill behavior also adjusts formula references appropriately (relative vs. absolute).

#### Arithmetic operations

You can use the `SUM` function for addition, and simple inline operators for subtraction, multiplication, and division directly in cells.

For example::

~~~
    =SUM(A1:A5)
    =D1 - D2
    =A5 * E7
    =SUM(B1, C1 * D1)
~~~

These formulas follow standard spreadsheet behavior, supporting mixed operations and cell references.

##### Special / built-in helper functions

In addition to standard functions such as `SUM` or `AVERAGE`, several helper formulas are available::

~~~
    =CELL()         Returns the cell reference (for example `A1`).
    =COLUMN()       Returns the current column number.
    =ROW()          Returns the current row number.
    =VALUE(c, r)    Returns the value of the cell at the given column and row.
    col: Number, row: Number, processedValue: Boolean.
~~~

This feature is currently in **BETA** and should be used with caution, when manipulating important data.

See more from the [jspreadsheet-ce documentation](https://jspreadsheet.com/docs/v8/formulas).

## Linked Resources/Experiments
You can link a Resource or Experiment entry to another Experiment or Resource entry. Just begin to type the name of the entry you want to link in the text editor, Linked Resources field, or Linked Experiments field, and an autocompletion list will appear. Select the entry you want to link and press enter. If you link an entry from the text editor, it will automatically be added to the Linked Experiments/Resources section. The number of links is unlimited.

This feature can be used to view the Resources or Experiments that are linked to a given entry. For example, you can view all the Experiments that use a particular Resource by looking at the Linked Experiments section in the entry for that Resource.

You can also use this feature to organize entries by project, sort of like a folder. For example, you can create a Resource entry for a given project and link all the Experiments and Resources that are associated with that project.

Next to the possibility to preview the content of a linked entry (1) and to delete a link (4), in edit mode, there are two actions to import content from a linked entry:

<figure>
  <img src="/img/user-linked-entries-tools.png" alt="link actions" />
  <figcaption>Import links.</figcaption>
</figure>

Import Links (2)
    Links to entries that are present inside a linked entry are copied into the current entry.
    For example, let's say there is an experiment (Time travel) that requires certain reagents (banana peel and beer) and devices (flux capacitor and Mr. Fusion) which are explained in more detail in the corresponding resource entries. The resources are linked to the experiment. Unfortunately, the experiment does not work the first time, so there is need for a second iteration (Time travel II). Time travel II gets a link to Time travel and now all the required reagents and devices can be imported easily by clicking the "Import Links" button.

Import Body (3)
    The text body of a linked entry is copied into the current entry at the cursor position.

## Attach a file

<figure>
  <img src="/img/user-file-uploader.png" alt="user file uploader" />
  <figcaption>File uploader.</figcaption>
</figure>

Click this region to open the file browser, or drag and drop a file to this region to add it to the entry. The file size limit depends on the server configuration, but there is no limit on file type. If you upload an image, a thumbnail will be created. There is no limit on the number of files you can attach to an Experiment.

Various file types are recognized by eLabFTW:

* molecule files such as cif, pdb, sdf, and mol files: The resulting icon will display the molecule in 2D or 3D
* DNA files such as FASTA, gb, ape, dna, and gff: These will be displayed via a fully featured viewer
* image files such as png, jpg, gif, and tiff: These will show as a thumbnail icon
* pdf files: These are shown as thumbnail icons and can optionally be included in pdf exports


## Saving your changes

To save changes made to the text editor, click the floppy disk icon on the top left of the editor, or the Save button below it. Changes in the text editor are saved automatically 7 seconds after the user stopped typing.

Changes made to any other field are saved automatically, or saved when you click outside of the field. A successful save action is indicated by the "Saved" banner that will show at the top left of the screen.

## elabid
In the bottom right part of the Experiment, you can see something like: «Unique elabid: 20150526-e72646c3ecf59b4f72147a52707629150bca0f91». This number is unique to each Experiment, and immutable (won't ever change). You can use it to reference an Experiment with an external database.

## Comments
People can leave comments on Experiments. Not everyone can edit your Experiment, but they can leave a comment. The owner of the Experiment will receive an email if someone comment their Experiment.

