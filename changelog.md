# QoL improvements
> - Full error handling revamp
> - Full client permission check revamp to ensure the bot has necessary server permissions to function correctly
> - Bot will now attempt to notify server owner upon required permissions being lost
> - Upon any database error following the bot getting added to a server, it will attempt to DM the server owner informing them of the error, steps to fix it, and where to reach out for help
> - Fun commands API request failure handlers
> - Better handling for deleted settings channels & roles to prevent broken data
> - Improved **`/help`** formatting to include system details on staff command page, including what settings are enabled/disabled by default 
> - Full **`/security-tips`** revamp to include more information and better readability
> - Staff commands now have built in permission overrides to prevent them from even loading to non-staff members (hard check still in place)
> - Improved clarity on setup instructions & added more information for frequently asked questions
> - Added clarification buttons to setting change responses and other system related messages to clarify the use of the feature
> - Added settings for optional roles to be pinged upon a vent being sent, or a new vent pending staff reviewal for servers with the review system enabled
> - Renamed **`/vent-approval-enable/disable`** to **`/staff-review-enable/disable`** to prevent settings confusion
> - Added role position and user checks to **`/anon-ban/unban`** to ensure nobody can ban themselves, unban themselves, or ban/unban any users with higher role positions than them (hard permission check still in place)
> - Added prevention for user inputs possibly exceeding the discord character limit
> - If the vent command is ran in a channel that is not listed, if there is at least 1 server channel listed it will direct the user to that
> - Added timestamps to various server logs, and all vent embeds that will display in user local time zones


# Main vent feature changes
> - The bot will now detect spoiler markdown (||) in vent content, and automatically add a trigger warning to the vent if the server is not using the staff review system and it may be triggering content
> - Added member permission checks for vents with attached images, the bot will no longer allow members to attach images with their vents if the venting channels built in permission overrides deny that member media perms, so it cannot be bypassed
> - Vents will now automatically be permitted to be sent in any threads of listed channels, allowing many more permitted venting channels if needed
> - Added built in discrimination filtering to automatically catch and block any common slurs from being sent in vent content, along with moderate bypass detection (this does not use AI)
> - Added detection and automatic blocking for attempted **@everyone** and **@here** pings. Though mentions in embeds don't work, attempting it will now be blocked
> - Added attachment check to vents to determine if the file is a video, and block it if so due to bots being unable to embed videos
> - Added vent reply notification, when a server member replies to your vent, the bot will DM you informing you who replied and where. These can be disabled with **`/vent-dm-disable`**, the same command to disable vent confirmation DMs
> - Added setting commands to optionally set a role to be pinged when a vent is sent, **'/vent-ping-enable/disable'**. This role cannot be set as **@everyone** or **@here**

# Staff approval system changes
> - Added parameter to **`/staff-review-enable`** to optionaly set a role to be pinged when a new vent is submitted for review
> - Pending approval messages will no longer expire after 30 days, and will remain usable for the duration the review channel exists, the bot is in the server, and the message is not deleted
> - Pending approval messages will now include a time stamp that will display in your local time zone
> - Bot will now pop up a message in the review channel if a pending vent message is deleted, and give the option to DM the author informing them of the cancellation
> - If the bots required permissions are revoked from the logging channel, users attempting to send a vent will receive a message informing them of the issue, and instructing them to reach out to server staff
> - If the bots required permissions are revoked from the venting channel while the vent is pending review, the "Approve" button will now properly address the error
