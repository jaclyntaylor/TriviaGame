# Trivia App Assignment

In this assignment, you will build a complete trivia application using **JavaScript**, **jQuery**, **Axios**, **localStorage**, and **sessionStorage**.

---

## Overview

Your task is to create a trivia quiz that:

* Fetches true/false questions from an API.
* Saves the questions in `localStorage`.
* Saves the correct answer for the current question in `sessionStorage`.
* Displays questions using jQuery.
* Lets the user answer and receive feedback using jQuery.
* Automatically loads the next question.
* Refetches new questions once the stored questions run out.

---

## API

Use Axios to fetch 10 true/false questions:

```
https://opentdb.com/api.php?amount=10&type=boolean
```

---

## Requirements

### 1. Page Load Behavior

When the page loads:

* Automatically load a trivia question.
* If questions exist in `localStorage`, use those.
* If not, fetch a new batch from the API and save them.

### 2. Loading Questions

Create a function that:

* Retrieves the stored trivia array from `localStorage`.
* Converts it from JSON.
* Removes one question from the array.
* Saves the remaining questions back to `localStorage`.
* Stores the correct answer for that question in `sessionStorage`.
* Displays the question text on the page using jQuery.
* Deletes the key from `localStorage` when no questions remain.

### 3. Displaying the Question

Use jQuery to:

* Insert the question text into a DOM element.
* Ensure HTML entities (like `&quot;`) appear correctly.

### 4. Handling User Answers

You must:

* Create click handlers for two buttons: **True** and **False**.
* Compare the clicked value to the value stored in `sessionStorage`.
* If correct:

  * Alert **“Correct!”**
  * Load a new question.
* If incorrect:

  * Alert **“Try again”**.

### 5. Storage Rules

* `localStorage` → Stores the batch of 10 questions.
  Survives page reload.

* `sessionStorage` → Stores only the current correct answer.
  Clears when the tab is closed.

