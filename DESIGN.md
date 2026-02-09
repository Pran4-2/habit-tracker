# Habit Tracking Dashboard - Design Document

## Overview
This is a simple, interactive habit tracking dashboard that helps you build and maintain daily habits. Track your progress, earn XP points, and celebrate your achievements!

## Dashboard Structure

### 1. Header Section
- **Dashboard Title**: "Habit Tracker"
- **Current Date Display**: Shows today's date
- **Overall Stats**: Quick view of today's progress

### 2. Daily Checklist Section
- List of all active habits for the day
- Each habit has:
  - Checkbox/toggle to mark as complete
  - Habit name
  - XP points (weight) display
  - Quick edit button
- Color-coded by completion status

### 3. Progress Section
- **Daily Progress Bar**: Visual bar showing today's completion percentage
- **XP Earned Today**: Current XP vs. Possible XP
- **Streak Counter**: Number of consecutive days completed
- **Weekly Score**: XP earned Mon-Fri (with weekend toggle)
- **Monthly Score**: Total XP for the current month

### 4. Celebration Section
- Dynamic messages when milestones are reached:
  - Day completed (all habits done)
  - Week completed (5 or 7 days based on settings)
  - Month milestone (20+ days completed)
  - Streak milestones (7, 14, 30, 60, 90 days)

### 5. Habit Management Section
- **Add New Habit Button**: Opens form to create a habit
- **Edit Habits**: Modify name and XP weight
- **Delete Habits**: Remove habits (with confirmation)
- **Settings**: Toggle weekend tracking, customize XP weights

## Data Model

### Habit Object
```json
{
  "id": "unique-id",
  "name": "Morning Exercise",
  "xp": 10,
  "active": true,
  "createdAt": "2026-01-01"
}
```

### Daily Log Object
```json
{
  "date": "2026-02-09",
  "completedHabits": ["habit-id-1", "habit-id-2"],
  "totalXP": 25,
  "possibleXP": 50
}
```

### User Settings Object
```json
{
  "includeWeekends": false,
  "celebrationMessages": true,
  "theme": "light"
}
```

### Streak Data
```json
{
  "currentStreak": 5,
  "longestStreak": 15,
  "lastCompletedDate": "2026-02-08"
}
```

## Scoring Logic

### XP System
1. **Default XP Values**: Each habit has a weight (default: 10 XP)
2. **Custom Weights**: Users can assign 1-100 XP per habit based on difficulty
3. **Daily Total**: Sum of XP from all completed habits
4. **Daily Possible**: Sum of XP from all active habits

### Weekly Score
1. **Default (Mon-Fri)**: Sum XP from Monday to Friday
2. **With Weekends**: Optionally include Saturday and Sunday
3. **Weekly Target**: 100% = All habits completed all tracked days
4. **Display**: Shows XP earned / XP possible

### Monthly Score
1. **Calendar Month**: Sum of all daily XP in current month
2. **Days Tracked**: Count of days where at least one habit was completed
3. **Monthly Average**: Total XP / Days in month
4. **Display**: Shows total XP and days completed

### Streak Rules
1. **Streak Definition**: Consecutive days where 80%+ of daily XP was earned
2. **Streak Breaks**: Missing a day or earning <80% breaks the streak
3. **Grace Period**: None (strict counting)
4. **Streak Milestones**: 7, 14, 30, 60, 90, 180, 365 days

### Celebration Triggers
1. **Daily Complete**: All habits checked off (100% daily XP)
2. **Weekly Complete**: All habits completed all week
3. **Perfect Month**: 100% completion for 25+ days in a month
4. **Streak Milestones**: Special messages at 7, 30, 90+ day streaks

## Step-by-Step Build Plan

### Phase 1: Foundation (HTML Structure)
1. Create index.html with semantic HTML5 structure
2. Add all dashboard sections (header, checklist, progress, management)
3. Include basic form elements for habit management

### Phase 2: Styling (CSS)
1. Create clean, simple styles with good contrast
2. Implement responsive layout (mobile-friendly)
3. Add progress bar styles and animations
4. Style celebration messages with visual appeal

### Phase 3: Core Functionality (JavaScript)
1. **Data Management**:
   - Initialize default habits
   - Load/save to localStorage
   - CRUD operations for habits

2. **Daily Checklist**:
   - Render habits for today
   - Handle checkbox toggles
   - Update progress in real-time

3. **Progress Tracking**:
   - Calculate daily progress percentage
   - Update progress bar visually
   - Display XP earned vs. possible

4. **Scoring Systems**:
   - Weekly score calculation (with weekend toggle)
   - Monthly score aggregation
   - Streak calculation and tracking

5. **Celebrations**:
   - Detect completion milestones
   - Display appropriate messages
   - Add confetti or animations (optional)

6. **Habit Management**:
   - Add new habit form
   - Edit existing habits
   - Delete with confirmation

### Phase 4: Polish & Testing
1. Test all features manually
2. Add helpful tooltips and instructions
3. Ensure data persists correctly
4. Mobile responsive testing
5. Cross-browser compatibility check

## Technical Approach

### Technology Stack
- **HTML5**: Structure and semantics
- **CSS3**: Styling with flexbox/grid for layout
- **Vanilla JavaScript**: No framework needed (keep it simple)
- **LocalStorage**: Client-side data persistence

### Why No Framework?
- User is not technical
- Single-file application is easier to understand
- No build process or dependencies
- Can be opened directly in any browser
- Easy to customize and modify

### File Structure
```
habit-tracker/
├── index.html          (Complete dashboard - HTML, CSS, JS in one file)
├── README.md           (User instructions)
└── DESIGN.md          (This document)
```

## User Instructions (Simple Language)

### How to Get Started
1. **Open the File**: Double-click index.html to open in your web browser
2. **Add Habits**: Click "Add Habit" and enter habit name and XP points
3. **Daily Use**: Check off habits as you complete them each day
4. **Track Progress**: Watch your XP grow and streak build
5. **Stay Motivated**: Celebrate when you hit milestones!

### Understanding XP Points
- **Easy habits**: 5-10 XP (e.g., drink water)
- **Medium habits**: 10-20 XP (e.g., 15 min exercise)
- **Hard habits**: 20-50 XP (e.g., 1 hour study)
- **Major habits**: 50-100 XP (e.g., complete project)

### Tips for Success
1. Start with 3-5 habits (don't overwhelm yourself)
2. Be honest - check only when truly completed
3. Adjust XP weights based on actual difficulty
4. Use the streak as motivation
5. Celebrate small wins!

## Future Enhancements (Optional)
- Export/import data functionality
- Habit categories/tags
- Custom habit schedules (not every day)
- Charts and graphs for trends
- Multiple user profiles
- Backup to cloud storage
- Mobile app version
