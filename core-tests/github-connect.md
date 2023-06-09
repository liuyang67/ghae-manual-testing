This document is adapted from [GHES Enterprise Connect](https://github.com/github/pe-releases/blob/master/qa/ghes-manifests/enterprise-connect/github-connect.md).
# GitHub Connect
  - Setup and configure
    - [ ] Visit `/enterprises/[enterprises_name]` and ensure there is a new 'Github Connect' item in the left-hand nav
    - [ ] Click the item and click 'Enable Github Connect' and confirm you are redirected to `https://github.com/enterprise-installation/`
    - [ ] Choose an org that you have permission on and click the 'Connect' button
    - [ ] Confirm that you are redirected to `/enterprises/[enterprises_name]/settings/dotcom_connection` and the status shows the connection is authorised
  - Search
    - [ ] Search for anything on the GHE instance, you should not be able to access any .com search results yet
    - [ ] At `/enterprises/[enterprises_name]/settings/dotcom_connection`, **Enable** the 'Users can search GitHub.com' option
    - [ ] Search for things you know exist on the instance & confirm they display on the 'Local results' tab
    - [ ] Search for things you know exist on .com and confirm they display on the 'GitHub.com results' tab
  - User contributions
    - [ ] At `/enterprises/[enterprises_name]/settings/dotcom_connection`, **Enable** the 'Users can share contribution counts to GitHub.com' option
    - [ ] As any logged in user, navigate to `/settings` and confirm you have a new 'GitHub Connect' section
    - [ ] Click it and then click on 'Connect to GitHub.com' and continue through allowing access to your account
    - [ ] Upon returning to the settings section, confirm you are now able to enable 'Send my contribution counts to GitHub.com' and click the 'Update contributions' button
    - [ ] Within 1 hour, your GHE contributions should be added to your .com account
  - Disconnect
    - [ ] Visit `/enterprises/[enterprises_name]/settings/dotcom_connection` and click 'Disable GitHub Connect'
    - [ ] Now try searching again and confirm that no results from github.com appear
