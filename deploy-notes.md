Deployment Notes

- Create repo, git init
- Copy gitignore from previous project =>
  git commit -m "first commit"
  git branch -M main
  git remote add origin git@github.com:b3nnyc/INSERTREPONAME.git
  git push -u origin main
- npm init
- Create app.yaml

App Engine: - console.cloud.google.com - App Engine -> create app - Following screen provides documentation - click do this later - create app.yaml: - specify what is being used to run code - very first time we create appengine service, cannot give it a name - will give error - one line needed for simple app:
runtime: nodejs16 - service name is website that is created - one project can contain multiple services
service: insert-name-here - gcloud config set project INSERTPROJECTIDHERE - needs to be configured to specific account - if using same account, use cloud shell in project, copy HTTPS link, git clone INSERTLINKHERE - cd INSERTREPONAMEHERE - gcloud app deploy - check and make sure all details are correct - for custom domain goes into dispatch.yaml

        for domains:
            - when telling computers to point to domain, done using A records and subdomains use CNAME to point to pages.
            - for subdomain (eg. thissite.b3nnyc.com) add thissite as a CNAME



Cloud Run: - Cloud Run tab - Create service - Continuously deploy new revisions from a source repository - Set up with cloud build - Authenticate - Install - Choose repo - Choose branch - Build type: Go, Node.js ... - Add start script (found in package.json) - Choose region - Authentication - allow unauthenticated invocations
