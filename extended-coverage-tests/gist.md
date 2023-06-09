- With `Enable subdomains` checked in `http(s)://[hostname]setup/settings` (you'll need to append `xip.io` to your hostname because of the [subdomain dependacies](https://github.com/github/help-docs/blob/enterprise-2.0/enterprise/2.0/admin/implementation-guide/index.md#subdomains))
  - Gist
    - [ ] Clicking on *GitHub Gist* goes to Gist creation (`http(s)://gist.[hostname]`)
    - Gist creation (`http(s)://gist.[hostname]`)
      - [ ] "Gist is a simple way to…" banner is displayed on first run
      - [ ] Add a description
      - Name the file
        - [ ] A filename without an extension is created as plain text
        - [ ] Adding an extension to a filename autocompletes the language
      - [ ] Change the indent mode
      - [ ] Change the indent size
      - [ ] Change the line wrap mode
      - Adding a file
        - [ ] Drag a file onto the browser
        - [ ] Click the *Add file* button
      - The main text area
        - [ ] *Create…* buttons are disabled when empty
        - [ ] Add some text and click a *Create…* button
      - Create a public Gist
        - [ ] Ensure that the public Gist gets listed on `http(s)://gist.[hostname]/discover`
      - Create a secret Gist
        - [ ] Ensure that a secret Gist is not listed on `http(s)://gist.[hostname]/discover`
    - The Gist titlebar
      - [ ] Searching for a query opens the suggestion box and a query can be selected
      - [ ] *All gists* goes to Discover Gists (`http(s)://gist.[hostname]/discover/`)
      - [ ] *GitHub* goes to the root of your instance (`http(s)://[hostname]/`)
      - [ ] Clicking the new Gist button goes to to Gist creation (`http(s)://gist.[hostname]`)
      - [ ] Clicking on 'View profile' in the avatar-popover goes to Your Gists (`http(s)://gist.[hostname]/[username]`)
    - Interacting with Gists (`http(s)://gist.[hostname]/[user]/[id/hash]`)
      - Edit
        - [ ] Make a public Gist private
        - [ ] Make a private Gist public
        - [ ] Make a change and click the *Update* button
      - [ ] Delete a Gist
      - [ ] Check a Gist's revisions
      - [ ] Star a Gist and ensure that the stars are updated in the sidebar and inline on `/gist/discover`
      - [ ] Fork a Gist and ensure that the forks are updated in the sidebar and inline on `/gist/discover`
      - [ ] Comment on a Gist and ensure that the number updates inline on `/gist/discover`
      - [ ] Embed a gist
      - [ ] Clone a gist via HTTPS
    - Your Gists (`http(s)://gist.[hostname]/[username]`)
      - With gists present
        - [ ] The number of public/private gists are displayed in the sidebar
      - When there are no gists
        - [ ] "You don't have any gists yet." box is displayed
