# Browser Navigation History – Stack (based on Linked List)

This project simulates the navigation history of a web browser, implementing the back and forward history functionality using two distinct approaches: a custom stack (`MyStack`) based on a singly linked list and a list-based solution using Java’s `LinkedList`. The system supports operations like visiting pages, going back to previous pages, and navigating forward.

## Project Overview

The main objective is to simulate the web browser's navigation history, focusing on two key features:
1. **Back Navigation**: Allows users to go back to previously visited pages.
2. **Forward Navigation**: Enables users to move forward to pages they navigated away from.

### Two Approaches:
1. **List-Based Navigation**: Uses Java’s `LinkedList` to manage back and forward history.
2. **Stack-Based Navigation**: Implements a custom stack data structure (`MyStack`) using a singly linked list.

## Features
- **Dynamic Stack Management**: The custom `MyStack` class supports dynamic memory allocation, allowing the stack size to grow or shrink based on the number of visited pages.
- **LIFO Behavior**: Both stacks (back and forward) operate using the Last-In-First-Out (LIFO) principle, ensuring the most recently visited pages are handled first.
- **Navigation Consistency**: Ensures the back and forward navigation is accurate and consistent, even when switching between back and forward operations.

## System Design

The system uses two stacks:
- **Back Stack**: Stores pages visited by the user in a backward direction.
- **Forward Stack**: Stores pages that the user has navigated away from.

The custom stack (`MyStack`) is implemented using a singly linked list where each node represents a page. This setup ensures that operations like pushing, popping, and peeking are efficient with O(1) time complexity.

## System Operations

- **visitPage(String url)**: Navigates to a new page and clears the forward stack.
- **back()**: Navigates back to the previous page by popping from the back stack.
- **forward()**: Navigates forward to the next page by popping from the forward stack.

### Example Flow:
1. **Visiting Pages**: Navigates through pages (`Home -> page1.com -> page2.com -> page3.com`).
2. **Back Navigation**: Pressing "back" navigates to the previous page (`page2.com -> page1.com -> Home`).
3. **Forward Navigation**: Pressing "forward" restores the next page (`page2.com -> page3.com`).

## Testing

JUnit tests were implemented to ensure the correctness of the system:
- **Basic Functionality**: Verifies core operations (e.g., visiting pages, back, and forward navigation).
- **Edge Cases**: Handles cases like back navigation from "Home" or forward navigation when no history is available.
- **Stress Testing**: Evaluates the system's performance with large datasets and numerous operations.

### Test Coverage:
- Push/Pop operations
- Back/Forward navigation accuracy
- Handling of empty stacks and invalid operations


## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Aasimshah7/Browser-Navigation-History.git
