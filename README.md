![banner](images/puppet-may-the-source-be-with-you-2023.jpg)

# May The Source Be With You - Hackathon 2023

Welcome to our first annual _May the Source Be With You_ virtual hackathon focused on improvements to our developer tooling ecosystem.

Do you have a pet peeve about the PDK, rspec-puppet, puppet-lint, the Puppet VSCode extension, or any other tool you use when building Puppet code? Join forces with us to help defeat these pain points during our live event.

* May 4th, 2023
* PDT: 10 am - 6 pm 
* CEST: 10 am - 6 pm 

----

Table of Contents
-----------------

- [Before starting](#before-starting)
- [Tools and resources](#tools-and-resources)
- [List of challenges](#list-of-challenges)
- [Submitting your contribution](#submitting-your-contribution)

### Before starting

- [Sign up for the hackathon](https://docs.google.com/forms/d/e/1FAIpQLSc0jDa0SIFJjmBh9q2SoH55hIixFXbCWyedvGib5eUiRXyZbg/viewform) In case you haven't done that before
    - 🦤 A little birdie says that you might even get a bit of exclusive swag for participating, too! 
- Make sure you are logged in the [Puppet Community Slack](https://slack.puppet.com/)
- Join the [`#hackathons`](https://puppetcommunity.slack.com/archives/C055MT5TA2K/p1683127438265399) channel
    - Most of the communication will be asynchronous, make sure you are in that channel so you don't miss anything!
- Have some coffee ☕ and cookies 🍪 handy 

### Tools and resources

- [Zoom](https://support.zoom.us/hc/en-us/articles/4415294177549-Downloading-the-Zoom-desktop-client-and-mobile-app). The hackathon kick-off and closing will happen via Zoom, make sure to check the `#hackathons` channel for more up to date information.
- [Slack](https://slack.com/download)

### List of challenges

- Developer tooling ecosystem
    - [Puppet Rspec](https://github.com/puppetlabs/rspec-puppet)
        - RSpec tests for your Puppet manifests & modules
        - Open issues: https://github.com/puppetlabs/rspec-puppet/issues
    - [Puppet Litmus](https://github.com/puppetlabs/puppet_litmus)
        - Litmus is a command line tool that allows you to run acceptance tests against Puppet modules
        - Open issues https://github.com/puppetlabs/puppet_litmus/issues
    - [Puppet VS Code extension](https://github.com/puppetlabs/puppet-vscode)
        - Open issues https://github.com/puppetlabs/puppet-vscode/issues
    - [Provision](https://github.com/puppetlabs/provision)
        - When provisioning to GCP fails, make `provision::provision_service provisioner` retry on 500 error responses, there should be a MAX RETRY set though (3). So, the CI doesn’t fail due to provisioning failures.
        - Previous attempts: https://github.com/puppetlabs/provision/pull/194
    - [PE Status Check](https://github.com/puppetlabs/puppetlabs-pe_status_check)
        - lookup indicator_exclusions from hiera pe_status check
        - Related issue on Github: https://github.com/puppetlabs/puppetlabs-pe_status_check/issues/127
    - Rubocop offenses
        - Help us to fix Rubocop offenses from our tooling and modules.
        - This is a good way to get to know a new project, by making small changes to reduce the number of Rubocop offenses in a project.
        - This is just one example about a [rubocop TO DO file from the PDK project](https://github.com/puppetlabs/pdk/blob/main/.rubocop_todo.yml)
        - The best approach to fix these would be to:
            - find repos with a rubocop_todo.yml
            - Look at the rules that have been excluded
            - Comment one out
            - Run bundle exec rubocop
            - Commit your changes :)
        - Here is the general search on all our public Github repos that use a `.rubocop_todo.yml` file: https://github.com/search?q=org%3Apuppetlabs+path%3A.rubocop_todo.yml&type=code
    - [Forge Ruby Gem](https://github.com/puppetlabs/forge-ruby)
        - Issue: This library (gem) currently does no response caching of its own, instead opting to re-issue every request each time.
- General help needed
    - [Puppet's repositories labeled as `hacktoberfest`](https://github.com/search?q=topic%3Ahacktoberfest+org%3Apuppetlabs+fork%3Atrue&type=repositories)
- Greenfield solutions
    - Build a module’s legacy facts scanner, it should receive an optional parameter (replace=true) to replace automatically the legacy facts for current facts
- Bring your own challenge
    - Maybe you have a bug that has been bothering you for some time now, or you want to improve a feature that your work depends on. Work on something that motivates you 😊
    - You are not familiar with Puppet's Dev tooling ecosystem but you still want to contribute in a module? Please feel free to do that 🙌

### Submitting your contribution

After creating a Pull Request (PR) on the Github repositories, make sure to add the label `MayTheSourceBeWithYou` to it.