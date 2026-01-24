# Project Deadline & Importance Feature

## Overview

The Project Deadline & Importance feature allows users to mark project deadlines and set importance levels for better project management and organization. This feature uses browser local storage to persist your deadline data, so it's available across sessions.

## Features

### 1. **Set Project Deadlines**
- Click the calendar icon (📅) on any project card or list item
- Enter a deadline date
- Select an importance level (Low, Medium, High, Critical)
- Add optional notes about the project
- Save your deadline - it's automatically persisted

### 2. **Visual Indicators**
- **Deadline Badges**: Display on cards showing the deadline date and time remaining
- **Importance Colors**:
  - 🟢 **Green**: Low importance
  - 🟠 **Orange**: Medium importance
  - 🔴 **Red**: High importance
  - 🔴 **Dark Red**: Critical importance

- **Status Indicators**:
  - Green badge: Normal (more than 7 days)
  - Orange badge: Soon (3-7 days)
  - Red badge: Urgent (1-3 days)
  - Dark Red badge: Overdue (past deadline)

### 3. **Sort & Filter**
Use the Sort dropdown to organize projects by:
- **By Deadline**: Projects sorted by due date (earliest first)
- **By Importance**: Projects sorted by importance level (Critical to Low)

### 4. **Deadline Management**
- **View**: See current deadline info when opening the modal
- **Update**: Modify deadlines and importance anytime
- **Delete**: Remove deadlines when no longer needed

## How to Use

### Setting a Deadline

1. Navigate to the **Projects** section on OpenPlayground
2. Find the project you want to manage
3. Click the **calendar icon** (📅) on the project card or list item
4. In the modal that appears:
   - Select a **Deadline Date** (date picker)
   - Choose an **Importance Level** by clicking one of the 4 options
   - Optionally add **Notes** about the project
   - Click **Save Deadline**

### Updating a Deadline

1. Click the calendar icon on a project that already has a deadline
2. The modal shows your current deadline information
3. Make any changes and click **Save Deadline**

### Removing a Deadline

1. Click the calendar icon on a project with a deadline
2. Click the **Remove** button (red delete button)
3. Confirm the deletion

### Sorting by Deadline/Importance

1. Open the **Sort** dropdown in the projects section
2. Select either:
   - **By Deadline**: Shows projects with deadlines first (sorted by date), then projects without deadlines
   - **By Importance**: Shows projects by importance level (Critical → High → Medium → Low), then projects without set importance

## Data Storage

- **Storage Location**: Browser's localStorage
- **Data Key**: `projectDeadlines`
- **Persistence**: Your deadline data persists across browser sessions
- **Privacy**: All data stays locally in your browser - never sent to servers

### Export/Import Data

Coming soon! You'll be able to export and import deadline data as JSON for backup and transfer purposes.

## Importance Levels Explained

| Level | Icon | Color | Use Case |
|-------|------|-------|----------|
| **Low** | ↓ | Green | Nice-to-have projects, side activities |
| **Medium** | − | Orange | Regular projects, standard priority |
| **High** | ↑ | Red | Important projects, should prioritize |
| **Critical** | ⚠ | Dark Red | Urgent projects, highest priority |

## Status Messages

The deadline badge shows helpful status information:

- **"Due today"** - Deadline is today
- **"Due tomorrow"** - Deadline is tomorrow
- **"X days remaining"** - Days left until deadline
- **"X days overdue"** - How many days past the deadline (appears in dark red)

## Tips & Best Practices

✅ **Do:**
- Set realistic deadlines to avoid overwhelm
- Use importance levels consistently
- Review your deadlines regularly
- Update deadlines as priorities change

❌ **Don't:**
- Overload everything as "Critical"
- Ignore overdue badges
- Set deadlines too far in the future (harder to track)

## Browser Compatibility

This feature works in all modern browsers that support:
- localStorage API
- ES6 modules
- Date picker inputs

Supported browsers: Chrome, Firefox, Safari, Edge (latest versions)

## Troubleshooting

### Deadlines not showing?
- Check if localStorage is enabled in your browser
- Try refreshing the page
- Check browser console for errors (F12 → Console tab)

### Data lost after closing browser?
- Ensure localStorage is not being cleared
- Check browser privacy settings
- Look for any extension that might be clearing storage

### Modal not opening?
- Ensure JavaScript is enabled
- Check that the calendar icon is being clicked correctly
- Look for console errors (F12 → Console)

## Features Coming Soon

- 📊 Deadline dashboard with statistics
- 📧 Notification/reminder system
- 📤 Export/import functionality
- 🔄 Recurring deadlines
- 📱 Mobile app integration

## Technical Details

The feature is built with:
- **projectDeadlineManager.js**: Core logic for managing deadline data
- **deadlineUI.js**: User interface and modal management
- **deadline.css**: All styling for deadline components
- **cardRenderer.js**: Integration with project cards

All data is managed client-side using browser localStorage API.

## Feedback & Issues

Found a bug or have a feature suggestion? 
- Create an issue on GitHub
- Check the [CONTRIBUTING.md](../CONTRIBUTING.md) guide
- Review [DEBUGGING_GUIDE.md](../DEBUGGING_GUIDE.md) for troubleshooting

---

**Last Updated**: January 2026
**Version**: 1.0
