# Editing card collection data

1) Go to:
https://towncards.my.to/e/cardset

Anyone can view the page and download json file.
Only admins can upload.

1) Download the json file.

1) Edit the json file and plug in the set names and corresponding card names where it says "set x" and "card x".  Sets and cards should be in same order as actual game.

1) Upload the edited file with complete card collection data.

## Things to keep in mind

- if you find a typo, fix the file and re-upload.
- always upload entire collection data.  no partial uploads.
- order matters.  Set 1 (in game) should be first set, #2 should be second, etc.  don't reorder.

- don't touch aliases field.  server builds them on upload.  it will ignore anything you put there and make its own.  so if you change Cookout - Call to Cookout - Coal, server will detect and add alias for old mistaken name.

when it hits 10am UTC on July 10, server should automatically start using the new card data.  it reads the json file already, but ignores it since date is in the future.  on july 10 it will start showing the temp card names on player pages until you upload the real names.

upload tool is restricted to just you.  others can download, so if you want Han or someone to dl the file and fill in the names, they can help.  but only your account can upload.

it's rough, not polished like my other pages.  cause this is a one-time thing for admins, not users.
