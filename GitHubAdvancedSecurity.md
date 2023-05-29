# Access Policy

## Assumptions

- At least one organization has been set up under the enterprise.
- At least one repository has been set up under one of these enterprise-managed orgs.
- Tester is an enterprise admin, i.e. they have admin access at the enterprise, org, and repo levels and are allowed to modify those settings.

## Enterprise-level settings

### Acceptance criteria

1. Navigate to the Enterprise settings page (`/enterprises/:enterprise/settings/profile`).
1. Click on "Policies".
    - [ ] "Actions" should now be an option on the sidebar.
1. Click on "Advanced Security".
    - [ ] "Base permissions" section (in page body) should have "Allow for all organizations".
1. Change "Base permissions" option to "Allow for seleted organizations".
    - [ ] A list of organizations that the enterprise manages should appear below the dropdown.
    - [ ] Each organization should have "Not allowed" selected by default in far right dropdown.
1. Select all organizations.
    - [ ] A new menu titled "Set organization permissions" should appear on the far right.
1. Select "Allowed" in bulk actions menu.
    - [ ] Menu for each organization in the list will now be set to "Allowed".
1. Apply "Not allowed" to all organizations.
1. Above the organization list, change "Enable for seleted organizations" to "Never allow".
    - [ ] Org list disappears.
    - [ ] Radio buttons underneath are all disabled.
1. Above the organization list, change "Never allow" to "Allow for all organizations"

## Org-level settings

Github Advanced Security is considered **allowed for an organization** if all of the following is true:

- an org admin allowed Github Advanced Security for all organizations.
- an org admin allowed Github Advanced Security for certain organizations and that includes the one we're testing.

Scenarios should be tested under each of these conditions.

### Acceptance criteria

1. Navigate to an org's settings page (`/organizations/:org/settings/profile`).
    - [ ] "Security & analysis" should be an option on the left navigation.
1. Click on "Security & analysis" in navigation menu.
    - See individual scenarios below.

**Scenario: Org can run Github Advanced Security**

- Requirement: At least one repository has been created for certain organizations.
- "Policies" section:
  - [ ] "Disable all" Under GitHub Advanced Security is clickable by default.
  - [ ] "Enable all" Under GitHub Advanced Security is unclickable.
  - Changing the option to:
    - "Disable"
      - [ ] "Disable all" Under GitHub Advanced Security is unclickable.
      - [ ] "Enable all" Under GitHub Advanced Security is clickable.

**Scenario: Org cannot run Github Advanced Security when no repo**

- Requirement: There is no repository has been created for certain organizations.
- "Policies" section:
  - [ ] Under GitHub Advanced Security, "Disable all" and "Enable all" is disabled and cannot be changed to anything else.
  - [ ] No message appears.
- [ ] "Secret scanning" section underneath are disabled.

**Scenario: Org is not allowed to run Github Advanced Security**

- "Policies" section:
  - [ ] Under GitHub Advanced Security, "Disable all" and "Enable all" is disabled and cannot be changed to anything else.
  - [ ] "GitHub Advanced Security cannot be enabled because of a policy setting for the organization." message appears.
- [ ] "Secret scanning" section underneath are disabled.
