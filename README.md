# SPIDEY 🕷️ - Advanced Discord Activity Tracker

> **With great staff comes great responsibility... to track their activity!**

SPIDEY is a comprehensive Discord bot designed to monitor, analyze, and celebrate staff and member activity across your server. Built with discord.py 2.6.4, SPIDEY provides real-time leaderboards, detailed statistics, and automated monthly reports to help you understand and recognize your community's most active contributors.

---

## 🌟 Overview

SPIDEY transforms server activity tracking into an engaging, transparent, and rewarding experience. Whether you're managing a gaming community, content server, or professional team, SPIDEY gives you the insights you need to recognize top performers, measure engagement, and maintain accountability.

### Why SPIDEY?

- **📊 Dual Tracking System** - Separate tracking for staff members and all server members
- **🏆 Real-Time Leaderboards** - Auto-updating embeds with top 10 rankings
- **📅 Monthly Analytics** - Automatic monthly resets with historical data preservation
- **🎤 Voice Monitoring** - Accurate voice channel time tracking down to the minute
- **💬 Message Counting** - Comprehensive message activity across all channels
- **🌍 Multi-Server Support** - Perfect server isolation with independent configurations
- **⚡ Interactive Setup** - Easy configuration with dropdown menus and live previews
- **🔒 Privacy-First** - Complete data control with selective removal options

---

## ✨ Key Features

### **1. Comprehensive Activity Tracking**

**Message Tracking:**
- Counts every message sent by tracked members
- Real-time updates across all text channels
- Excludes bot messages for accuracy
- Historical message scanning with `/scan` command

**Voice Channel Monitoring:**
- Tracks join/leave times with millisecond precision
- Automatic session management (even during bot restarts)
- Calculates total voice time in minutes
- Handles multiple voice channels simultaneously

**Activity Scoring:**
- Combined score based on messages and voice time
- Fair ranking system that values both text and voice engagement
- Prevents gaming the system with balanced metrics

### **2. Real-Time Leaderboards**

**All-Time Leaderboards:**
- Lifetime statistics for staff and all members
- Top 10 rankings with detailed breakdowns
- Updates automatically every 60 seconds
- Beautiful embeds with emoji rankings (🥇🥈🥉)

**Monthly Leaderboards:**
- Automatic reset on the 1st of each month
- Track performance month-over-month
- Compare current month vs all-time stats
- Historical data preserved for analysis

**Leaderboard Features:**
- User avatars and display names
- Message counts and voice time
- Combined activity scores
- Timestamp of last update
- Supports both staff-only and all-members tracking

### **3. Detailed Statistics**

**Individual Stats (`/stats`):**
- Personal ranking position
- Total messages sent
- Total voice channel time
- Activity score breakdown
- Month-to-date performance
- All-time vs monthly comparison

**Server Stats:**
- Total tracked members
- Combined message counts
- Total voice minutes
- Server-wide engagement metrics

### **4. Easy Setup & Configuration**

**Interactive Setup (`/setup`):**
- Step-by-step configuration with dropdown menus
- Real-time preview of settings
- Select staff role from list
- Choose leaderboard channels
- Configure all-members tracking separately
- Live embed updates showing your selections

**Configuration Management:**
- View current settings with `/config`
- Selective removal options with `/remove_config`:
  - Remove staff tracking only
  - Remove all-members tracking only
  - Clear activity data (keep config)
  - Delete everything
- Cancel button for safety

### **5. Multi-Server Support**

**Perfect Server Isolation:**
- Each server has completely separate data
- Independent configurations per server
- No data mixing or cross-server leaks
- Scalable to unlimited servers

**Server-Specific Features:**
- Different staff roles per server
- Separate leaderboard channels
- Independent tracking settings
- Isolated database queries with `WHERE server_id = ?`

### **6. Advanced Functionality**

**Historical Scanning:**
- Scan past messages with `/scan <days>`
- Catch up on activity before bot joined
- Progress tracking during scan
- Respects role assignments (only counts current staff)

