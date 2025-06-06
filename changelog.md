# QoL improvements
> - Full error handling revamp
> - Full client permission check revamp to ensure the bot has necessary server permissions to function correctly
> - Bot will now attempt to notify server owner upon required permissions being lost
> - Fun commands API request failure handlers
> - Better handling for deleted settings channels & roles to prevent broken data
> - Improved **`/help`** formatting to include system details on staff command page
> - Full **`/security-tips`** revamp to include more information and better readability
> - Staff commands now have built in permission overrides to prevent them from even loading to non-staff members (hard check still in place)
> - Improved clarify on setup instructions & added more information for frequently asked questions
> - Added clarification buttons to setting change responses and other system related messages to clarify the use of the feature
> - Added settings for optional roles to be pinged upon a vent being sent, or a new vent staff reviewal for servers with the review system enabled
> - Renamed **`/vent-approval-enable/disable`** to **`/staff-review-enable/disable`** to prevent settings confusion
> - Added attachment check to vents to determine if the file is a video, and block it if so due to bots being unable to embed videos
> - Added role position and user checks to **`/anon-ban/unban`** to ensure nobody can ban themselves, unban themselves, or ban/unban any users with higher role positions than them (hard permission check still in place)
> - Added prevention for user inputs possibly exceeding the discord character limit
> - If the vent command is ran in a channel that is not listed, if there is at least 1 server channel listed it will direct the user to that
> - Added timestamps to various server logs that will display in local user time zones


# Staff approval system changes
> - Added parameter to **`/staff-review-enable`** to optionall set a role to be pinged when a new vent is submitted for review
> - Pending approval messages will no longer expire after 30 days, and will remain usable for the duration the review channel exists, the bot is in the server, and the message is not deleted
> - Pending approval messages will now include a time stamp that will display in your local time zone
> - Bot will now pop up a message in the review channel if a pending vent message is deleted, and give the option to DM the user informing them of the cancellation
> - If the bots required permissions are revoked from the logging channel, users attempting to send a vent informing them of the issue, and instructing them to reach out to server staff
