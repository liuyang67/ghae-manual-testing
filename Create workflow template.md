
 



# Acceptance criteria

## Repo level 

###  Scenario: Only the suggested templates are displayed, the templates created by yourself are not displayed on Repo level .

1. Open the AE instance, Navigate to [hostmane]/new,create a new repo named ".github", Do not check "Add a README file", click create repository.

2. Create new folder  in  .github  repo , add 2 new file in the created folder.
   - Create a new folder named workflow-templates
   - Create 2 new file in workflow-templates
     - [ ] test1.properties.json
     
     
      	          {
				    "name": "Octo Organization Workflow",
				    "description": "Octo Organization CI workflow template.",
				    "iconName": "star",
				    "categories": [
				        "Go"
				    ],
				    "filePatterns": [
				        "package.json$",
				        "^Dockerfile",
				        ".*\\.md$"
				    ]
				}

      - [ ] test1.yml
      
                    name: Octo Organization CI
				
				on:
				  push:
				    branches: [ $default-branch ]
				  pull_request:
				    branches: [ $default-branch ]
				
				jobs:
				  build:
				    runs-on: ubuntu-latest
				
				    steps:
				      - uses: actions/checkout@v2
				
				      - name: Run a one-line script
				        run: echo Hello from Octo Organization
                
5. Download the svg pictures, then Navigate to [hostname]/.github/upload/main, choose your files,Commit directly to the main branch,click commit changes.

    - Download svg ：https://www.ikonate.com/
    - Note:

		- [ ] This .svg file should changed to same  with test1.properties.json : iconName

       - [ ] Eg. My iconName is star, so my .svg file name should be star.svg
      
    
6. Then the folder(workflow-templates) should show:
    - test1.properties.json
    - test1.yml 
    - star.svg
 
7. Check result:
   - Navigate to [hostname]/orgname/.github/actions/new.
   - You can only see suggested templates.
  
##   Enterprise level or organizational level 

###  Scenario: Display two workflow template,One is you just created, anther is the default template on enterprise level or organizational level.

1. Open the AE instance,Navigate to [hostmane]/enterprises/codescanner.
2. Create an organization,(such as org-rep-ruoxi-1 ),click settings, Click the action tab on the left side of the page，select allow all action, save.
3. Under the organization you just created, create a new repo named ".github", Do not check "Add a README file",click create repository.
4. Create new folder  in  .github  repo , add 2 new file in the created folder.
   - Create a new folder named workflow-templates
   - Create 2 new file in workflow-templates
     - [ ] test1.properties.json
     
     
      	          {
				    "name": "Octo Organization Workflow",
				    "description": "Octo Organization CI workflow template.",
				    "iconName": "star",
				    "categories": [
				        "Go"
				    ],
				    "filePatterns": [
				        "package.json$",
				        "^Dockerfile",
				        ".*\\.md$"
				    ]
				}

      - [ ] test1.yml
      
                    name: Octo Organization CI
				
				on:
				  push:
				    branches: [ $default-branch ]
				  pull_request:
				    branches: [ $default-branch ]
				
				jobs:
				  build:
				    runs-on: ubuntu-latest
				
				    steps:
				      - uses: actions/checkout@v2
				
				      - name: Run a one-line script
				        run: echo Hello from Octo Organization
                
5. Download the svg pictures, then Navigate to [hostname]/.github/upload/main, choose your files,Commit directly to the main branch,click commit changes.

    - Download svg ：https://www.ikonate.com/
    - Note:

		- [ ] This .svg file should changed to same  with test1.properties.json : iconName

       - [ ] Eg. My iconName is star, so my .svg file name should be star.svg
      
    
6. Then the folder(workflow-templates) should show:
    - test1.properties.json
    - test1.yml 
    - star.svg
 
7. Check result:
   - Navigate to [hostname]/orgname/.github/actions/new.
   - You can see workflow template created by you under the suggested templates.
   - Make sure the template you created appears and the avatar is the svg image you uploaded.
   - Open the created template, click set up this workflow ,Click Edit new File or Preview .
   - Make sure that the template has no garbled characters and can be edited，Preview displayed normally, and can be submitted.
   
   
   
 ## Scenario: Display one workflow template just you create on enterprise level or organizational level.
 
 
