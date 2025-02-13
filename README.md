# vps-playbook
An ansible playbook that deploys my VPS through GitHub Actions

## What is the purpose of this repository?
The purpose of this repository is to learn and apply CI/CD principles and Ansible best practices. 
Using ansible-playbooks to deploy VPSes (Virtual Private Servers) and Github Actions (CI/CD Pipeline)

## What's the vision of this project?
The vision of this project is to have an automated workflow to make changes to my server when needed.

## What's the plan?
The plan is that every time a change happens in the main branch it will trigger the cd workflow which deploys the changes to the server.
The ci part will be handled on merge requests where tests will be ran to make sure everything works.

## What is the workflow? What tools will be used?
### Tools to be used:
  1. Github Actions (CI/CD pipeline)
  2. Ansible (Deployment)
  3. Molecule (testing)
  4. Ansible-lint (linter)

### Repository rules to be applied:
  1. No force push allowed
  2. Commit to main only via merge request and upon rafasmour's approval
  3. Merges will be made only if all tests are passed
  4. Actions tab will be invisible to others

### How to secure this workflow:
  1. Actions that have sensitive information will be imported from private actions
  2. The public will only be able to see the structure of the workflow not the actions tab
  3. Fork any third-party actions that will be used to make sure no secrets are leaked

### How to make this workflow fast:
  1. Use Alpine as the linux distro as its lightweight
  2. Refine the workflow and make sure only necessary steps or taken

### How to make this workflow cheap:
  1. Reduce time required for the workflow to run
  2. Always plan before executing to avoid wasting time

### How to make this workflow future proof:
  1. Stick to best practices ( can't go wrong)
  2. Always take a step back before execution
  3. Leave room open for additions in the playbook

### How to work with this:
You need to open a branch if you are a collaborator or the owner. Once you test evertyhing on your localmachine and push it and satisfy the branches goals you make a merge request. if tests are not passed repeat.
The tests will be done with Molecule on docker ubuntu containers

### Skills required before getting started:
 - [X] Github Actions
 - [X] Ansible
 - [ ] GitHub Repository Rules
 - [X] Git
 - [ ] Molecule
 - [X] CI/CD
 - [ ] Best Practices 

### Things to consider/read before starting (for rafasmour):
 - [ ] Get a coffee ☕
 - [ ] Read about github rules
 - [ ] Read about Github action import from private repos
 - [ ] Read about Molecule
 - [ ] Plan the structure of the playbook
 - [ ] Plan the structure of the VPS
```
What users will exist?
Main user (to be used by Sys Admins):
- Sudo access
Deployer user (to be used by Ansible or other deployers):
- Limited access to Docker and non-sudo commands
Root user:
- Capture, silence, kidnap and lock him up.
- Forget about him...

How will apps be shipped into production:
Using a similar workflow to this repo
after tests are done and a merge request is made
deploy using either GitHub Actions or Ansible playbooks

````
 
   
