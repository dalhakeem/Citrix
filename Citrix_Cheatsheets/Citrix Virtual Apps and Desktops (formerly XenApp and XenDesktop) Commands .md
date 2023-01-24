# Citrix Virtual Apps and Desktops (formerly XenApp and XenDesktop) Commands Cheatsheet

## PowerShell Commands

- Get list of published applications: `Get-XAApplication`
- Get list of published desktops: `Get-XADesktop`
- Get list of Delivery Groups: `Get-XDDeliveryGroup`
- Get list of machines in a Delivery Group: `Get-XDDeliveryGroupMachine -DeliveryGroupName <Name>`
- Get list of sessions for a machine: `Get-XDSession -MachineName <Name>`
- Get list of users connected to a machine: `Get-XDSession -MachineName <Name> | select-object UserName`
- Get list of active sessions for a user: `Get-XDSession -UserName <Username>`
- Get list of active sessions for all users: `Get-XDSession`
- Disconnect a user session: `Stop-XDSession -SessionId <SessionId>`
- Disconnect all user sessions: `Stop-XDSession -All`
- Get list of currently active policies: `Get-XDPolicy`
- Get list of currently active policies for a user: `Get-XDPolicy -UserName <Username>`
- Get list of currently active policies for a machine: `Get-XDPolicy -MachineName <MachineName>`

## Command Line Tools

- Get list of published applications: `query process`
- Get list of published desktops: `query process /service:xd`
- Get list of active sessions: `query session`
- Disconnect a user session: `logoff <SessionId>`
- Disconnect all user sessions: `logoff /server:<ServerName>`
- Get list of currently active policies: `query policy`

