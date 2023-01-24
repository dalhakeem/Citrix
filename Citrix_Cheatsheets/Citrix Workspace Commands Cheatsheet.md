# Citrix Workspace Commands Cheatsheet

## PowerShell Commands

- Get list of installed Citrix Workspace App: `Get-BrokerApplication -AdminAddress <FQDN> -Credential (Get-Credential)`
- Get list of registered user devices: `Get-BrokerDevice -AdminAddress <FQDN> -Credential (Get-Credential)`
- Get list of registered user sessions: `Get-BrokerSession -AdminAddress <FQDN> -Credential (Get-Credential)`
- Get list of active user sessions: `Get-BrokerSession -AdminAddress <FQDN> -Credential (Get-Credential) -SessionState Active`
- Disconnect a user session: `Remove-BrokerSession -AdminAddress <FQDN> -Credential (Get-Credential) -SessionId <SessionId>`
- Disconnect all user sessions: `Get-BrokerSession -AdminAddress <FQDN> -Credential (Get-Credential) | Remove-BrokerSession -AdminAddress <FQDN> -Credential (Get-Credential)`
- Get list of currently active policies: `Get-BrokerPolicy -AdminAddress <FQDN> -Credential (Get-Credential)`
- Get list of currently active policies for a user: `Get-BrokerPolicy -AdminAddress <FQDN> -Credential (Get-Credential) -UserName <Username>`
- Get list of currently active policies for a device: `Get-BrokerPolicy -AdminAddress <FQDN> -Credential (Get-Credential) -DeviceName <DeviceName>`

## Command Line Tools

- Get list of installed Citrix Workspace App: `CtxBroker.exe query process`
- Get list of registered user devices: `CtxBroker.exe query device`
- Get list of registered user sessions: `CtxBroker.exe query session`
- Get list of active user sessions: `CtxBroker.exe query session /state:Active`
- Disconnect a user session: `CtxBroker.exe logoff <SessionId>`
- Disconnect all user sessions: `CtxBroker.exe logoff /server:<ServerName>`
- Get list of currently active policies: `CtxBroker.exe query policy`