**Voice Session Recovery:**
- Tracks members already in voice when bot starts
- Resumes sessions after bot restarts
- No data loss from disconnections

**Monthly Auto-Reset:**
- Checks monthly tables on bot startup
- Automatically creates new month if needed
- Preserves all-time data while resetting monthly stats

**Background Tasks:**
- Leaderboard updates every 60 seconds
- Voice session monitoring
- Monthly table maintenance
- Automatic presence updates

---

## 🎯 Perfect For

- **Gaming Communities** - Track moderator and admin activity
- **Content Servers** - Measure creator and staff engagement
- **Community Servers** - Analyze member participation levels
- **Team Workspaces** - Monitor collaboration and communication
- **Support Servers** - Measure helper activity and response times
- **Educational Servers** - Track student and teacher engagement
- **NFT/Crypto Communities** - Monitor team and member activity
- **Esports Organizations** - Analyze team communication patterns

---

## 🚀 Getting Started

### **1. Invite SPIDEY**
Use the OAuth2 URL with required permissions:
- View Channels
- Send Messages
- Embed Links
- Read Message History
- Connect (for voice tracking)

### **2. Enable Required Intents**
In Discord Developer Portal → Bot Settings:
- ✅ Presence Intent
- ✅ Server Members Intent
- ✅ Message Content Intent

### **3. Configure Your Server**
Run `/setup` and follow the interactive configuration:
1. Select staff role from dropdown
2. Choose staff all-time leaderboard channel
3. Choose staff monthly leaderboard channel
4. *Optional:* Configure all-members tracking
5. Watch live preview update as you select

### **4. Optional: Scan History**
Run `/scan 30` to analyze last 30 days of messages

### **5. Enjoy!**
SPIDEY automatically tracks activity and updates leaderboards every 60 seconds

---

## 🎮 Commands

### **Admin Commands** (Server Owner/Admin Only)

| Command | Alias | Description |
|---------|-------|-------------|
| `/setup` | `/s` | Interactive setup with dropdown menus |
| `/config` | `/c` | View current server configuration |
| `/remove_config` | `/rc` | Selectively remove tracking or data |
| `/scan <days>` | `/sc` | Scan historical messages (max 365 days) |

### **User Commands** (Staff Members)

| Command | Alias | Description |
|---------|-------|-------------|
| `/stats [member]` | `/st` | View activity statistics (defaults to yourself) |
| `/help_staff` | `/hs` | Display all available commands with aliases |

### **Prefix Commands**
All slash commands also work with `s!` prefix:
- `s!setup`, `s!config`, `s!stats`, etc.

---

## 🔒 Privacy & Security

### **Data Collection**
- Only tracks messages and voice time from public server channels
- Only tracks users with designated staff or all-members roles
- No DMs or private messages are monitored
- No personal information beyond Discord username and ID

### **Data Storage**
- SQLite database (local, not cloud)
- Server-isolated data with `WHERE server_id = ?` on all queries
- No data sharing between servers
- Complete data ownership by server admins

### **Data Control**
- Server admins can view all tracked data with `/config`
- Selective removal with `/remove_config`:
  - Remove specific tracking types
  - Clear activity data
  - Delete everything
- GDPR compliant with full data deletion capability

### **Security Features**
- Admin-only access to configuration commands
- Ephemeral responses (only visible to command user)
- Bot owner cannot access server data without permissions
- No API endpoints or external data access

---

## 🛠️ Technical Details

### **Technology Stack**
- **Language:** Python 3.8+
- **Library:** discord.py 2.6.4
- **Database:** SQLite3 with WAL mode
- **Commands:** Hybrid (slash + prefix support)
- **Architecture:** Event-driven with background tasks

