
### Acceptance criteria

1. Create a new repository on GitHub(Org or repo level), adding the .gitignore and select Node.
1. Enable action and create a self-runner.
1. Clone the repository to your loocal machine.
    - [ ] $ git clone https://github.com/your-username/your-repository.git.
    - [ ] $ cd your-repository.
1. Create an index.js file and add a basic alert is:(On your local clone repo)
    - [ ]  alert("Hello, World!");
1. Initialize an npm package with npm init. In the package initialization wizard, enter your package with the name: @YOUR-USERNAME/YOUR-REPOSITORY, and set the test script to exit 0. This will generate a package.json file with information about your package. (On your local machine)
    - [ ]  $ npm init
    - [ ]  ...
    - [ ]  package name: @YOUR-USERNAME/YOUR-REPOSITORY
    - [ ]  ...
    - [ ]  test command: exit 0
    - [ ]  ... 
1. Run npm install to generate the package-lock.json file, then commit and push your changes to GitHub.
    - [ ]  $ npm install
    - [ ]  $ git add index.js package.json package-lock.json
    - [ ]  $ git commit -m "initialize npm package"
    - [ ]  $ git push
1. Find "Publish Node.js Package" in the Actions under this repo, and then click"set up this workflow",delete the job of "publish-npm",and then commit it directly.
1. This workflow will run tests using node and then publish a package to GitHub Packages when a release is created.
1. If the Repo level package published:
    - [ ] On your enterprise, navigate to the main page of the repository.
    - [ ] To the right of the list of files, click Packages.
    - [ ] Click the name of the package that you want to view.
    - [ ] In the top right of your package's landing page, click Package settings.
    - [ ] Click "Delete this package"
    - [ ] To confirm deletion, type the package name and click "I understand the consequences...", deleted it.
    - [ ] On your enterprise, navigate to the main page of the repository.
    - [ ] On the right, click Package settings.
    - [ ] On the left, click Manage versions.
    - [ ] On the top right, use the "Versions" drop-down menu and select Deleted.
    - [ ] Next to the deleted package version you want to restore, click Restore.
    - [ ] To confirm, click I understand the consequences, restore this version.
1. If the Org level package published:
    - [ ] On your enterprise,navigate to the main page of the organization.
    - [ ] To the right of the list of files, click Packages.
    - [ ] Click the name of the package that you want to view.
    - [ ] In the top right of your package's landing page, click Package settings.
    - [ ] Click "Delete this package".
    - [ ] To confirm deletion, type the package name and click "I understand the consequences...", deleted it.
    - [ ] On your enterprise, navigate to the main page of the organization.
    - [ ] Under your organization name, click Settings.
    - [ ] On the left, click Packages.
    - [ ] Under "Deleted Packages", next to the package you want to restore, click Restore.
    - [ ] To confirm, type the name of the package and click I understand the consequences, restore this package.
    - [ ] When restore this package, click package again.
