# Basic Realm Environment Workflow + CI/CD


#### Github auto deploy currently needs initial UI configuration - start with 2 apps created on the UI

1. [UI] Add environment tags to the dev and prod app in the ‘Deployment’ section
2. [UI] Add relevant environment variables that you may already be using in your app logic in the ‘Values’ section
3. [UI] Configure both apps to deploy from the Github branches/repositories corresponding to each app’s environments in the ‘Deployment’ section
4. Export the dev app via UI or realm-cli
5. Use `%%environment.values.<name>` or `context.environment.<name>` to use across configs and environment values to define environment variables. 
6. Push config to the dev GitHub branch linked to the dev app
7. Make PR to master/prod or run any CI/CD actions (builds, tests, etc) when commit is pushed
8. Ensure master branch source has environment set to ‘production’ in realm_config.json - don’t change this after the first time this is set and add file to .gitignore if needed. 
9. Push PR to master
10. New source on master branch should be reflected in the production app config in the cloud. 
11. Repeat.


This repo has a sample state of what your development and master/prod branch should look like when using Realm Apps with Github Autodeploy
