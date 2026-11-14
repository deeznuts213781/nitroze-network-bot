# Nitroze Network Bot — Features & Hypixel API Usage

## Bot Functionality

Nitroze Network Bot is a private Discord bot developed exclusively for the Nitroze Network Discord server.

Its main features include:

- **Ticket System:** Allows users to open support, role request, and carrying service tickets.
- **Ticket Management:** Allows staff to claim, unclaim, rename, and close tickets.
- **Role Requests:** Allows users to apply for carrier roles through a ticket form.
- **Carrier Management:** Allows authorised staff to accept carriers and assign the appropriate Discord roles.
- **Carrier Logging:** Allows carriers and administrators to submit service logs using the `/log` command.
- **Ticket Transcripts:** Automatically generates HTML transcripts when tickets are closed and sends them to a designated logging channel.
- **Activity Logs:** Records relevant ticket and staff actions in designated Discord logging channels.

## Hypixel API Usage

The Hypixel API is used exclusively for Minecraft player verification during carrier role applications.

When a user opens a Role Request Ticket, they are required to provide their Minecraft IGN.

The bot retrieves the Minecraft account's UUID and queries the Hypixel Player API to check whether a Discord account is linked to that player's Hypixel profile.

To link their Discord account, the applicant must first use the `/link` command in the Hypixel lobby.

The bot then compares the Discord account linked to the Hypixel profile with the Discord account of the person submitting the role application. This helps verify that the applicant owns the Minecraft account they are applying with.

### API Usage Restrictions

- API requests are only made when a Role Request Ticket is opened and verification is required or when a user runs /userinfo.
- The API is not used for continuous player tracking.
- The bot does not perform bulk player lookups.
- The bot does not collect or store player statistics.
- The API is not provided to third parties.
- The API key is stored securely as an environment variable and is never exposed to users.

The bot is privately operated and is not publicly distributed.
