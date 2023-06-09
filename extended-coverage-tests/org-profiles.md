Org profile (`http(s)://[hostname]/[org name]`)
  - When signed in as an owner
    - [ ] Private repos are displayed with the 'Private' label
    - [ ] Filter repos by Public, Private, Sources and Forks
    - [ ] The settings *gear* icon is present and goes to `http(s)://[hostname]/organizations/[org name]/settings/profile`
    - [ ] The *+ New Repository* button is present and goes to `http(s)://[hostname]/organizations/[org name]/repositories/new`
    - People box
      - [ ] Users can be selected to view their org permissions
      - [ ] Clicking *People* goes to `http(s)://[hostname]/orgs/[org name]/people`
      - [ ] *Add member* button goes to `http(s)://[hostname]/orgs/[org name]/invitations/new`
      - The 'People' page (`http(s)://[hostname]/orgs/[org name]/people`)
        - 'Outside collaborators' tab
          - [ ] Outside collaborators are listed
          - [ ] Click on an outside collaborators username to manage their access
          - [ ] Clicking *Invite to organization* goes to `http(s)://[hostname]/organizations/[org name]/invitations/[user]/edit`
        - 'Members' tab
          - [ ] Filter for a member
          - [ ] People without 2FA enabled are denoted by the red 'warning' triangle
          - [ ] The number of teams a person is on is listed and can be clicked on to view all the teams
          - [ ] The person listed that you are signed in as has a dropdown menu to switch their organization visibility between public and private
          - [ ] Click the *Add member* button to `http(s)://[hostname]/orgs/[org name]/invitations/new`
          - [ ] Remove a person from a team by selecting them and clicking the *Remove from organization* button
          - [ ] Demote a member that is also collaborating on a repo to just an outside collaborator by selecting them and clicking the *Convert to outside collaborator* button
      - Invite a new member to an org (`http(s)://[hostname]/orgs/[org name]/invitations/new`)
        - Search for a user
          - [ ] Already added users are greyed-out
          - [ ] A new user can be found and selecting them goes to `http(s)://[hostname]/orgs/[org name]/invitations/[user]/edit`
          - 'Invite [user] to [org]' page (`http(s)://[hostname]/orgs/[org name]/invitations/[user]/edit`)
            - [ ] Invite a user to be a member
            - [ ] Invite a user to be an owner
            - [ ] Multiple teams can be selected and clicking *Add member* adds them to the teams
    - The 'Teams' page (`http(s)://[hostname]/orgs/[org name]/teams`)
      - [ ] Filter for a team
      - [ ] Clicking the *My teams* button filters with your username
      - [ ] Clicking the *+ New team* button goes to `http(s)://[hostname]/orgs/[org name]/new-team`
      - Click on a team name to go to its individual team page (eg. `http(s)://[hostname]/orgs/[org name]/teams/[team name]`)
      - A team that you belong to
        - [ ] Leave a team by clicking the *Leave* button
      - A team you are yet to join
        - [ ] Teams you are yet to join are still listed
        - [ ] Click the *Join* button to join the team
      - Clicking the *Add members* button on a team that has no members goes to its individual team page
      - An individual team page (`http(s)://[hostname]/orgs/[org name]/team/[team name]`)
        - The *Team members* tab/list
          - [ ] Clicking on a user goes to their org permissions
          - [ ] Add an owner using the 'Add a person' filter
          - *Gear* icon drop down menu
            - [ ] Convert a user to an outside collaborator
            - [ ] Remove from the team
        - The *Repositories* tab/list
            - [ ] Add a repo using the filter
            - [ ] Remove a repo from the Repositories list by clicking the *Remove* button
            - Permission level dropdown
              - [ ] When set to 'Admin' there is no inline help text
              - [ ] When set to 'Write' or 'Read', clicking on *View details* opens a modal that displays which team members have greater access
        - The team name box
          - [ ] Edit a team name's description
          - [ ] Click the *Leave* button to leave the team
          - [ ] The *Settings* button goes to `http(s)://[hostname]/orgs/[org name]/teams/owners/edit`
        - Editing a team (`http(s)://[hostname]/orgs/[org name]/teams/[team name]/edit`)
          - [ ] The team name can be updated
          - [ ] The description can be updated
          - [ ] The secrecy level can be altered
          - [ ] Delete a team
    - Audit log (`http(s)://[hostname]/organizations/[org name]/settings/audit-log`)
      - Recent events list
        - [ ] The avatar of an invited user is nested in the corner of the avatar of the person who invited them
        - [ ] Country names are listed
        - [ ] The time when the event was created is listed
      - Search
        - [ ] Select an event query to filter by it
        - [ ] Click *X Clear current search* to clear the filter
  - When signed in as a non-owner member (`http(s)://[hostname]/[org name]/`)
    - [ ] The settings *gear* icon is not present
    - [ ] When 'Allow members to create repositories for this organization' (`http(s)://[hostname]/organizations/[org name]/settings/member_privileges`) is enabled, the *+ New Repository* button is present, when disabled the button disappears
    - People box
      - [ ] The *Add someone* button is not present
      - The 'People' page (`http(s)://[hostname]/orgs/[org name]/people`)
        - [ ] The 2FA indicator is not present
        - [ ] The *Add member* button is not present
        - [ ] The *Members | Outside collaborators'* switcher is not present
        - [ ] The *Manage access* text link is not present
    - When a member is a team maintainer  (`http(s)://[hostname]/orgs/[org name]/teams/[team name]`)
      - The *Team members* tab
        - [ ] 'Team maintainer' label is shown
        - [ ] Remove a member using the *Gear* icon dropdown
        - [ ] Demote a team maintainer using the *Gear* icon dropdown
      - The *Repositories* tab
        - [ ] Remove a repo from the Repositories list by clicking the *Remove* button
        - [ ] Switching the permission level dropdown to 'Read' or 'Write' does not display the 'Some members have greater privileges. *View details*' text link
      - The team name box
        - [ ] Non-team maintainers cannot edit the description
        - [ ] The *Settings* button is not displayed for non-team maintainers
    - [ ] When there are no team maintainers or owners on a team the "Add some team maintainers" banner is presented
    - [ ] A team maintainer can add an org member to a team that they maintain
  - When completely signed out
    - [ ] Private repos are not displayed
    - [ ] *This organization has no public repositories* warning is shown If there are no public repos
    - [ ] The settings *gear* icon is not present
    - [ ] The *+ New Repository* button is not present
    - People box
      - [ ] 'This organization has no public members.' warning is shown when there are no public members
      - [ ] Public members are listed when there are public members
      - The 'People' page when there are public members (`http(s)://[hostname]/orgs/[org name]/people`)
        - [ ] The only info listed for a member is their username, avatar and a *Follow* button
    - [ ] The 'Teams' box is not displayed
