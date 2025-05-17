# NNIIT
# Smart Flashcard System Backend

A simple backend API built with **FastAPI** to support a Smart Flashcard System. This backend allows users to add flashcards with just a question and answer, and automatically infers the **subject** of each flashcard using rule-based keyword matching. Students can then retrieve a mixed batch of flashcards from multiple subjects intelligently.

---

## Project Overview

Traditional flashcard apps require users to manually tag subjects, which can be cumbersome. This backend simplifies the process by automatically detecting the subject of each flashcard based on keywords in the question. For example, a question containing “photosynthesis” will be categorized under “Biology.”  
Later, when students request flashcards, the system returns a diverse, shuffled set of flashcards spanning different subjects, tailored to that student.

---

## Features

- **Add Flashcard** (`POST /flashcard`):  
  Accepts flashcard data (`student_id`, `question`, `answer`) and infers the subject automatically. Saves the flashcard for that student.

- **Get Flashcards by Mixed Subjects** (`GET /get-subject`):  
  Retrieves a shuffled list of flashcards for a student, mixing cards from different subjects up to a requested limit.

- **Rule-Based Subject Classification**:  
  Uses predefined keywords mapped to subjects for inference, no training data required.

- **Persistent Storage**:  
  Flashcards are stored in a JSON file (`flashcards.json`) for simplicity and easy testing.


