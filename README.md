# Website and documentation for the MIMIC Critical Care Database

## Instructions for running the website locally

1. Install Hugo. For instructions, see: https://github.com/gohugoio/hugo/releases/tag/v0.74.3
2. Clone the website repository:
   ```
   git clone --recursive https://github.com/MIT-LCP/mimic-website.git
   ```
3. Run ```hugo server``` at the command line to build the website and serve the pages;
4. View the website at: http://127.0.0.1:1313

## Note on deploying the website

1. Add mimic-production to remote
   After the pull request of the new material is merged into the main branch of mimic-website, pull down the latest version of main to your  local repo. Run the following command after filling in the IP address for server Heimdallr:
 
   `git remote add mimic-production webuser@<IP address for Webserver>:/home/webuser/mimic-website.git`
 
   * Optional: Check if the command above ran correctly,
   Run command: `git remote -v`
   should return:
   mimic-production webuser@<IP address for Webserver>:/home/webuser/mimic-website.git (fetch)
   mimic-production webuser@<IP address for Webserver>:/home/webuser/mimic-website.git (push)
   origin   https://www.github.com/MIT-LCP/mimic-website (fetch)
   origin   https://www.github.com/MIT-LCP/mimic-website (push)
 
2. Sshuttle into the production server
 
   Run the following command after filling in the  LCP username and IP address: `alias sshholyoke="sshuttle -r <LCP username>@helios.mit.edu <IP address for Webserver, replace list part with '0/24'>"`
 
   Run command: `sshholyoke`
 
   Should return:  “client: Connected” after you enter your password
 
3. Push development
 
   In another terminal from your mimic-website repo:
 
   Run command: `git push mimic-production`


   * Note:
   Your public key (for the machine you're pushing from) must be in the webuser group

   Currently, some minor errors exist related to reading git log. If error messages show up after push to mimic-production, website deployment might still be successful. It is always good practice to check the website after deployment.
   
   Error message is "Failed to read Git log: fatal: not a git repository: '.'". 

## Issues with the website or MIMIC

Please raise issues related to the website or MIMIC-III in the [mimic-code repository](https://github.com/mit-lcp/mimic-code).
