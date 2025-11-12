# Instructions for Card Trading spreadsheet (Admins only)

<img src="https://cdn.mos.cms.futurecdn.net/A3QcCbtCNT2ihjozVDQDfe.jpg" height="200px" />

## Adding users

First you need permissions on the spreadsheet.  Contact Ed/Globex.

Then add users like this:

1. Add new user info to Town Info sheet after existing users.
2. Go to menu Task Automator -> Update users.  This copies new users to all card data sheets.
3. Wait while update runs.  A small box in top middle says it's running.
4. Now click Task Automator -> Sort data by name.  This sorts data sheets in alphabetical order.  Can take 2 mins - just wait.
Sheets are locked during this process.

That's it.  Add any number of users at a time to Town Info and then run Task Automator commands.  Just don't sort by hand.

<img src="https://static0.colliderimages.com/wordpress/wp-content/uploads/2023/06/homer-simpson-from-the-simpsons.jpg" height="200px" />

The first time you use Task Automator, it will ask for approval.  Follow the steps below. 


## Authorize app (first time only)

The first time you use the Task Automator menu, you'll get a confirmation page similar to this:
<img src="https://developers.google.com/static/apps-script/images/unverified-app-ui.gif" style="max-height: 90vh;" />

- First choose which google account to use.  Pick the one that was given Editor access to the spreadsheet.
- Then it will say "This app isn't verified".  In bottom left, click Advanced.
- Click in bottom left where it says something like "go to blah blah (unsafe)" or "run so-and-so (unsafe)"
- Type or click continue / accept on following screens.  You may have to scroll to bottom of page.

What it means: "unverified" means that the script wasn't reviewed by Google.
The script for menu functions doesn't run on your machine, it runs on Google servers.
And it can't access your Google account data, only the Shark Swap spreadsheet.

## Removing Users

<img src="https://puzzledpagan.com/wp-content/uploads/2016/06/093.jpg?w=573&h=323" height="200px" />

To remove a single user:
- Go to Town Info tab
- Cut and paste their town name, town code, etc (cols A-D) from active users to Not Participating (col J).
- select the cell in col J with the name of user you are removing.
- Run the menu option "Task Automator -> Remove user"

That's it.  Script will run and do the following:
- copy user's row in Cumulative to sheet Removed (just to backup their data in case of mistakes)
- delete user's row in Cumulative
- delete user's row in all 15 card group sheets
- resort Town Info sheet active users (cols A-H) to move empty rows to the bottom

Script has several safeguards built in:
- it will only delete name in active cell
- it will not run if active cell is not in column Not Participating
- it will not run if username still appears in Town Info active users (col A)

## Troubleshooting

<img src="https://static0.srcdn.com/wordpress/wp-content/uploads/2018/09/Homer-Simpson-in-The-Simpsons.jpg?w=1200&h=628&fit=crop" height="200px" /> 

If anything goes wrong, **don't edit spreadsheet by hand**.  This is likely to corrupt data.
Contact Ed/Globex to sort it out.
