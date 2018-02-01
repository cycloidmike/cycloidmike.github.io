---
layout: default
---

# How to set up a personal website using AWS Route 53 and GitHub Pages

1. Create a GitHub account
  - [https://github.com/](https://github.com/)
  
2. Create a new repository and name it _{username}_.github.io where _{username}_ is your github user name
  - [https://github.com/new](https://github.com/new)
  - Your source code will be accessible to the public but it's **free**. You also have the option to upgrade your account to create private repos.

3. Create an AWS account and register a domain
  - [https://console.aws.amazon.com/route53/home?DomainRegistration](https://console.aws.amazon.com/route53/home?DomainRegistration)
  - It costed me $12 for a .com top level domain
  - Hosting it in Route 53 costs me $0.51 per month
    - $0.50 fixed cost to add my domain to their hosting service
    - $0.01 variable cost of $0.40 per 1,000,000 queries
    - Current prices - [https://aws.amazon.com/route53/pricing/](https://aws.amazon.com/route53/pricing/)
   
4. In AWS, navigate to Route 53 -> Hosted Zones and select your domain name.
5. Click the blue "Create Record Set" button near the top
6. Add **www** as the name, since Route 53 doesn't support URL rewrites.
7. Change the Type to **CNAME - Canonical name**
8. Set the value to _{username}_.github.io and click Create

9. Navigate to your GitHub Page https://github.com/{username}/{username}.github.io
10. Opening up the repo's settings and scroll down to the GitHub Pages section
11. Set the custom domain to www.{yourdomain} and save
12. Add some content to your repo
  - All you need is an index.html in your repo or you can use a built in Jekyll theme
13. Go to your domain and enjoy

###Update- I've switched over to Google Domains because Route 53 does not support routing of apex domains and the first million queries are included with registering the domain to Google.

[back](./)
