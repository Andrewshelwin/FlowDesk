# FlowDesk
Task Management UI App built using Kotlin and XML. Includes Home, Tasks, and Progress screens with Bottom Navigation.

# FlowDesk - Task Management App

A modern, beautifully designed Android task management application built with Kotlin and Material Design 3.

## Features

### Home Screen
- Welcome header with profile picture
- 4 stat cards showing task statistics:
  - Today's tasks
  - Goals setup
  - On Hold tasks
  - Past Due tasks
- Today's task list with detailed task cards
- Material Design FAB for adding new tasks

### Tasks Screen
- All tasks view
- Filter chips: All Tasks, In Progress, Completed
- Comprehensive task list with:
  - Time and duration
  - Task title and description
  - Participant avatars
  - Action buttons

### Progress Screen
- Weekly calendar view
- Focus mode status card with visualization
- Activity bar chart showing daily hours
- Stats cards showing completed tasks

### Profile Screen
- User profile display with avatar
- Personal information display:
  - Username
  - Email address
  - Phone number
- Custom toolbar with back navigation
- Profile picture editing capability
- Clean, card-based layout for user information
- Consistent design language with other screens

## Tech Stack

- **Language**: Kotlin
- **UI**: Material Design 3
- **Architecture**: MVVM with Fragments
- **Navigation**: Android Navigation Component
- **Layout**: ConstraintLayout, LinearLayout
- **RecyclerView**: For dynamic lists
- **ViewBinding**: Type-safe view access

## Design Features

- **Color Scheme**:
  - Primary: #6C63FF (Purple)
  - Background: Lavender (#ECEBFF)
  - Card backgrounds: Semi-transparent white (#E6FFFFFF)
  - Accent cards: Peach & Blue

- **Typography**: Sans-serif with medium and bold weights
- **Corner Radius**: Rounded cards (16-22dp)
- **Elevation**: Subtle shadows for depth
- **Icons**: Material icons throughout

## Project Structure

```
app/src/main/
├── java/com/example/flowdesk/
│   ├── adapters/
│   │   └── TaskAdapter.kt
│   ├── models/
│   │   ├── Task.kt
│   │   └── StatCard.kt
│   ├── ui/
│   │   ├── HomeFragment.kt
│   │   ├── TasksFragment.kt
│   │   ├── ProgressFragment.kt
│   │   └── ProfileFragment.kt
│   └── MainActivity.kt
└── res/
    ├── layout/
    │   ├── activity_main.xml
    │   ├── fragment_home.xml
    │   ├── fragment_tasks.xml
    │   ├── fragment_progress.xml
    │   ├── fragment_profile.xml
    │   ├── item_stat_card.xml
    │   └── item_task_card.xml
    ├── values/
    │   ├── colors.xml
    │   ├── strings.xml
    │   └── themes.xml
    ├── drawable/
    ├── menu/
    └── navigation/
```

## Setup Instructions

1. **Prerequisites**:
   - Android Studio Arctic Fox or later
   - JDK 17
   - Android SDK 24+

2. **Build**:
   ```bash
   ./gradlew build
   ```

3. **Run**:
   - Open project in Android Studio
   - Sync Gradle
   - Run on emulator or device (API 24+)

## Key Components

### MainActivity
- Hosts NavHostFragment
- Sets up bottom navigation
- Handles FAB interactions

### HomeFragment
- Displays 4 stat cards
- Shows today's task list
- Profile header with notifications

### TasksFragment
- Complete task list
- Filter functionality
- Task management

### ProgressFragment
- Calendar week view
- Focus mode visualization
- Progress statistics

### ProfileFragment
- User profile information display
- Custom toolbar with back navigation
- Profile data management
- Personal information cards:
  - Username with @ handle
  - Email address
  - Phone number
- Profile picture with edit capability
- ViewBinding for type-safe view access

### TaskAdapter
- RecyclerView adapter for tasks
- Binds task data to card views
- Handles task item clicks

## Customization

### Colors
Edit `res/values/colors.xml` to change the color scheme.

### Layouts
All layouts use Material Design 3 components and can be customized in their respective XML files.

### Task Data
Update the task lists in fragments with your own data source (database, API, etc.).

### Profile Data
Modify the `setupProfileData()` method in `ProfileFragment.kt` to integrate with your user management system or database.

## Future Enhancements

- Task creation and editing
- Task completion tracking
- Focus mode timer
- Notifications
- Cloud sync
- Dark theme
- Task categories
- Priority levels
- Search functionality
- Profile editing and image upload
- Settings and preferences
- Multi-user support
- Data persistence with Room database
- Backend API integration

