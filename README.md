🕷️ **SPIDEY - Advanced Activity Tracking Bot**

With great staff comes great responsibility! SPIDEY is a powerful Discord bot designed to track and monitor staff and member activity across your server with real-time leaderboards, comprehensive statistics, and automated monthly reports.

**✨ KEY FEATURES**

📊 **Dual Tracking System**
• Staff Activity Tracking - Monitor your team's performance
• All Members Tracking - Track entire server engagement
• Separate leaderboards for each group
• Role-based permissions and visibility

📈 **Real-Time Leaderboards**
• All-Time leaderboards (lifetime stats)
• Monthly leaderboards (auto-resets each month)
• Live updates with every message and voice session
• Beautiful embed designs with rankings and stats

🎤 **Comprehensive Tracking**
• Message counts per user
• Voice channel time tracking
• Automatic session management
• Join/leave detection with accuracy

🗓️ **Monthly Statistics**
• Automatic monthly resets
• Historical data preservation
• Compare performance month-over-month
• Track trends and growth

⚙️ **Easy Setup & Management**
• Interactive setup with dropdown menus
• Real-time configuration preview
• Flexible role and channel assignment
• Selective data removal options

🌍 **Multi-Server Support**
• Complete server isolation
• Independent configurations per server
• Separate databases per server
• No data mixing or conflicts

**🎯 COMMANDS**

**Setup Commands (Admin Only):**
• `/setup` - Interactive configuration with live preview
• `/config` - View current server settings
• `/remove_config` - Selectively remove tracking or data
• `/scan` - Scan historical messages for catch-up

**User Commands:**
• `/stats [member]` - View detailed activity statistics
• `/help_staff` - Display all available commands

**📊 PERFECT FOR**
• Gaming communities tracking moderator activity
• Content servers monitoring staff engagement
• Community servers measuring member participation
• Team servers analyzing collaboration metrics
• Any server wanting detailed activity insights

**🔒 PRIVACY & SECURITY**
• Server-isolated data storage
• Admin-only configuration access
• Ephemeral command responses
• No data sharing between servers
• Complete control over your data

**🌟 TECHNICAL HIGHLIGHTS**
• Built with discord.py 2.6.4
• Hybrid commands (slash & prefix)
• SQLite database for reliability
• Asia/Dhaka timezone support
• Background task automation
• Optimized performance

**💡 USE CASES**
• Track staff performance and accountability
• Measure community engagement levels
• Identify active vs inactive members
• Reward top contributors monthly
• Analyze voice channel usage patterns
• Monitor team communication trends

**🚀 GETTING STARTED**
1. Invite SPIDEY to your server
2. Run `/setup` to configure tracking
3. Select staff role and leaderboard channels
4. Watch real-time updates automatically!

**📞 SUPPORT**
Join our support server: discord.gg/owoasia
Use `/help_staff` in your server for command reference

With great staff comes great responsibility - let SPIDEY help you track it! 🕷️
```

---

## 🔐 Required Bot Permissions

### **Permission Integer:** `277025770560`

### **Individual Permissions Needed:**

#### **Text Permissions:**
- ✅ **View Channels** - To see channels and read configurations
- ✅ **Send Messages** - To send leaderboard updates and responses
- ✅ **Embed Links** - To display beautiful leaderboard embeds
- ✅ **Read Message History** - For `/scan` command to analyze past messages
- ✅ **Use External Emojis** - For displaying rankings and decorations
- ✅ **Add Reactions** - For interactive features (optional)

#### **Voice Permissions:**
- ✅ **View Channels** - To see voice channels
- ✅ **Connect** - To track when members join voice channels

#### **General Permissions:**
- ✅ **Manage Roles** - For potential role-based features (if extended)

### **Minimal Permissions (Core Functionality):**
```
Permission Integer: 277025770496

- View Channels
- Send Messages
- Embed Links
- Read Message History
- Connect (Voice)
```

---

## 🔧 Required Privileged Gateway Intents

### **In Discord Developer Portal → Bot Settings:**

#### ✅ **PRESENCE INTENT** (Required)
- Tracks online/offline status
- Monitors member presence changes
- Used for activity accuracy

#### ✅ **SERVER MEMBERS INTENT** (Required)
- Access to member list
- Track member joins/leaves
- Essential for voice tracking

#### ✅ **MESSAGE CONTENT INTENT** (Required)
- Read message content
- Count messages from staff
- Track activity in real-time

---

## 📊 Bot Settings Configuration

### **OAuth2 URL Generator Settings:**

**Scopes:**
- ✅ `bot`
- ✅ `applications.commands`

**Bot Permissions:**
```
View Channels
Send Messages
Embed Links
Read Message History
Connect
```