1. Open the AE instance,Navigate to [hostmane]/enterprises/codescanner.
2. Create an organization,(such as org-rep-ruoxi-1 ),click settings, allow all action, save.
3. Under the organization you just created, create a new repo named ".github", check "Add a README file",click create repository.
4. Create new folder  in  .github  repo , add 2 new file in the new folder.
   - Create new folder(workflow-templates) in .github
   - Create 2 new file in folder(workflow-templates)
     - [ ] test1.properties.json
     
     
      	          {
				    "name": "Octo Organization Workflow",
				    "description": "Octo Organization CI workflow template.",
				    "iconName": "star",
				    "categories": [
				        "Go"
				    ],
				    "filePatterns": [
				        "package.json$",
				        "^Dockerfile",
				        ".*\\.md$"
				    ]
				}

      - [ ] test1.yml
      
                    name: Octo Organization CI
				
				on:
				  push:
				    branches: [ $default-branch ]
				  pull_request:
				    branches: [ $default-branch ]
				
				jobs:
				  build:
				    runs-on: ubuntu-latest
				
				    steps:
				      - uses: actions/checkout@v2
				
				      - name: Run a one-line script
				        run: echo Hello from Octo Organization
                
5. Download the svg pictures, then Navigate to [hostname]/.github/upload/main, choose your files,Commit directly to the main branch,click commit changes. 

    - Download svg ：https://www.ikonate.com/

    - Note:

		- [ ] This .svg file should changed to same  with test1.properties.json : iconName

       - [ ] Eg. My iconName is star, so my .svg file name should be star.svg
      
    
6. Then the folder(workflow-templates) should show:
    - test1.properties.json
    - test1.yml 
    - star.svg
 
7. Check result:
   - Navigate to [hostname]/orgname/.github/actions/new.
   - You can see workflow template created by you
   - Make sure the template you created appears and the avatar is the svg image you uploaded.
   - Open the created template, click set up this workflow ,Click Edit new File or Preview .
   - Make sure that the template has no garbled characters and can be edited, Preview displayed normally, and can be submitted.
   
   
## Scenario: Template icons showing related tests .

1. Open the AE instance , Navigate to [hostmane]/enterprises/codescanner. 
2. Create an organization,(such as org-rep-ruoxi-1 ),click settings, allow all action, save.
3. Under the organization you just created, create a new repo named ".github", check "Add a README file",click create repository.
4. Create new folder  in  .github  repo , add 2 new file in the new folder.
   - Create new folder(workflow-templates) in .github
   - Create 2 new file in folder(workflow-templates)
     - [ ] test1.properties.json
     
     
      	          {
				    "name": "Octo Organization Workflow",
				    "description": "Octo Organization CI workflow template.",
				    "iconName": "star",
				    "categories": [
				        "Go"
				    ],
				    "filePatterns": [
				        "package.json$",
				        "^Dockerfile",
				        ".*\\.md$"
				    ]
				}

      - [ ] test1.yml
      
                    name: Octo Organization CI
				
				on:
				  push:
				    branches: [ $default-branch ]
				  pull_request:
				    branches: [ $default-branch ]
				
				jobs:
				  build:
				    runs-on: ubuntu-latest
				
				    steps:
				      - uses: actions/checkout@v2
				
				      - name: Run a one-line script
				        run: echo Hello from Octo Organization
                
5. Download the non svg pictures, then Navigate to [hostname]/.github/upload/main, choose your files,Commit directly to the main branch,click commit changes.
            
6. Then the folder(workflow-templates) should show:
    - test1.properties.json
    - test1.yml 
    - picture
 
7. Check result:
   - Navigate to [hostname]/orgname/.github/actions/new.
   - You can see workflow template created by you.
   - Make sure the template you created appears and the avatar is  garbled characters.
   - Open the created template, click set up this workflow ,Click Edit new File or Preview .
   - Make sure that the template has no garbled characters and can be edited, Preview displayed normally, and can be submitted.
   
   
   
 

 ## Scenario:This case requires permission testing
 
   - refer to :   
   
  	- https://github.ghe.com/beyondsoft-ghae-testing/CustomDocs/blob/main/GitHubAdvancedSecurity.md
                   
  	- https://github.com/github/c2c-actions/blob/main/docs/test-manifests/access-policy.md






      









