# Org Team Onboarding (PAGE IN REVIEW)

Handle setting up and onboarding of new team members for the organisation team for each event.

## General Tasks

* Set up new team member accounts in the system
* Assign appropriate roles and permissions
* Ensure all necessary documentation is available to new team members
* Monitor progress and provide support as needed

## Timeline

### Pre-kickoff

* Put out a call-for-volunteers form
  * Announce on socials
  * Reach out to known local community members for recommendations and interest
* Review runbooks and roles for updates needed from previous feedback and retros
* Create a new event-specific GitHub team on GitHub (e.g. [Org Team - Dutch Cloud Native Day 2026
](https://www.dutchcloudnativeday.nl/team/))
* Create a new event-specific private repo (e.g. `utrect-26`) for storing all relevant documents and tracking issues
* Setup a new Project board on GitHub for the new event, associated with the newly created repo
* Give the Steering Committee team admin permissions to the Repo and Project board
* Give the newly created Org team admin permissions to the Repo and Project board

### Kickoff

* Organise a kick-off meeting for the new Org Team
  * Provide an overview of the event, its goals and the structure of Dutch Cloud Native Day
  * Assign roles and responsibilities to each team member
  * Collect all volunteers GitHub usernames
* Add all Org Team volunteers as members of the new GitHub team
  * This can be done with the following CLI command:

    ```shell
    TEAM_NAME="org-team-amsterdam-2026"
    USER="XXX"

    gh api \
      --method PUT \
      -H "Accept: application/vnd.github+json" \
      -H "X-GitHub-Api-Version: 2022-11-28" \
      /orgs/RejektsConference/teams/$TEAM_NAME/memberships/$USER \
      -f 'role=member'
    ```

* Reach out to responsibility roles and provide access to needed credentials and services

### Post Conference

* Organise a retro with Org Team and collect feedback on the event
  * What went well?
  * What didn't go well?
  * Any CoC incidents?
  * Review any attendee feedback

## Reminders or Common Mistakes

<!-- What do you always try to remember when you come back to this every year? Do you often find yourself scrambling for vendors? Are you always trying to remember where you left your towel? Leave notes for the next person so we can improve :) -->
