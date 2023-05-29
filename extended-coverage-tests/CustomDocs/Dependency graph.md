# Access Policy
## Acceptance criteria

1. Navigate to the repo Insights page (`/hostname/username/repo_name/pulse`).
1. Click on "Dependency graph"(also check it on `/hostname/username/repo_name/network/dependencies`).
1. When there are no Dependency repos:
    - [ ] "No manifest files found To enable the dependency graph, your repository must define dependencies in one of the supported manifest file types, like package.json or Gemfile." message is displayed.
1.  When there are Dependency repo:
    - [ ] When there are no security vulnerability in  dependencies:
        - [ ] Show all dependencies in manifest files.
    - [ ] When there are security vulnerability in  dependencies:
        - [ ] Show all dependencies in manifest files.
        - [ ] "We found a potential security vulnerability in one of your dependencies" is displayed.
        - [ ] Click on "View Dependabot alerts" to view the Dependabot alerts(`/hostname/username/repo_name/security/dependabot`).    
1. Click on "Dependency alerts"(`/hostname/username/repo_name/security/dependabot`).
1. When "Dependency alerts" is disbale:
    - [ ] "Dependabot alerts are disabled.To receive Dependabot alerts, you must first enable Dependabot alerts in this repository’s settings." is displayed.
    - [ ] Go to "[hostname]/enterprises/github/settings/dotcom_connection" page to "Enable github connect".
    - [ ] Click "Connect" to connect with server.
    - [ ] Select "Eanble with notifications" or "Eanble with no notifications" for "Dependabot",then "Confirm change",check the "Dependabot alerts" status is enabled in `[repo-name]/settings/security_analysis`. 
1. When "Dependency alerts" is enable:
    - [ ] When there are no security vulnerability:
      - [ ] "Welcome to Dependabot alerts! Dependabot alerts track security vulnerabilities that apply to your repos".
    - [ ] When there are security vulnerability:
      - [ ] Repository's Dependabot alerts tab lists all open and closed Dependabot alerts.
      - [ ] Show all alerts are listed,they can be sorted alphanumerically or by newest/oldest.
 1. Dissmissing Dependabot alerts
    - [ ] Select the "Dismiss all" dropdown,and click a reason for dissmissing the alert.
    - [ ] Click "Manage repository vulnerability setting" to view the vulnerability setting at "/hostname/username/repo_name/settings/security_analysis".
    - [ ] Click "Manage account notification setting" to view the notification setting at "/hostname/settings/notifications".
