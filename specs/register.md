# Register


## As a user register

Assumptions:
* Registration of a 3bot is located on a ‘centralized bootstrap 3bot’ that has access to the threefold network to launch 3bots and send emails
* Code will be added to the threefold code base
  * Frontend code & high level flow in this repo
  * Using JSX as a backend lib for blockchain / ... technology
* We need a system to prevent bots for creating lots of (FREE) 3bots
 * Suggestions: Captcha (first version), SMS verification (next version)
* Location is a list of regions to get a 3bot close to your location
* After clicking deploy, user is redirected to their 3bot for initialization
### Mockups

![Register mockups](./images/register.svg)


### Actions after submitting

- We register 3bot on the blockchain (is in JX)
- Send email to user; containing link to 3bot init page (using a token in the url for security)
- Deploy 3bot in correct location, configure url in webgateway? [urls](./urls.md)
