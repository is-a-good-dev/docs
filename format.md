# Formats

Following json formats is important as it allows us to easily process your domain without any issues. If the correct json format is not followed, you will be told and the pull request will **not** be merged. 

Currently we only accept `A` and `CNAME` records. If you would like your domain to be redirected, you will have to use external tools such as [redirect.pizza](https://redirect.pizza/) as we don't have the required resources to do this at the moment. 

When submitting your pull request, we ask that you add your email under the email key in the json. This is so that we can contact you if anything is due to change or if your sub-domain has violated laws, terms or anything of that nature. Invalid contact details will be refused a sub-domain. 

## JSON Format Template

```json
{
  "repo":"", 
  "owner":{
    "username":"",
    "email":""
  },
  "target":{
  "record-type":""
  },
  "proxied": false
}
```
**Breakdown of json template:**
- *"repo"* - This is your repository, the place where the code for the site is. If you don't have a repository you can leave this blank.
- *"owner"* - This is a category for your information. This section needs to be filled out, or your PR will **not** be merged.
  - *"username"* - This is where you put your Github username. 
  - *"email"* - This is where you put your email.
- *"target"* - This is a category for the record information. 
  - *"record-type"* - This key will be replaced with either  `A` or `CNAME`. This is where you will add the record type and the target. 
- *"proxied"* - Whether you need it proxied through Cloudflare. If you don't know what it means, leave it to false.

## JSON Example 
```json
{
  "repo":"https://github.com/is-a-good-dev/docs",
  "owner":{
    "username":"wclarkey",
    "email":"will@wclarke.dev"
   },
   "target":{
     "CNAME":"hosting.gitbook.io"
    },
    "proxied": false
}
```
*See the file [here](https://github.com/is-a-good-dev/Register/blob/main/sub-logs/docs.json).*

---
**If you are unsure about this, [open a new issue](https://github.com/is-a-good-dev/Register/issues/new) and one of the maintainers or contributors will help you out.**
