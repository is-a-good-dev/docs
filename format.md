# Formats

Following the specific JSON format is important as it allows us to easily process your domain without any issues. If the correct format is not followed, you will be told and the pull request will **not** be merged. 

Currently we only accept `A` and `CNAME` records. If you would like your domain to be redirected, you will have to use external tools such as [redirect.pizza](https://redirect.pizza) as we don't have the required resources to do this at the moment. 

When submitting your pull request, we ask that you add your email under the email key in the file. This is so that we can contact you if anything is due to change or if your subdomain has violated laws, terms or anything of that nature. Invalid contact details will end up with you being refused a subdomain. 

## JSON Format Template
```json
{
  "repo": "",

  "owner": {
    "username": "",
    "email": ""
  },

  "target": {
    "record-type": {
       "name": "", 
       "value": ""
     }
  },

  "proxied": false
}
```

**Breakdown of the template**:
- *"repo"* - This is your repository, the place where the code for the site is. If you don't have a repository you can leave this field blank or remove the field.
- *"owner"* - This is a category for your information. This section needs to be filled out, or your pull request will **not** be merged.
  - *"username"* - This is where you put your GitHub username.
  - *"email"* - This is where you put your email address.
- *"record-type"* - This is a category for the record information.
  - *"name"* - This is the desired subdomain.
  - *"value"* - This is the value for the record, for example with an `A` record it would be an IP.
- *"proxied"* - If you want the record proxied through Cloudflare. If you don't know what it means, leave it to false.

## JSON Example 
```json
{
  "repo": "https://github.com/is-a-good-dev/docs",

  "owner": {
    "username": "is-a-good-dev",
    "email": "will@is-a-good.dev"
  },

  "target": {
    "CNAME": {
      "name": "docs", 
      "value": "hosting.gitbook.io"
    }
  },

  "proxied": false
}
```
*You can find the the file [here](https://github.com/is-a-good-dev/register/blob/main/reserved/docs.json).*

---
**If you are unsure about this, [open a new issue](https://github.com/is-a-good-dev/register/issues/new) and one of the maintainers or helpers will help you out.**
