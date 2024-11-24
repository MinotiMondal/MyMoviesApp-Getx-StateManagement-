# My Movies Application

This Flutter application demonstrates a movie list with individual  details for each movie. 

---

## Architectural Choices
 
### State Management
- **`GetX`**:
    - Handles reactive state management, dependency injection, and routing.
    - Reduces boilerplate while improving code maintainability.

### Modular Design
- Divided into controllers and views for better separation of concerns:
    - **`MovieListView`**: Displays the list of Movie.
    - **`MovieDetailView`**: Shows detailed information about a selected Movie.
    - **`FavouriteList`**: From movie details favourite icon click it will go to Favourite lidt screen (Sqflite database)


---

## Third-Party Libraries


1. **`http`**
    - Handles API requests for fetching post data.

2. **`get`**
    - Provides state management, dependency injection, and navigation.
    - Simplifies app development by offering a single, unified approach.

3. **`visibility_detector`**
    - Monitors the visibility of list items (posts) to start or pause timers dynamically based on visibility.

---

## How to Run the Application

### Prerequisites
- Flutter SDK (latest stable version)
- Android Studio, VS Code, Xocode or any preferred IDE
- An emulator or a physical device for testing

### Setup
1. Clone the repository:
   ```
   git clone <repository-url>
   cd <repository-folder>
2. Install dependencies:
   ```
   flutter pub get
3. Run the application:
   ```
   flutter run

## Application Features

### Movie List:
- Displays a list of posts, each with its own independent timer.
- When a post is clicked, its timer pauses, while the timers for other posts continue running.
- When navigating back to the post list, the paused timer for the clicked post resumes from where it left off.

### Mocie Details:
- Shows the detailed view of a selected post.
- The timer for the post pauses when the user clicks on it and resumes correctly when navigating back, ensuring the timer state is preserved across screens.


## Directory Structure

lib/


|______controllers





|          |_______movieController.dart







|________views


|           |______post_list_vie


|           |______post_detail_view.dart


|________main.dart          
