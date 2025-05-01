
## Method Reference

### Main.java
- `start(Stage primaryStage)` – Initializes UI components and sets event handlers
- `updateNotesList(ListView<String>)` – Updates the note list view with all notes
- `updateNotesList(ListView<String>, List<Note>)` – Updates the note list with filtered notes
- `showAlert(String, String)` – Displays an alert window with a message

### KnowledgeBase.java
- `addNote(String text, List<Tag> tags)` – Adds a new note to the base and saves it in history
- `getNotes()` – Returns the current list of notes
- `deleteNote(int index)` – Deletes a note at the given index and updates the file
- `saveNotesToFile(String fileName)` – Serializes and saves the notes to a file
- `loadNotesFromFile(String fileName)` – Loads notes from a file
- `undo()` – Undoes the last note addition and moves it to redo stack
- `redo()` – Redoes the last undone note
- `searchNotesByTag(Tag tag)` – Filters notes that contain the given tag

### FileManager.java
- `saveNotesToFile(List<Note>, String)` – Writes the list of notes to the specified file using ObjectOutputStream
- `loadNotesFromFile(String)` – Reads and returns a list of notes from a file using ObjectInputStream

### Note.java
- `createNote(String, List<Tag>)` – Factory method to create a Note object
- `getText()` – Returns the text of the note
- `getTags()` – Returns the list of tags
- `deleteNote()` – Clears the text and tags (used before removing a note)

### Tag.java
- `createTag(String)` – Factory method to create a Tag
- `getName()` – Returns the tag name

### History.java
- `saveState(Note)` – Adds a note to the undo stack
- `undo()` – Returns and removes the last note from the undo stack

## How to Run
1. Make sure JavaFX is configured properly.
2. Run `Main.java`.
3. Use the interface to add, search, and manage notes.
