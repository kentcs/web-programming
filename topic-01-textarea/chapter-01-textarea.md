# Chapter 1: Working with Textareas and Local Storage

Welcome to Topic 01! In this chapter, you'll learn how to use the `<textarea>` element for multi-line text input, handle events, and store/retrieve data using localStorage. You'll build a simple notes app and gain hands-on experience with interactive web features.

---

## Outline
1. Introduction to Textareas
2. Event Handling with Textareas
3. Adding and Showing Text
4. Saving Data with localStorage
5. Loading Data from localStorage
6. Final Challenge
7. Instructor Tips

---

## 1. Introduction to Textareas
The `<textarea>` element lets users enter multi-line text. You can set its size with `rows` and `cols` attributes.

**Example:**
```html
<textarea id="myTextArea" rows="4" cols="40"></textarea>
```

**Try it:**
Add a textarea to your page. Change the number of rows and columns to see how it affects the size.

---

## 2. Event Handling with Textareas
You can use JavaScript to respond to user actions, such as button clicks. Use `addEventListener` to attach event handlers.

**Example:**
```html
addTextButton = document.getElementById("addTextButton");
addTextButton.addEventListener("click", function() {
    textarea.value += "...some more text..."
});
```

**Try it:**
Add a button that appends text to the textarea when clicked.

---

## 3. Adding and Showing Text
You can read and update the value of a textarea using JavaScript. Use `console.log()` to display the current text in the browser console.

**Example:**
```html
showTextButton = document.getElementById("showTextButton");
showTextButton.addEventListener("click", function() {
    console.log(textarea.value);
});
```

**Try it:**
Add a button that logs the textarea content to the console.

---

## 4. Saving Data with localStorage
localStorage lets you save data in the browser so it persists after a page reload. Use `localStorage.setItem(key, value)` to store data.

**Example:**
```html
saveNotesButton = document.getElementById("saveNotesButton");
saveNotesButton.addEventListener("click", function() {
    notes = textarea.value;
    localStorage.setItem("notes", notes);
    alert("Your notes have been stored.");
});
```

**Try it:**
Add a button that saves the textarea content to localStorage and shows an alert.

---

## 5. Loading Data from localStorage
You can retrieve saved data with `localStorage.getItem(key)`. Load notes when the page loads and display them in the textarea.

**Example:**
```html
window.addEventListener("load", function() {
    storedNotes = localStorage.getItem("notes");
    if (storedNotes) {
        textarea.value = storedNotes;
    }
});
```

**Try it:**
Reload the page and see your notes appear automatically if they were saved.

---


## 6. Final Challenge
Build a simple notes app that lets users enter, append, show, and save notes. Make sure notes persist after reloading the page.

---

## 7. Further Exercises & Improvements

Try these additional exercises to improve your notes app and deepen your understanding:

### Accessibility
- Add a `<label>` for your textarea and use `aria-label` or a descriptive `placeholder`.

### User Feedback
- Display a status message on the page when notes are saved or loaded, instead of just using `alert`.
- Show a message if there are no saved notes when the page loads.

### Error Handling
- Prevent saving empty notes and show a warning if the textarea is blank.
- Handle possible exceptions with localStorage (e.g., quota exceeded).

### Styling
- Add more spacing or grouping for buttons using Bootstrap classes.
- Use Bootstrap grid or card components for a more polished layout.

### Code Organization
- Move your JavaScript code to a separate file and link it in your HTML.
- Use `const` for variables that don’t change.

### Features
- Add a button to clear notes from localStorage.
- Allow users to save multiple notes or a list of notes instead of just one string.

---

## 8. Instructor Tips
- Demonstrate each feature step by step.
- Encourage students to experiment with textarea size and event handlers.
- Show how localStorage works and discuss its limitations (e.g., only stores strings, limited size).
- Use browser dev tools to inspect localStorage and debug JavaScript.

---

Congratulations! You’ve completed Topic 01 and learned how to build interactive web features with textareas and localStorage.