### **Database Schema**
- `server_config` - Server configurations
- `staff_activity` - Staff all-time stats
- `all_members_activity` - All-members all-time stats
- `staff_monthly_activity` - Staff monthly stats
- `all_members_monthly_activity` - All-members monthly stats
- `voice_sessions` - Active voice session tracking

### **Performance**
- Optimized SQL queries with indexed columns
- Background task scheduling for updates
- Efficient memory usage with session cleanup
- Rate limit handling built-in

### **Timezone**
- All timestamps in Asia/Dhaka timezone (GMT+6)
- Configurable in code if needed

---

## 📊 Use Cases & Examples

### **Example 1: Gaming Community**
Track moderator activity to:
- Reward most active staff monthly
- Identify inactive moderators
- Measure response times in support channels
- Recognize top contributors with special roles

### **Example 2: Content Server**
Monitor creator engagement:
- Track time spent in voice creation sessions
- Count messages in collaboration channels
- Monthly competitions with prizes
- Leaderboard showcased in announcements

### **Example 3: Professional Team**
Analyze team collaboration:
- Measure communication frequency
- Track meeting attendance (voice time)
- Monthly performance reviews
- Identify top performers for promotions

---

## 🎨 Customization

### **Embeds**
Beautiful, colorful Discord embeds with:
- Server branding integration
- Emoji decorations (🥇🥈🥉 for top 3)
- Real-time timestamps
- User avatars
- Color-coded ranks

### **Configurable Options** (in code)
- Timezone (default: Asia/Dhaka)
- Update interval (default: 60 seconds)
- Leaderboard size (default: top 10)
- Bot prefix (default: `s!`)
- Bot owner ID for special permissions

---

## 🐛 Troubleshooting

### **Leaderboard not updating?**
- Check bot has "Send Messages" and "Embed Links" permissions
- Verify leaderboard channel is set with `/config`
- Ensure staff role is configured

### **Voice tracking not working?**
- Bot needs "View Channels" and "Connect" permissions
- Member must have staff/all-members role
- Check voice channel permissions

### **Messages not counting?**
- Verify user has the tracked role
- Check bot can see the channel
- Bot messages are excluded

### **Commands not appearing?**
- Run `/help_staff` to see all commands
- Wait up to 1 hour for Discord to sync slash commands
- Check bot has "Use Application Commands" permission

---

## 🔄 Updates & Roadmap

### **Current Version Features**
- ✅ Dual tracking system (staff + all members)
- ✅ Real-time leaderboards (all-time + monthly)
- ✅ Voice channel tracking
- ✅ Historical message scanning
- ✅ Interactive setup with dropdowns
- ✅ Selective data removal
- ✅ Multi-server support

### **Planned Features** (Community Requested)
- 📅 Weekly leaderboards
- 📈 Data export (CSV/JSON)
- 🎯 Custom activity goals
- 🏅 Achievement system
- 📊 Web dashboard
- 🔔 Activity alerts
- 📸 Leaderboard image generation

---

## 📞 Support & Community

- **Support Server:** discord.gg/owoasia
- **Help Command:** `/help_staff` (shows all commands)
- **Bug Reports:** Contact via support server
- **Feature Requests:** Submit in support server

---

## 📝 License

This project is provided as-is for Discord communities. Modify and adapt as needed for your server's requirements.

---

## 🙏 Credits

**Made with ❤️ for Discord communities worldwide!**

Built using:
- discord.py - Discord API wrapper
- SQLite - Lightweight database
- Python - Programming language

---

## 🕷️ About SPIDEY

Like a spider spinning its web, SPIDEY weaves together all your server activity data into a comprehensive picture. It watches over your community quietly but effectively, tracking every contribution your members make.

Just as Spider-Man protects his community, SPIDEY helps you recognize and celebrate the people who protect and support your Discord server.

**With great staff comes great responsibility... to track their activity!** 🕸️

---

**SPIDEY 🕷️ - Your friendly neighborhood activity tracker!**

*Empowering Discord communities with transparent, engaging activity tracking since 2025.*
