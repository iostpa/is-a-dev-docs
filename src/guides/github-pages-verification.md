---
label: Github Pages Verification
---

# Verify your is-a.dev Domain with GitHub Pages

## Get your verification string

1. Open GitHub, press on your profile icon on the top right, and press `Settings`.

![1]("../img/github_pages_verification_step_1.png")

2. Press `Pages`.

![2]("../img/github_pages_verification_step_2.png")

3. Press `Add a domain`.

![3]("../img/github_pages_verification_step_3.png")

4. In the field that appears, type your is-a.dev domain name (e.g. `myname.is-a.dev`) and press `Add domain`.

![4]("../img/github_pages_verification_step_4.png")

5. Copy the hostname and the verification string.

![5]("../img/github_pages_verification_step_5.png")

## Create the domain file

Create a JSON file inside the `domains/` directory called `domains/hostname.json` using the hostname you copied in step 5 with the following content and submit a pull request:

```json
{
    "owner": {
        "username": "<github-username>",
        "email": "<email@address>"
    },
    "record": {
        "TXT": "<github-verification-string>"
    }
}
```

## Configuration
After your pull request has been merged, repeat the steps to get the verification string and press the `Verify` button.
If it shows any error such as `Unable to verify your domain`, try waiting a few minutes (sometimes up to 24 hours) as the DNS change might not have reflected on the DNS server.
