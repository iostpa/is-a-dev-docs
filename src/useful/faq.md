---
tags: useful
icon: question
---

# Frequently Asked Questions (FAQ)

## Which records are supported?
We support the following records:
- A
- AAAA
- CNAME
- MX
- TXT
- URL (Redirection)
- NS (limited access)
- SRV
- CAA

## Why does my domain still redirect to the is-a-dev website?
This usually occurs due to the cache of your browser becoming invalid and [clearing your browser's cache](https://support.google.com/accounts/answer/32050) should solve this issue.

## Can I use a CNAME record with any other records?
You cannot request a subdomain nor submit changes containing a CNAME with any other records (TXT, A, MX, etc...)

## How long will it take for my PR to get merged?
When we get into it. We always want you to wait for as short as possible. But maintainers cannot always be online. We have school and work, this is just a side project. Just be patient and we'll get to it as soon as possible! For a chance for a quicker review, send your PR in [⁠pull-requests](https://discord.com/channels/830872854677422150/1130858271620726784).

## Which services do you support?
We support all services. For example: GitHub Pages and Cloudflare Pages.

## Can I create nested subdomains? (sub-sub domains)
Yes, you can! Simply create a file such as `blog.example.json` and follow the same guidelines as you would while registering `example.json`. Please note in order to have `blog.example.is-a.dev`, you must also own `example.is-a.dev`.

## How can I edit my domain?
You can edit your domain's JSON file and submit a pull request to edit your domain.

## How can I delete my domain?
You can delete your domain's JSON file and submit a pull request to delete your domain.

## I keep getting a SSL error while using GitHub Pages, how do i fix this?
You need to go to your GitHub Pages settings on your website repository (likely called `<user.github.io>`) and make sure the `Enforce HTTPS` option is enabled to avoid this error.

## Can I be a maintainer/join the team?
No, we handpick every member of our team. You can increase your chances of being chosen by helping out people in our help forums.

## I have accidentally leaked sensitive information in my PR, how can I get my PR deleted?
If your PR **has not been merged**, you can email [security@m.is-a.dev](mailto:security@m.is-a.dev) or DM [williamharrison on Discord](https://discord.com/users/853158265466257448) however, if it has been merged already, then there is nothing we can do about it unfortunately.

## My DNS records are not updating even after 48 hours, what should I do?
Please open a help thread via any of our help channels and we will look into it.

## Can I use my domain for a minecraft server?
Sure, but it needs to be a nested subdomain (mc.example.is-a.dev). You would normally use a A record for this.

## Can I use NS records?
We allow NS records for the following reasons and users:
  - is-a.dev maintainers
  - Users who are using **multiple** Cloudflare (or similar providers') services, which often require their own zones (e.g., DynDNS, cloudflared tunnels, etc.)
  - Users who require a private zone, as they are using their home IP addresses behind Cloudflare (These cases will be carefully reviewed, as we understand some may claim to use a home IP address when they are not.)
  - Users with a lot of nested subdomains *may* be allowed to register NS records so they do not have to manage multiple files.
  - Aternos users (specifically Aternos, as they require NS records and you cannot modify DNS records under them).
!!!warning Note
These guidelines are not set in stone and may change. You are not limited to fitting only one of the criteria above; use them as a general guide. [@wdhdev](https://github.com/wdhdev) personally review each NS record request.
!!!

*We reserve the right to deny NS records at our discretion.*

## How can I make changes to my is-a.dev subdomain?

1. **Open your JSON file:** Navigate to the `domains` directory in your local repository and open the JSON file corresponding to your subdomain (`domains/<subdomain>.json`).

2. **Make your changes:** Edit the JSON file (or delete) to reflect the changes you want to make.

3. **Commit your changes:** Once you've made your changes, commit them to your local repository.

4. **Push your changes:** Push your changes to your forked repository on GitHub.

5. **Submit a Pull Request:** Go to your forked repository on GitHub and open a pull request.

6. **Wait for your PR to be merged:** After you have submitted your pull request, wait for it to be reviewed and merged. Once your pull request has been merged, your changes should be live!
!!!warning Warning
Make sure to monitor your PR for reviews in case some changes are requested. Also note that it can take up to 48 hours in some cases for your changes to take effect after your PR is merged.
!!!
