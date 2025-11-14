# Privacy Policy for SPIDEY 🕷️

**Last Updated:** November 14, 2025

## Introduction

SPIDEY ("the Bot") is a Discord activity tracking bot that monitors and displays server member activity statistics. This Privacy Policy explains how SPIDEY collects, uses, stores, and protects your data.

By inviting SPIDEY to your Discord server or using its features, you agree to this Privacy Policy.

---

## 1. Information We Collect

### 1.1 Automatically Collected Data

SPIDEY automatically collects the following data when operating in your server:

**Server Information:**
- Server ID (unique Discord server identifier)
- Server name
- Configuration settings (roles, channels selected by admins)

**User Information:**
- User ID (unique Discord user identifier)
- Username and display name
- Role assignments (to determine tracking eligibility)
- Avatar URL (for leaderboard display)

**Activity Data:**
- Message count (number of messages sent in tracked channels)
- Voice channel time (duration spent in voice channels)
- Timestamps of activity
- Monthly and all-time statistics

### 1.2 Data NOT Collected

SPIDEY does **NOT** collect:
- ❌ Message content or text
- ❌ Direct messages (DMs)
- ❌ Private conversations
- ❌ Email addresses
- ❌ IP addresses
- ❌ Location data
- ❌ Payment information
- ❌ Data from users without tracked roles

---

## 2. How We Use Your Data

### 2.1 Primary Uses

Your data is used exclusively for:

**Activity Tracking:**
- Counting messages sent by tracked members
- Tracking voice channel participation time
- Calculating activity scores and rankings

**Leaderboard Display:**
- Showing top 10 active members in server leaderboards
- Displaying individual statistics when requested
- Comparing all-time vs monthly performance

**Server Management:**
- Allowing admins to configure tracking settings
- Enabling historical message scanning
- Providing data removal options

### 2.2 Data Processing

- All data processing occurs locally within the bot
- Data is stored in SQLite database files
- No third-party analytics or tracking services are used
- Data is not sold, shared, or transferred to external parties

---

## 3. Data Storage and Security

### 3.1 Storage Location

- **Database Type:** SQLite (local file-based database)
- **Location:** Stored on the bot hosting server
- **Isolation:** Each Discord server's data is completely isolated
- **Queries:** All database queries use `WHERE server_id = ?` to prevent data mixing

### 3.2 Security Measures

**Technical Protections:**
- Server-specific data isolation
- No cross-server data access
- Parameterized SQL queries (prevents SQL injection)
- Admin-only access to configuration commands

**Access Controls:**
- Only server administrators can configure tracking
- Only tracked role members can view their own stats
- Ephemeral responses (visible only to command user)
- Bot owner cannot access server data without permissions

### 3.3 Data Retention

**Active Servers:**
- Data is retained as long as the bot remains in your server
- Monthly data resets on the 1st of each month
- All-time data is preserved indefinitely

**Removed Servers:**
- When the bot is removed from a server, data is retained
- Server admins can manually delete all data before removal using `/remove_config`

---

## 4. Your Rights and Controls

### 4.1 Data Access

**Server Administrators Can:**
- View all configuration with `/config`
- See total statistics with `/stats`
- Check which data is being tracked

**Tracked Members Can:**
- View their own statistics with `/stats`
- See their ranking in leaderboards
- Request data deletion through server admin

### 4.2 Data Deletion

**Selective Removal:**
Server administrators can delete data using `/remove_config`:
- Remove staff tracking configuration only
- Remove all-members tracking configuration only
- Clear all activity data (keep configuration)
- Delete everything (complete removal)

**Complete Deletion:**
To completely remove all server data:
1. Run `/remove_config` in your server
2. Select "🗑️ Remove Everything"
3. All configuration and activity data will be permanently deleted

