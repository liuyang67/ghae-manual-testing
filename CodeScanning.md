
# Access Policy

## Repo-level settings

### Acceptance criteria

1. Navigate to an repo's settings page (`/hostname/org_name/repo_name/setting/security_analysis`).
    - [ ] "Security & analysis" should be an option on the left navigation.
1. Click on "Security & analysis" in navigation menu.
1. Click "Set up" to set up Code scanning.
1. When "Code scanning" is set up :(example language:javascript)
    - When there are no javascript repository:
      - [ ] Enable action and create a self-runner.
      - [ ] Click "Set up" go to Code scanning alert(`/hostname/org_name/repo_name/security/code-scanning`).
      - [ ] Click "Set up this workflow"to create a CodeQL Analysis.
      - [ ] Running this workflow have error. 
    - When there are javascript repository:
      - [ ] Enable action and create a self-runner.
      - [ ] Click "Set up" go to Code scanning alert(`/hostname/org_name/repo_name/security/code-scanning`).
      - [ ] Click "Set up this workflow"to create a CodeQL Analysis.
      - [ ] Running this workflow is successfully.
      - [ ] Create a file named by .js.
      - [ ] Create a PR.
    - When The Code are no security vulnerability:
      - [ ] Check "CodeQL Analysis" is successfully.
      - [ ] Check "Code scanning results / CodeQL" is successfully.
      - [ ] Click "Code scanning results / CodeQL" Details showd "No new or fixed alerts".
      - [ ] Merage PR.
    - When The Code are security vulnerability:
      - [ ] Check "CodeQL Analysis" is successfully.
      - [ ] Check "Code scanning results / CodeQL" is error.
      - [ ] Click "Code scanning results / CodeQL" Details showd "1 new alert including 1 high/higher/Medium/any severity security vulnerability".
      - [ ] See the annotations about this alert.
      - [ ] Merage PR.
      - [ ] Navigate to the Code scanning alert page (`/hostname/org_name/repo_name/security/code-scanning`).
      - [ ] Repository's Code scanning alerts tab lists all open and closed Code scanning alerts.
      - [ ] Show all alerts are listed,they can be sorted alphanumerically or by newest/oldest.
      - [ ] Click the security vulnerability alert.
      - [ ] Review the alert, then click Dismiss and choose a reason for closing the alert.
    - Define which alert severity should cause a pull request check to fail.
      - [ ] If the security vulnerability are not you chose Security level.
       - [ ] Check "CodeQL Analysis" is successfully.
       - [ ] Check "Code scanning results / CodeQL" is successfully.
       - [ ] Click "Code scanning results / CodeQL" Details showd "No new or fixed alerts".
       - [ ] Merage PR.
      - [ ] If the security vulnerability are you chose Security level.
       - [ ] Check "CodeQL Analysis" is successfully.
       - [ ] Check "Code scanning results / CodeQL" is error.
       - [ ] Click "Code scanning results / CodeQL" Details showd "1 new alert including 1 high/higher/Medium/any severity security vulnerability".
       - [ ] See the annotations about this alert.
       - [ ] Merage PR.
       - [ ] Navigate to the Code scanning alert page (`/hostname/org_name/repo_name/security/code-scanning`).
       - [ ] Repository's Code scanning alerts tab lists all open and closed Code scanning alerts.
       - [ ] Show all alerts are listed,they can be sorted alphanumerically or by newest/oldest.
       - [ ] Click the security vulnerability alert.
       - [ ] Review the alert, then click Dismiss and choose a reason for closing the alert.
      

      
