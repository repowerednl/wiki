# Wiki

This repository is the source for documentation shown in tooltips on some
Repowered web applications.

### Contributing

To contribute, you will need write access to this repository. Contact someone
from the Data team to help out.

1. Locate the file you want to edit or add in the [root](/) or [nl](/nl) folder
   for English and Dutch respectively.
    - Files are organized by application and then by topic.
    - Use 'Add file' button at the top right in a folder to create a new file
    with the `*.md` extension.
    - Use the pencil icon at the top right of a file to edit the file.
1. Update or add the necessary metadata at the top of the file.
    - Metadata is formatted as follows:
        ```yaml
        ---
        title: <title>
        description: <description>
        ---
        ```
    - The `title` is the title shown at the top of the opened tooltip drawer.
    - The `description` is the text shown when hovering over the tooltip icon.
    This should not be more than a few words.
1. If you are updating release notes instead of a tooltip, update the `date`
   field to the current date and time. This ensures users are notified.
1. Update or add the content which will be shown in the tooltip drawer.
    - A limited set of markdown formatting is currently supported:
        - primary (`#`), secondary (`##`) and tertiary (`###`) headings
        - ordered (`1.`) and unordered (`-`) lists
        - images (`![alt text](image.jpg)`, external only)
        - URLs (`[text](url)`)
    - Use clear language understandable by a non-technical audience.
1. Preview the changes by clicking the 'Preview' button at the top left of the
   editor.
1. Save your changes by clicking the 'Commit changes...' button at the top right
   of the editor.
1. Verify what's shown in the pop-up:
    - The commit message ("Update \<file\>") and description (empty) can be left
    unaltered.
    - 'Commit directly to the `main` branch' is checked.
1. Click 'Commit changes'.
1. Verify that the changes are shown in the targeted web application after
   refreshing the page.