**User-Specific Deletion:**
Individual users cannot delete their own data, but can request deletion through:
- Contacting server administrators
- Removing themselves from tracked roles
- Leaving the server (future activity won't be tracked)

### 4.3 GDPR Compliance

**Right to Access:** View your data with `/stats`  
**Right to Rectification:** Data auto-updates as you use Discord  
**Right to Erasure:** Request deletion via server admin or `/remove_config`  
**Right to Restrict Processing:** Remove tracked role to stop tracking  
**Right to Data Portability:** Contact support server for data export  
**Right to Object:** Remove bot from server or leave tracked roles  

---

## 5. Data Sharing and Third Parties

### 5.1 No Data Sharing

SPIDEY does **NOT**:
- Share data with third parties
- Sell user information
- Use external analytics services
- Send data to external APIs
- Share data between Discord servers

### 5.2 Discord Platform

Data is processed through Discord's API:
- Discord's own Privacy Policy applies to platform data
- SPIDEY only accesses data Discord provides through their API
- Bot operates within Discord's Terms of Service

---

## 6. Minors and Children

- SPIDEY does not knowingly collect data from users under 13
- Discord's Terms of Service require users to be 13+ years old
- Parents/guardians should monitor their children's Discord usage
- Server administrators are responsible for their server's compliance with age restrictions

---

## 7. International Data Transfers

- Bot is hosted on servers (specify your hosting location)
- Data may be transferred internationally depending on hosting
- All data remains within bot's database (no external transfers)
- Standard data protection measures apply regardless of location

---

## 8. Changes to Privacy Policy

### 8.1 Updates

- Privacy Policy may be updated to reflect feature changes
- "Last Updated" date will be modified at the top
- Major changes will be announced in support server
- Continued use after updates constitutes acceptance

### 8.2 Notification

Users will be notified of significant privacy changes via:
- Support server announcements
- Bot status updates
- Documentation updates

---

## 9. Contact and Support

### 9.1 Questions or Concerns

For privacy-related questions:
- **Support Server:** discord.gg/owoasia
- **Help Command:** `/help_staff` in your server
- **Data Requests:** Contact via support server

### 9.2 Data Deletion Requests

To request complete data deletion:
1. Use `/remove_config` command in your server (if admin)
2. Contact support server if you need assistance
3. Provide server ID for verification

---

## 10. Legal Compliance

### 10.1 Applicable Laws

SPIDEY complies with:
- General Data Protection Regulation (GDPR)
- Discord's Developer Terms of Service
- Discord's Developer Policy
- Applicable local data protection laws

### 10.2 Data Protection Officer

For GDPR-related inquiries:
- Contact via support server: discord.gg/owoasia

---

## 11. Consent

By using SPIDEY, you consent to:
- Data collection as described in this policy
- Processing of activity data for leaderboards
- Storage of data in SQLite database
- Display of statistics in server channels

**Server Administrators** consent to:
- Tracking of members with designated roles
- Display of member activity in leaderboards
- Collection of server configuration data

**Tracked Members** consent to:
- Activity tracking (messages and voice time)
- Display in server leaderboards
- Storage of activity statistics

---

## 12. Data Breach Notification

In the unlikely event of a data breach:
- Affected servers will be notified within 72 hours
- Notification will include breach details and impact
- Remediation steps will be provided
- Regulatory authorities will be notified if required

---

## 13. Cookies and Tracking

- SPIDEY does not use cookies
- No web-based tracking mechanisms
- All tracking occurs through Discord API only
- No browser data is collected

---

## 14. Summary

**What SPIDEY Collects:**
✅ User IDs and usernames  
✅ Message counts (not content)  
✅ Voice channel time  
✅ Activity timestamps  

**What SPIDEY Does NOT Collect:**
❌ Message content  
❌ Private messages  
❌ Personal information  
❌ Data from non-tracked users  

**Your Control:**
🔒 Admins can delete all data with `/remove_config`  
🔒 Users can view their stats with `/stats`  
🔒 Complete server isolation (no data mixing)  
🔒 No third-party sharing  

---

## Contact Information

**Support Server:** discord.gg/owoasia  
**Bot Prefix:** `s!`  
**Help Command:** `/help_staff`  

---

**By using SPIDEY 🕷️, you acknowledge that you have read and understood this Privacy Policy.**

*With great data comes great responsibility!* 🕸️
