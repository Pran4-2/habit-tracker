# 🎯 Habit Tracker Dashboard

A simple, interactive habit tracking dashboard to help you build and maintain daily habits. Track your progress, earn XP points, build streaks, and celebrate your achievements!

## 🚀 Quick Start

### How to Use
1. **Open the Dashboard**: Simply double-click on `index.html` to open it in your web browser
2. **No Installation Required**: Works completely in your browser, no internet connection needed
3. **Your Data is Private**: All data is stored locally on your computer

### First Time Setup
1. Open `index.html` in any modern web browser (Chrome, Firefox, Safari, Edge)
2. You'll see 3 example habits to get you started
3. Click "Add Habit" to create your own habits
4. Check off habits as you complete them each day

## ✨ Features

### 📋 Daily Checklist
- View all your habits for the day
- Simple checkboxes to mark habits as complete
- Real-time progress updates
- Color-coded completion status

### 📊 Progress Tracking
- **Daily Progress Bar**: Visual representation of your daily completion
- **XP System**: Earn points for each completed habit
- **Current Streak**: See how many consecutive days you've maintained your habits
- **Weekly Score**: Track your XP for the week (Mon-Fri by default)
- **Monthly Score**: Total XP earned this month

### 🎉 Celebrations
Get motivational messages when you:
- Complete all habits for the day (100%)
- Hit streak milestones (7, 14, 30, 60, 90+ days)
- Achieve weekly and monthly goals

### ⚙️ Habit Management
- **Add New Habits**: Create custom habits with personalized XP values
- **Edit Habits**: Change habit names and XP points anytime
- **Delete Habits**: Remove habits you no longer need
- **Flexible Settings**: Toggle weekend tracking on/off

## 📖 Understanding the System

### What is XP?
XP (Experience Points) represents the value or difficulty of each habit:
- **Easy habits** (5-10 XP): Small tasks like "Drink water" or "Make bed"
- **Medium habits** (10-20 XP): Regular activities like "15 min exercise" or "Meditate"
- **Hard habits** (20-50 XP): Challenging tasks like "1 hour study" or "Run 5K"
- **Major habits** (50-100 XP): Big commitments like "Complete project" or "Deep work session"

### How Scoring Works

#### Daily Score
- Complete habits to earn their XP
- Progress bar shows percentage completed
- Aim for 100% each day!

#### Weekly Score
- Sums up XP from Monday to Friday (by default)
- Toggle "Include weekends" to count Saturday and Sunday
- Great for seeing weekly consistency

#### Monthly Score
- Total XP earned during the current month
- Tracks how many days you completed habits
- Reset automatically each month

#### Streak Counter
- Counts consecutive days where you completed 80%+ of your daily XP
- Missing a day or earning <80% breaks the streak
- Build long streaks for maximum motivation!

## 💡 Tips for Success

### Starting Out
1. **Begin Small**: Start with 3-5 habits. Don't overwhelm yourself!
2. **Be Specific**: "Exercise for 15 minutes" is better than "Exercise"
3. **Set Realistic XP**: Match XP to actual difficulty for you
4. **Check Daily**: Make checking habits part of your routine

### Building Habits
1. **Morning Review**: Check the dashboard first thing in the morning
2. **Evening Update**: Mark off completed habits before bed
3. **Be Honest**: Only check habits you actually completed
4. **Adjust as Needed**: Edit habits if they're too easy or too hard

### Staying Motivated
1. **Watch Your Streak**: Try to maintain or beat your longest streak
2. **Celebrate Wins**: Enjoy the celebration messages!
3. **Track Progress**: See your weekly and monthly scores grow
4. **Adjust XP**: Make harder habits worth more points

## 🔧 Technical Details

### Technology
- **Pure HTML/CSS/JavaScript**: No frameworks or dependencies
- **LocalStorage**: Data saved in your browser
- **Single File**: Everything in one HTML file
- **Responsive**: Works on desktop and mobile

### Data Storage
Your data is stored locally in your browser using LocalStorage:
- Habits and their XP values
- Daily completion logs
- Streak information
- Settings preferences

**Important**: Data is tied to your browser. If you:
- Clear browser data, you'll lose your habits
- Use a different browser, you'll start fresh
- Use private/incognito mode, data won't persist

### Browser Compatibility
Works in all modern browsers:
- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Opera

## 📱 Mobile Use

The dashboard is fully responsive and works great on mobile devices:
1. Open `index.html` on your phone's browser
2. Add to home screen for quick access
3. Use just like the desktop version

## 🎨 Customization

### Changing Colors
The dashboard uses a purple gradient theme. To customize:
1. Open `index.html` in a text editor
2. Find the `<style>` section
3. Modify the color values (search for `#667eea` and `#764ba2`)

### Adjusting XP Ranges
Default XP range is 1-100. To change:
1. Open `index.html` in a text editor
2. Find `<input type="number" id="habitXP" min="1" max="100"`
3. Adjust `min` and `max` values

## 📋 Complete Feature List

### Dashboard Sections
1. **Header**: Title, current date, and quick stats
2. **Stats Overview**: 4 cards showing key metrics
3. **Progress Section**: Visual progress bar and XP counter
4. **Daily Checklist**: All habits with checkboxes
5. **Settings**: Toggle options for customization

### Functionality
- ✅ Add unlimited habits
- ✅ Edit habit names and XP values
- ✅ Delete habits with confirmation
- ✅ Toggle habit completion
- ✅ Real-time progress updates
- ✅ Daily/weekly/monthly scoring
- ✅ Streak tracking
- ✅ Celebration messages
- ✅ Weekend toggle for weekly score
- ✅ Data persistence (localStorage)
- ✅ Responsive mobile design
- ✅ Clean, modern UI

## 🤔 FAQ

**Q: Can I use this on multiple devices?**
A: Each device stores its own data. To sync across devices, you'd need to manually export/import data (feature not currently included).

**Q: What happens if I miss a day?**
A: Your streak will break if you miss a day or complete less than 80% of your habits. Start a new streak the next day!

**Q: Can I track different habits on different days?**
A: Currently, all habits are shown every day. You can simply skip habits that don't apply on certain days.

**Q: How do I backup my data?**
A: Your data is in browser localStorage. To backup, copy the data from your browser's developer tools, or take screenshots of your habits.

**Q: Can I change XP values after creating a habit?**
A: Yes! Click "Edit" on any habit to change its name or XP value.

## 🎯 Example Habit Plans

### Morning Person Plan (60 XP total)
- Wake up at 6 AM (10 XP)
- Morning exercise (15 XP)
- Healthy breakfast (10 XP)
- Meditation (15 XP)
- Plan the day (10 XP)

### Student Plan (75 XP total)
- Study for 2 hours (30 XP)
- Complete assignments (20 XP)
- Review notes (15 XP)
- Read course material (10 XP)

### Fitness Plan (80 XP total)
- 30 min workout (20 XP)
- 10,000 steps (15 XP)
- Drink 8 glasses of water (10 XP)
- Healthy meals (20 XP)
- 8 hours sleep (15 XP)

### Productivity Plan (90 XP total)
- Deep work session (40 XP)
- Clear inbox (10 XP)
- Plan tomorrow (10 XP)
- Learn something new (20 XP)
- No social media before noon (10 XP)

## 📞 Support

This is a standalone application that runs entirely in your browser. There's no server or account system.

For issues or questions:
1. Make sure you're using a modern browser
2. Check that JavaScript is enabled
3. Try clearing your browser cache and reloading

## 📄 License

Free to use and modify for personal use.

---

**Built with ❤️ to help you build better habits, one day at a time!**

Start your habit tracking journey today! 🚀
