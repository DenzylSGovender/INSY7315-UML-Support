# UML Diagrams and UX Journey Guide

## Overview

This guide introduces the most common diagrams used during systems analysis and software design. Each diagram provides a different perspective of the same system and helps developers communicate ideas effectively.

> **Note:** A UX Journey Diagram is **not** a UML diagram. It is a User Experience (UX) artefact used to understand the user's interaction with a system.

---

# Learning Outcomes

After completing this guide, you should be able to:

- Explain the purpose of different UML diagrams.
- Identify when each diagram should be used.
- Create a Class Diagram.
- Create a Sequence Diagram.
- Create a State Diagram.
- Create a UX Journey Diagram.
- Compare the differences between these modelling techniques.

---

# UML Diagrams

## What is UML?

**Unified Modeling Language (UML)** is a standardized visual language used to model, design, and document software systems.

Instead of writing long descriptions, UML uses diagrams to illustrate:

- System structure
- User interactions
- Object relationships
- System behaviour
- Object lifecycles

Think of UML as the **blueprint** of a software system.

---

# 1. Class Diagram

## Purpose

A Class Diagram models the **structure** of a software system.

It shows:

- Classes
- Attributes
- Methods
- Relationships between classes

### Example

```
+----------------+
|    Student     |
+----------------+
| -studentID     |
| -name          |
+----------------+
| +borrowBook()  |
+----------------+

         |
         | borrows
         |
         V

+----------------+
|      Book      |
+----------------+
| -bookID        |
| -title         |
| -available     |
+----------------+
| +checkStatus() |
+----------------+
```

### Questions it answers

- What objects exist?
- What information do they store?
- What behaviour do they have?
- How are they connected?

---

# 2. Sequence Diagram

## Purpose

A Sequence Diagram shows **how objects communicate over time**.

It focuses on:

- Message passing
- Order of execution
- Interaction between objects

### Example

```
Student        Librarian          Book
   |                |               |
   | Borrow Book    |               |
   |--------------->|               |
   |                | Check Status  |
   |                |-------------->|
   |                | Available     |
   |                |<--------------|
   |                | Issue Book    |
   |<---------------|               |
```

### Questions it answers

- What happens first?
- Who communicates with whom?
- What is the order of events?

---

# 3. State Diagram

## Purpose

A State Diagram illustrates how a single object changes state during its lifetime.

### Example

```
        +-----------+
        | Available |
        +-----------+
              |
        Borrow Book
              |
              V
        +-----------+
        | Borrowed  |
        +-----------+
              |
        Return Book
              |
              V
        +-----------+
        | Available |
        +-----------+
```

### Questions it answers

- What states can an object be in?
- What events cause the object to change state?

---

# 4. UX Journey Diagram

## Purpose

A UX Journey Diagram focuses on the **user's experience** while interacting with a system.

Unlike UML, it models the user's journey rather than the software itself.

### Example

```
Start
   |
   v
Search Book
   |
   v
Select Book
   |
   v
Borrow Book
   |
   v
Receive Confirmation
   |
   v
End
```

Alternative outcomes:

- Book unavailable
- Search again
- Join waiting list

### Questions it answers

- What does the user do?
- What does the system respond with?
- Where could the user experience problems?

---

# Comparing the Diagrams

| Diagram | Focus | Answers |
|----------|-------|---------|
| UX Journey Diagram | User Experience | What does the user do? |
| Class Diagram | Structure | What objects exist? |
| Sequence Diagram | Interaction | How do objects communicate? |
| State Diagram | Behaviour | How does an object change over time? |

---

# Example Scenario

A student wants to borrow a library book.

1. The student searches for a book.
2. The system displays available books.
3. The student selects a book.
4. The librarian issues the book.
5. The system marks the book as borrowed.

Using this single scenario, different diagrams show different aspects of the same system.

| Diagram | What it Shows |
|----------|---------------|
| UX Journey | User experience |
| Class Diagram | System structure |
| Sequence Diagram | Flow of communication |
| State Diagram | Book lifecycle |

---

# Recommended Learning Resources

## UML Specification

- https://www.omg.org/spec/UML

---

## Lucidchart

- https://www.lucidchart.com/pages/uml-diagrams

Excellent visual examples of:

- Class Diagrams
- Sequence Diagrams
- State Diagrams
- Activity Diagrams
- Use Case Diagrams

---

## GeeksforGeeks

https://www.geeksforgeeks.org/unified-modeling-language-uml-introduction/

---

# UX Journey Resources

## Nielsen Norman Group

https://www.nngroup.com/articles/journey-mapping-101/

---

## Lucidchart User Journey Maps

https://www.lucidchart.com/pages/user-journey-map

---

# Recommended Diagramming Tools

### diagrams.net (draw.io)

https://app.diagrams.net

---

### Visual Paradigm Online

https://online.visual-paradigm.com

---

### Lucidchart

https://www.lucidchart.com

---

# Summary

Each diagram tells part of the same story.

- **UX Journey Diagram** – Focuses on the user's experience.
- **Class Diagram** – Describes the structure of the system.
- **Sequence Diagram** – Describes interactions between objects.
- **State Diagram** – Describes how an object's state changes over time.

Professional software engineers often create multiple diagrams for the same system because each one provides a different perspective that helps stakeholders, developers, and testers understand the software.

If there are any sites that are not working, please reach out to me.
