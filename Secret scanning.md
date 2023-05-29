
      
  ## Secret scanning
  
  ### Acceptance criteria
  
  #### Workflow for creating secret scan using default settings
1. New Custom patterns in 3 levels
      - enterprise-level
          -  Navigate to the enterprise settings page `(/hostname/enterprises/codescanner)' .
          - [ ] Click on "policies" on the left side of the page，then Click the " advanced security" tab.
          - [ ] Under the Organization Permissions，Make sure Base permissions is allowed for all organizations（default）.
          - [ ] Click "Security features".
          - [ ] Click on the green "New Custom patterns".
          - [ ] Fill in the "Custom pattern name", the name format Bunch cannot be Chinese.
          - [ ] Fill in the "Secret format", which is required to comply with the example_[A-Za-z0-9]{40} rule, such as octocat_token_[a-zA-Z0-9]{15}.
          - [ ] Click  more options， it will show before Before secret and After secret, Clicking less options and it becomes more options again.
          - [ ] Fill in the password format that can match the rule in "Test string", such as octocat_token_123456789qwerty.
          - [ ] Click create Custom pattern.
             
      - Org-level
          -  Create an organization, Navigate to the org settings page `(/hostname/org/settings/profile)'
          - [ ] Click the "security_analysis" tab on the left side of the page.
          - [ ] Check Automatically enable new repositories and Automatically enable repositories added to Advanced Security.
          - [ ] Click on the green "New Custom patterns".
          - [ ] Fill in the "Custom pattern name", the name format Bunch cannot be Chinese.
          - [ ] Fill in the "Secret format", which is required to comply with the example_[A-Za-z0-9]{40} rule, such as octocat_token_[a-zA-Z0-9]{15}.
          - [ ] Click  more options， it will show before Before secret and After secret, Clicking again will stack up and show less options.
          - [ ] Fill in the password format that can match the rule in "Test string", such as octocat_token_123456789qwerty.
          - [ ] Click create Custom pattern.
          
      - Repo-level
          - Create a repo under an organization,Navigate to the repo settings page `(/hostname/org/repo_name/settings/)'.
          - [ ] Click the "security_analysis" tab on the left side of the page.
          - [ ] Enable "GitHub Advanced Security", pops up the Enable GitHub Advanced Security for this repository? 
          - [ ] Clicking "Enable GitHub Advanced Security for this repository".
          - [ ] Enable the Secret scanning.
          - [ ] Click on the green "New Custom patterns".
          - [ ] Fill in the "Custom pattern name", the name format Bunch cannot be Chinese.
          - [ ] Fill in the "Secret format", which is required to comply with the example_[A-Za-z0-9]{40} rule, such as octocat_token_[a-zA-Z0-9]{15}.
          - [ ] Click  more options， it will show before Before secret and After secret, Clicking again will stack up and show less options.
          - [ ] Fill in the password format that can match the rule in "Test string", such as octocat_token_123456789qwerty.
          - [ ] Click create Custom pattern.
      
                   
        
  2. Create a PR to add files that contain the pattern secret created by above all.
      - [ ] Navigate to the repo settings page `(/hostname/org/repo_name/settings/)'.
      - [ ] Click code, then create a new file, edit a file, and modify the content to include the password format .
      - [ ] Select Create a new branch for this commit and start a pull request, then Commit new file.
      - [ ] Click pull request.
  
  3. View secret scanning alerts
     - Navigate to the repo settings page `(/hostname/org/repo_name/security/secret-scanning)'.
         - [ ] Secret "scanning alerts" is on the left side of the page.
         - [ ] Click the "secret scanning alerts", at least three levels an alert will appear on the list.
         - [ ] On the right side of the alrets list, click Filter and sort to test the filter function.
         
#### Workflow for creating secret scan using allowed for selected  organization. 
#### Uncheck any organization or an organization unrelated to secret scan.
      - enterprise-level
          -  Navigate to the enterprise settings page `(/hostname/enterprises/codescanner)' .
          - [ ] Click on "policies" on the left side of the page，then Click the " advanced security" tab.
          
          - [ ] Under the Organization Permissions，
          - [ ] Make sure Base permissions is allowed for selected  organization，Uncheck any organization or an organization unrelated to secret scan
          - [ ] Click "Security features".
          - [ ] Click on the green "New Custom patterns".
          - [ ] Fill in the "Custom pattern name", the name format Bunch cannot be Chinese.
          - [ ] Fill in the "Secret format", which is required to comply with the example_[A-Za-z0-9]{40} rule, such as octocat_token_[a-zA-Z0-9]{15}.
          - [ ] Click  more options， it will show before Before secret and After secret, Clicking less options and it becomes more options again.
          - [ ] Fill in the password format that can match the rule in "Test string", such as octocat_token_123456789qwerty.
          - [ ] Click create Custom pattern.
          
     - Org-level
          -  Create an organization, Navigate to the org settings page `(/hostname/org/settings/profile)'
          - [ ] Click the "security_analysis" tab on the left side of the page.
          - [ ] GitHub Advanced Security and Secret scanning button should be greyed out
          - [ ] A yellow reminder pops up : " GitHub Advanced Security cannot be enabled because of a policy setting for the organization."
          
#### Select organization related to secret scan.
1. New Custom patterns in 3 levels
 - enterprise-level is Check the organization to be used for the test sceret scan
 
          -  Navigate to the enterprise settings page `(/hostname/enterprises/codescanner)' .
          - [ ] Click on "policies" on the left side of the page，then Click the " advanced security" tab.
          
          - [ ] Under the Organization Permissions，
          - [ ] Make sure Base permissions is allowed for selected  organization，Check the organization to be used for the test sceret scan,
          - [ ] Click "Security features".
          - [ ] Click on the green "New Custom patterns".
          - [ ] Fill in the "Custom pattern name", the name format Bunch cannot be Chinese.
          - [ ] Fill in the "Secret format", which is required to comply with the example_[A-Za-z0-9]{40} rule, such as octocat_token_[a-zA-Z0-9]{15}.
          - [ ] Click  more options， it will show before Before secret and After secret, Clicking less options and it becomes more options again.
          - [ ] Fill in the password format that can match the rule in "Test string", such as octocat_token_123456789qwerty.
          - [ ] Click create Custom pattern.
          
     - Org-level
          -  Create an organization, Navigate to the org settings page `(/hostname/org/settings/profile)'
          - [ ] Click the "security_analysis" tab on the left side of the page.
          - [ ] Check Automatically enable new repositories and Automatically enable repositories added to Advanced Security.
          - [ ] Click on the green "New Custom patterns".
          - [ ] Fill in the "Custom pattern name", the name format Bunch cannot be Chinese.
          - [ ] Fill in the "Secret format", which is required to comply with the example_[A-Za-z0-9]{40} rule, such as octocat_token_[a-zA-Z0-9]{15}.
          - [ ] Click  more options， it will show Before secret and After secret, Clicking again will stack up and show less options.
          - [ ] Fill in the password format that can match the rule in "Test string", such as octocat_token_123456789qwerty.
          - [ ] Click create Custom pattern.
          
      - Repo-level
          - Create a repo under an organization,Navigate to the repo settings page `(/hostname/org/repo_name/settings/)'.
          - [ ] Click the "security_analysis" tab on the left side of the page.
          - [ ] Enable "GitHub Advanced Security", pops up the Enable GitHub Advanced Security for this repository? 
          - [ ] Clicking "Enable GitHub Advanced Security for this repository".
          - [ ] Enable the Secret scanning.
          - [ ] Click on the green "New Custom patterns".
          - [ ] Fill in the "Custom pattern name", the name format Bunch cannot be Chinese.
          - [ ] Fill in the "Secret format", which is required to comply with the example_[A-Za-z0-9]{40} rule, such as octocat_token_[a-zA-Z0-9]{15}.
          - [ ] Click  more options， it will show before Before secret and After secret, Clicking again will stack up and show less options.
          - [ ] Fill in the password format that can match the rule in "Test string", such as octocat_token_123456789qwerty.
          - [ ] Click create Custom pattern.
          
      
