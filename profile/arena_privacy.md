# SHoNgArena Privacy Policy

**Effective date:** July 2, 2026  
**Last updated:** July 2, 2026

SHoNgArena (“SHoNgArena”, “the Bot”, “the Application”, “we”, “us”, or “our”) is a Discord community-management, entertainment, economy, gaming, and moderation-support application.

This Privacy Policy explains what Discord-related data SHoNgArena processes, why it is processed, where it may be stored, and how users can contact us regarding privacy-related requests.

---

## 1. Scope

This Privacy Policy applies only to the SHoNgArena Discord bot and its related services, including:

- The Discord bot
- Database systems
- Redis cache systems
- Internal image-generation services
- Game and economy services
- Administrative logs and monitoring tools
- Hosting infrastructure operated for SHoNgArena

By interacting with SHoNgArena in a Discord server where it is installed, you acknowledge that limited Discord-related data may be processed as described in this policy.

---

## 2. Data We Collect and Process

Depending on the features used, SHoNgArena may collect, receive, store, or process the following categories of data.

### Discord account and server data

- Discord User IDs
- Guild IDs
- Channel IDs
- Message IDs
- Usernames and display names
- Avatar URLs or profile images provided through Discord
- Role and permission information
- Guild membership information where required
- Account age
- Server membership duration
- User role context for permissions, security checks, and feature access

---

### Activity and engagement data

SHoNgArena may process limited activity-related information used for engagement, economy protection, and anti-abuse controls.

This may include:

- Message activity counts
- Text activity days
- Voice participation duration
- User level or engagement indicators
- Activity summaries over recent periods
- Account activity state
- Risk indicators related to transfers or economy features

The Application does not use message content to calculate general server-wide activity statistics. Activity summaries may be retrieved from internal database systems as pre-calculated metrics.

---

### Economy, games, and account data

SHoNgArena may store data related to economy, gaming, and account features, including:

- Points
- Currency balances
- Wallet status
- Economy balances
- Store usage
- Transfer history
- Taxes applied to transfers
- Sender and receiver IDs
- Transfer security decisions
- Risk scores
- Suspension or rejection reasons
- Manual review records
- Game statistics
- Wins and losses
- Streaks
- Removals or penalties within games
- Seasonal points
- User preferences and bot settings

User preferences may include:

- Quote settings
- Profile themes
- Temporary voice-room settings
- Trusted lists
- Blocked lists
- Wallet and economy settings

---

### Message content and feature-specific data

SHoNgArena does not generally archive all messages sent in a Discord server.

However, message content may be processed when required for specific bot features.

Examples include:

- Reading prefix commands
- Processing game answers
- Processing replies used in games
- Generating quote images from a user-selected message
- Processing whisper messages
- Supporting command-based interactions
- Generating feature-specific logs where necessary

The Application may read message content only when a feature requires it.

---

### Whisper data

SHoNgArena includes a whisper feature that may store:

- Whisper message text
- Sender Discord User ID
- Recipient Discord User ID
- Sender display name
- Delivery time
- Opening time
- Expiry status
- Related Discord message links where applicable

Whisper messages may also be referenced in administrative or operational logs where needed for abuse prevention, dispute resolution, security review, or feature operation.

---

### Images and generated content

SHoNgArena may generate images for features such as:

- User profiles
- Quotes
- Games
- Streaks
- Whispers
- Community interaction features

The Application does not currently appear to permanently store user-uploaded Discord attachments as files.

Some image-generation features may process limited data through an internal SHoNgArena service hosted on infrastructure controlled by SHoNgArena.

This may include:

- Display names
- Avatar URLs
- Whisper text
- Sender information
- Recipient information
- Game-related data
- Streak-related data

This processing is used only to generate requested Discord content.

---

## 3. How We Use Data

SHoNgArena processes Discord-related data only as necessary to operate and maintain its features.

This includes:

- Processing commands and interactions
- Running games and entertainment features
- Managing economy systems
- Managing transfers and taxes
- Detecting suspicious transfers or abuse
- Preventing fraud and manipulation
- Supporting temporary voice-room features
- Generating quotes, profiles, streaks, games, and whisper images
- Verifying user roles and permissions
- Confirming guild membership when necessary
- Maintaining user preferences
- Supporting administrative and moderation workflows
- Investigating disputes, misuse, fraud, or security incidents
- Maintaining operational logs
- Improving reliability and stability of the Application

We do not sell Discord user data.

We do not use Discord user data for advertising or unrelated marketing.

---

## 4. Privileged Gateway Intents

### Guild Members Intent

SHoNgArena uses Guild Members data when necessary to:

- Confirm that a user is currently a member of the server
- Check role and permission context
- Control access to restricted bot features
- Verify user eligibility for transfers, whispers, and account-based actions
- Support anti-abuse and transfer-risk checks
- Fetch information for specific members when needed
- Temporarily cache role-related information

SHoNgArena is not intended to retrieve or maintain a full guild member list unnecessarily.

---

### Message Content Intent

SHoNgArena uses Message Content data only for features that require access to message text.

These features include:

- Prefix commands
- Game answers
- Interactive game responses
- Quote generation from selected messages
- Whisper messages
- Command and interaction workflows

SHoNgArena does not use Message Content to perform general monitoring of all server messages.

The Application does not currently process Discord direct messages as part of its normal content-processing workflows.

The bot may send direct messages to users for notifications, links, or feature-related communication where applicable.

---

## 5. Off-Platform Storage

SHoNgArena stores limited operational data outside Discord using systems required to operate the Application.

These systems may include:

- MongoDB
- Redis
- Supabase
- Internal hosting infrastructure
- Internal image-generation services
- Sentry, where enabled
- Server logs and monitoring systems

Examples of data stored outside Discord may include:

- Discord User IDs
- Guild IDs
- Channel IDs
- Role information
- Economy balances
- Transfer records
- Activity summaries
- Game records
- User preferences
- Risk indicators
- Whisper records
- Operational logs
- Security-related records

---

## 6. Data Retention

We retain data only for as long as reasonably necessary to operate SHoNgArena, maintain the economy and gameplay systems, prevent abuse, resolve disputes, investigate incidents, and protect the integrity of the community.

Current retention behavior may include:

- Economy data, balances, gameplay records, user preferences, and transfer records may remain stored until they are no longer needed or are removed through administrative action.
- Seasonal points may remain stored until they are no longer required for the relevant feature.
- Whisper messages expire after approximately 12 hours.
- Expired whisper records may remain stored for operational, security, review, abuse-prevention, or dispute-resolution purposes until deleted.
- Redis cache data is generally temporary.
- Activity cache data may be retained for approximately 5 minutes.
- Blacklist cache data may be retained for approximately 4 hours.
- Role cache data may be retained for approximately 1 hour.
- Whisper cooldown data may be retained for approximately 5 minutes.
- Some Redis keys may remain longer depending on the feature and configured expiration settings.
- Error-monitoring and server logs may be retained according to the relevant system configuration.

Certain records may be retained longer when required for:

- Fraud prevention
- Economy integrity
- Transfer dispute resolution
- Abuse investigation
- Server rule enforcement
- Security incidents
- Operational audits
- Legal obligations

---

## 7. Data Sharing

SHoNgArena does not sell, rent, license, trade, or provide Discord user data to advertisers.

Limited data may be processed by services required to operate SHoNgArena, including:

- Discord
- MongoDB infrastructure
- Redis infrastructure
- Supabase
- Internal SHoNgArena hosting infrastructure
- Internal image-generation services
