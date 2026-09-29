# Bibliotheca - Dual-Frame Book Information Portal

A web application designed for browsing book information using a two-part frame architecture:
- **Left Part**: Interactive Books List & Catalog (`book_list.html`), equipped with search, category filtering, and metadata preview.
- **Right Part**: Deep Book Information Display (`book_default.html` & individual book pages `book1_quantum.html` – `book6_philosophy.html`), loaded seamlessly using the frame target protocol (`target="rightFrame"`).

---

## Architecture Overview

```
                      +---------------------------------------+
                      |         Top Navigation Header         |
                      +-------------------+-------------------+
                      |                   |                   |
                      |    LEFT FRAME     |    RIGHT FRAME    |
                      | (name="leftFrame")| (name="rightFrame")|
                      |                   |                   |
                      |  book_list.html   | book_default.html |
                      |                   |         or        |
                      |  [Book 1] --------+--> book1_quantum  |
                      |  [Book 2] --------+--> book2_cloud    |
                      |  [Book 3] --------+--> book3_celest.  |
                      |  [Book 4] --------+--> book4_botan.   |
                      |  [Book 5] --------+--> book5_cyber.   |
                      |  [Book 6] --------+--> book6_philo.   |
                      |                   |                   |
                      +-------------------+-------------------+
                      |           Bottom Status Bar           |
                      +---------------------------------------+
```

---

## File Structure

| File | Description |
| :--- | :--- |
| [`index.html`](file:///c:/lab3/index.html) | **Main Entry Point**: Split-frame layout (`<iframe>`), interactive resizer, navigation & status bar. |
| [`index_frameset.html`](file:///c:/lab3/index_frameset.html) | **Classic HTML4 `<frameset>`**: Pure `<frameset cols="30%, 70%">` version for academic lab compliance. |
| [`book_list.html`](file:///c:/lab3/book_list.html) | **Left Frame**: Book catalog list with live search, genre filters, and `target="rightFrame"` links. |
| [`book_default.html`](file:///c:/lab3/book_default.html) | **Right Frame (Initial)**: Overview welcome screen, statistics, and quick feature cards. |
| [`book1_quantum.html`](file:///c:/lab3/book1_quantum.html) | **Right Frame**: *The Quantum Enigma: Physics & Reality* by Dr. Evelyn Reed. |
| [`book2_cloud.html`](file:///c:/lab3/book2_cloud.html) | **Right Frame**: *Architecting Modern Cloud Systems* by Marcus Vance. |
| [`book3_celestial.html`](file:///c:/lab3/book3_celestial.html) | **Right Frame**: *Chronicles of the Celestial Void* by Lyra Thorne. |
| [`book4_botanical.html`](file:///c:/lab3/book4_botanical.html) | **Right Frame**: *The Secret Life of Ancient Flora* by Dr. Alistair Finch. |
| [`book5_cyberpunk.html`](file:///c:/lab3/book5_cyberpunk.html) | **Right Frame**: *Cybernetic Dreams: Mind, Machine & Society* by Elena Rostova. |
| [`book6_philosophy.html`](file:///c:/lab3/book6_philosophy.html) | **Right Frame**: *The Golden Age of Philosophy* by Arthur Sterling. |
| [`css/main.css`](file:///c:/lab3/css/main.css) | Main shell styling, header, footer, glassmorphic accents, and resizer. |
| [`css/frame_left.css`](file:///c:/lab3/css/frame_left.css) | Styling for the catalog list, search input, badges, and thumbnail cards. |
| [`css/frame_right.css`](file:///c:/lab3/css/frame_right.css) | Styling for book detail views: 3D book covers, specs table, synopsis, TOC, reviews. |
| [`images/`](file:///c:/lab3/images/) | High-resolution custom book cover artwork. |

---

## How to Run

1. **Direct Browser Execution**:
   Double-click [`index.html`](file:///c:/lab3/index.html) or [`index_frameset.html`](file:///c:/lab3/index_frameset.html) to open in Microsoft Edge, Google Chrome, or Mozilla Firefox.

2. **Using Local HTTP Server**:
   ```bash
   cd c:\lab3
   python -m http.server 8000
   ```
   Open `http://localhost:8000/index.html` in your browser.