2. Create a PR to add files that contain the pattern secret created by above all.
      - [ ] Navigate to the repo settings page `(/hostname/org/repo_name/settings/)'.
      - [ ] Click code, then create a new file, edit a file, and modify the content to include the password format .
      - [ ] Select Create a new branch for this commit and start a pull request, then Commit new file.
      - [ ] Click pull request.
  
3. View secret scanning alerts
     - Navigate to the repo settings page `(/hostname/org/repo_name/security/secret-scanning)'.
         - [ ] Secret "scanning alerts" is on the left side of the page.
         - [ ] Click the "secret scanning alerts", at least three levels an alert will appear on the list.
         - [ ] On the right side of the alrets list, click Filter and sort to test the filter function. 
          
          
#### New Custom patterns after change permissions is never allowed.
      - enterprise-level
          -  Navigate to the enterprise settings page `(/hostname/enterprises/codescanner)' .
          - [ ] Click on "policies" on the left side of the page，then Click the " advanced security" tab.
          
          - [ ] Under the Organization Permissions，
          - [ ] Make sure Base permissions is never allowed.
          - [ ] Click "Security features".
          - [ ] Click on the green "New Custom patterns".
          - [ ] Fill in the "Custom pattern name", the name format Bunch cannot be Chinese.
          - [ ] Fill in the "Secret format", which is required to comply with the example_[A-Za-z0-9]{40} rule, such as octocat_token_[a-zA-Z0-9]{15}.
          - [ ] Click  more options， it will show before Before secret and After secret, Clicking less options and it becomes more options again.
          - [ ] Fill in the password format that can match the rule in "Test string", such as octocat_token_123456789qwerty.
          - [ ] Click create Custom pattern.
          
     - Org-level
          -  Create an organization, Navigate to the org settings page `(/hostname/org/settings/profile)'
          - [ ] Click the "security_analysis" tab on the left side of the page.
          - [ ] GitHub Advanced Security and Secret scanning button should be greyed out
          - [ ] A yellow reminder pops up : " GitHub Advanced Security cannot be enabled because of a policy setting for the organization."
          

         
          
        
    
        

    
  
