# Basic Realm Environment Workflow + CI/CD


### Github auto deploy currently needs initial UI configuration on with 2 apps already created from the UI

1. Add environment tags to the dev and prod app in the ‘Deployment’ section
2. Add relevant environment variables that you may already be using in your app logic in the ‘Values’ section
3. Configure both apps to deploy from the Github branches/repositories corresponding to each app’s environments in the ‘Deployment’ section
4. Export the dev app via UI or realm-cli
5. Push to the dev GitHub branch
6. Use %%environment.value to use across configs and environment values to define environment variables. 
7. Make PR to master/prod or run any CI/CD action when commit is pushed
8. Ensure master branch source has environment set to ‘production’ in realm_config.json - don’t change this after the first time. 
9. Push changes. 
10. Repeat.