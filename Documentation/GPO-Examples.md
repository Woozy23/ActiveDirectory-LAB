# Group Policy Objects Applied


## Restrict Control Panel
- Path: User Configuration - Policies - Administrative Templates - Control Panel
- Setting: Prohibit access to Control Panel = Enabled
- Applied to: OU = TestUsers

## Password Policy
- Path: Computer configuration - Windows Settings - Security Settings - Account Policies
- Setting: Minimum password length = 8
- Applied to: Domain level

## End Session Timeout
- Path: Computer Configuration - Windows Settings - Security Settings - Local P{olicies - Security Options
- Setting: Interactive Logon: Machine inactivity limit = 15 minutes
- Applied to: All domain users

## Remove Specific Desktop Icons
- Path: User Configuration - Administrative Templates - Desktop
- Setting: Hide and disable all items on the desktop = Enabled
- Applied to: Helpdesk OU

## Add Microsoft Outlook to Startup
- Path: User Configuration -  Administrative Templates - System - Logon
- Setting: Run these programs at user logon - Outlook.exe
- Applied to: Sales OU

## Enable Pop-up Blocker
- Path: User Configuration - Administrative Templates - Windows Components - Internet Explorer - Privacy
- Setting: Turn on Pop-up Blocker = Enabled
- Applied to: Marketing OU

## Prevent Deleting Browser History
- Path: User Configuration - Administrative Templates - Windows Components - Internet Explorer - Delete Browsing History
- Setting: Disable "Delete browsing history" = Enabled
- Applied to: All domain users

## Restrict Command Prompt
- Path: User Configuration - Administrative Templates - System
- Setting: Prevent access to the command prompt = Enabled
- Applied to: Students OU

## Screen Saver Timeout
- Path: User Configuration - Administrative Templates - Control Panel - Personalization
- Setting: Screen saver timeout = 900 seconds(15 minutes)
- Applied to: All domain computers
