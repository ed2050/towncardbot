# towncardbot
Discord bot for Township trading card info

# Help

Read this page for info.  Report problems or errors here: [Towncardbot Discussions](https://github.com/ed2050/towncardbot/discussions)

# Usage
towncardbot supports these commands. In discord chat on our server (MFBiF), type:
- **/whohas cardname** : shows who has extras of a card.  can enter multiple cardnames separated by comma.  with autocomplete

- **/whoneeds cardname** : show who needs a card.  cardname is same as /whohas

- **/trades username** : suggest trades between you and username, based on which cards each of you need / have extra.

- **/whois username** : having trouble finding someone?  know their discord name but not town name, or vice versa?  whois shows all info about a user in the Shark Card Collection spreadsheet.  Town name, town code, discord names, nicknames, coop, etc.

- **/show username** : quick stats on user's card collection.  how many they have, how many golds, and their top (rarest) extras and missing cards.

# Screenshots

/whohas lemonade,berry basket

<img width="712" height="286" alt="Screen Shot 2025-09-12 at 5 54 08 PM" src="https://github.com/user-attachments/assets/36a3cad2-790c-4cd3-b48f-aed58b7e5532" />

/trades azalea

<img width="707" height="300" alt="Screen Shot 2025-09-12 at 6 18 47 PM" src="https://github.com/user-attachments/assets/a0f64914-2bde-4279-ac25-d28b2f2a953a" />

/whois ed

<img width="713" height="136" alt="Screen Shot 2025-09-12 at 6 20 57 PM" src="https://github.com/user-attachments/assets/6799fb01-e7ad-470f-8f6c-ea6f23ed9ae8" />

/show kmimm

<img width="708" height="353" alt="Screen Shot 2025-09-12 at 6 23 56 PM" src="https://github.com/user-attachments/assets/aef92619-d48a-4d1a-b9c2-5ad868dea64c" />

# Notes

Sometimes the bot times out when discord is busy.  Wait a couple minutes and try again.

The card name completion syntax is a bit strange because of discord's UI.  Don't worry about double commas between some items.  Those exist to help keyboard navigation.  You can leave them alone, they won't hurt anything in your command.

Discord autocomplete has quirks.  When an autocomplete option comes up, you can accept it by either clicking with mouse or pressing tab with keyboard.  After accepting, the card name will end with two commas.  If you want to enter another card, PRESS BACKSPACE ONCE to remove the second comma, then start typing the second card name.  Unfortunately those commas and backspace are necessary.  Otherwise discord puts the second cardname in a different location where bot can't see it. Bot can only see card names in one string, separated by commas.  Discord doesn't support normal keyboard input standards, nothing I can do to fix it.
