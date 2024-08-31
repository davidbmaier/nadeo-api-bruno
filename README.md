# Bruno collection for Nadeo Web Services APIs

This is (hopefully) a convenient starting point for local API testing/discovery of Nadeo's Trackmania Web Services APIs.

For more information, see the [community documentation](<https://webservices.openplanet.dev/>) or reach out on the [Openplanet Discord](https://openplanet.dev/link/discord).

## How to use

This collection is meant for use in [Bruno](https://www.usebruno.com/), an open-source offline-only API client.

To use it in your own installation, simply use Bruno's `Open collection` button and select this repository's folder.

A couple additional hints for using this collection:

- Create a `.env` file and use the template in `.env.sample` to fill it. The auth-related values will automatically be used for authentication calls. It's recommended not to use your main game account, but to create a dummy Ubisoft account for sending arbitrary API requests. Dedicated server accounts can be created [here](https://api.trackmania.com/manager).
- I highly recommend providing a useful user agent in the `.env` file - it will be used in every request in this collection. Make sure to include some way to contact you (e.g. Discord username, email address) so Nadeo is able to identify and reach out to you if necessary.
- All authentication calls (apart from `Refresh Nadeo token`) have post-response scripts that save the relevant ticket/token in your Bruno environment. That way, all other calls can automatically use the correct tokens, and you don't have to copy/paste any authentication values between requests. If that's not working out of the box, make sure you have an environment selected.
- It should be self-explanatory that all requests you send are at your own risk - from Nadeo's perspective this is an undocumented and not officially supported set of APIs, so don't abuse them if you don't want to get banned.

## Background

This is a living repo that may get updated from time to time with new endpoints, parameters and random stuff. Note that this is a reflection of my local environment for testing API endpoints, so some changes may involve moving things around or very minor adjustments - I would recommend to just use it as a starting point and then make your own changes. If you're planning to do that, you may want to fork the repository so you can commit your own changes and track them over time as well.

Also keep in mind that this is not a standalone documentation; most endpoints don't include all possible parameters, and there's no additional explanation of what some of them do. Refer to the [community documentation](<https://webservices.openplanet.dev/>) for information about the endpoints.

Note that this collection doesn't necessarily contain all the documented endpoints, and there's no guarantee that it ever will. It should however be good enough to easily add any missing ones, should you need them (and of course you're more than welcome to open PRs for them if you'd like).
