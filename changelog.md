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


