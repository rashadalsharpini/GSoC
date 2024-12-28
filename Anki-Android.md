### [Development Guide](https://github.com/ankidroid/Anki-Android/wiki/Development-Guide#getting-started)
## Note Editor: Note Type Preview (175 hours)
### Problem

AnkiDroid is a flashcard app with a complex HTML/field-based templating engine. We currently have difficulties explaining a number of concepts to new users, both while onboarding, and for intermediate users:![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeTCTie94V5RFMuz8rwWozOSO3k0w1-0MUE3THMoyl-ubvbdMDlRW9JJUf9J81SGbCgyCFRX-HdKw5gGU9LJZme42vkzfOucsG9cW1Rj1yEXhGT5Nf_RqL1hQxMMb9HuhuiZPmW30d9P1ON5tj3-8086xs?key=MMP2W95DdARl_LNLmuznQg)

- The unexpected fact that the user adds ‘notes’ to the app, not ‘cards’
- One note can generate multiple cards
- Various ‘Note Types’ have unique properties
- A user can create or download additional note types
Currently, the user is provided with a text-based selection screen:
### Expected Outcomes
In order to resolve the above issues, we want to modify this screen to provide a preview of each note type available in the system, showing
- The number of cards which will be produced when the note type is used
- A visual preview of how each of the cards will look
- Each card has a separate HTML template, so the designs may vary
- Taking into account some special features: 
- A note type may request that the user types in the answer
- Cloze deletions: 1 input produces 1…n cards
- Image occlusion: 1 input
- The ability to open our Card Template Editor
The screen should allow a user to open up our Note Type Management screen and our manual. We should aim for the screen to prefer graphical elements over text
### Language:
EITHER:
- Kotlin & XML
- If the screen is Android-specific
- Svelte (Typescript + HTML)
- If the screen is to be integrated into all Anki clients
### Difficulty: Medium
### Mentor(s):
- David Allison

## Note Editor: Instant Add Note Editor (175 hours)
### Problem
We want to make it as painless as possible to add new notes to AnkiDroid.
It currently takes 4 or 5 taps from Chrome to add a note with a cloze deletion
By producing an ‘Instant Add’ editor, we can allow a user to create a cloze deletion with a tap, compared to a long press, followed by a tap. This is a significant time-saver when a user has many notes to add, making the app more pleasant to use
### Expected Outcomes
A user is able to select text in Android applications and select “Anki Card”. This will open an ‘instant add’ editor which allows the user to tap words or phrases in the text and turn them into cloze deletions.
This will be similar to the ‘share to’ dialog which Google Keep provides:
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXciZuW5wGMvlvmzbAJz0m0R_clcaW3oc1ZoBbffm-aQcTMrHjfCWvEToIoeJefCeWPOKeyOkFiCqO6AWSXYkZn_Gvr3V9g3x6AwSJpY-Efafk7rVqU_EpA95oqPVHh38jOwLPrQO2GAsPyd309S5kaHmdI?key=MMP2W95DdARl_LNLmuznQg)

Google Keep’s “Share to” Dialog
This dialog should load quickly, and be minimal in design
The dialog should allow loading of AnkiDroid’s heavyweight ‘add note’ screen
### Language: Kotlin, XML
### Difficulty: Medium 
### Mentor(s):
- David Allison