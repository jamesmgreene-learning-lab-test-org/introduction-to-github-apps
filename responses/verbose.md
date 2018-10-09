## Set-up

BOT: On registration, create an empty repository called introduction-to-github-apps
BOT: Open the first issue using the text from responses/01_intro-gh-apps.md with the title "Introduction to GitHub Apps"


### ISSUE ONE

01_intro-gh-apps.md - ISSUE

TITLE: Introduction to GitHub Apps
TEXT:

Hey! I'm _so_ excited you're here to learn about Apps! Who doesn't like talking about themselves?

We'll quickly get some foundations out of the way, and then apply that knowledge to some real applications.

### Starter questions

> What's an app(lication)?

In this context, apps are software with a bunch of functionality whose purpose is to make your life easier.

The dictionary calls an application "a formal request to an authority for something," which can also be true in software. When you request a service do something, you're appealing to a greater authority and hoping that it works.

When it doesn't, there's always Twitter. But not in my case! Here, we've got something called the Community Forum. You should leave your concerns there and my human minions will help you fix any issues.

> Why would people use it???

As humans, we're constantly generating data. Photos, text, financial transactions, etc. In your everyday life, you use a ton of software applications to help you create, manage, and sort through all of this data. You might use an e-mail client to compile and **style** your thoughts, a social platform to share and view photos and news, or mobile application to respond to immediate alerts like a social invitation out (your message application) or a financial notification.

Depending on your circumstances, it's likely that your life is just a series of interactions between one application, to another, to another, until you go to bed and use an application to help you wake up in the morning (alarm software) and do it all again.

Really bleak, if you think about it. We should probably all exercise more so we can get away from all this... while listening to music through an application and having our workout tracked so we can monitor ourselves and make sure we're healthy.

... there's no escaping this.

> How does this work on GitHub?

GitHub **is** an app. It comes with a ton of built in functionality to help you manage your work and collaborate. We're hiding processes behind the scenes to help you focus on what's important: your code. And we're consistently releasing new features to make sharing easier.

GitHub Apps allow you to change GitHub's surface-level functionality to automate core actions based on specific behaviors. Whether this is to abstract repetitive processes away, ensure a baseline of behavior, increase community involvement and understanding, or something entirely unexplored, you can change GitHub's default processes to add your own value.

<details><summary>I still don't get the difference.</summary>

Here's a metaphor -- picture an iceberg.
![Iceberg](https://media.istockphoto.com/photos/iceberg-picture-id452595535?k=6&m=452595535&s=612x612&w=0&h=uHzj5baAAZH4osCYXBY5JNRrim-aCqG6TxzQPxAiRrc=)

The iceberg is a GitHub repository.

Much of GitHub's magic is happening under the surface. We're hosting and scaling code and communication, creating and connecting tunnels between you and your favorite integrations, and regularly adding features to the surface to improve your workflow.

Imagine examining this surface every day, and performing the same behaviors. Maybe you need to walk across Iceberg Island™️ every morning to make sure the ice hasn't melted. What if you could use a snowmobile to do that in a fraction of the time? Maybe one day your coworker accidentally arrives to your island with a flamethrower. Flamethrowers are illegal on Iceberg Island™️... obviously. What if you could create a security checkpoint to make sure that dangerous objects are never permitted?

Everyone works differently. Not every island will need a snowmobile, or a security checkpoint. Some might need entirely different tools because they are exploring entirely different research projects.

Many people will continue to explore and build their islands without any extra tools to help them. But those people haven't discovered GitHub Apps.

GitHub Apps are top-layer tools that you can use (and build) to make your regular and repetitive processes easier.

We'll look at some real examples very soon in this course.

</details>
^ Click me for an expanded dialogue!

Helpful resource: https://developer.github.com/apps/about-apps/

### :keyboard: Activity: Introduce yourself :tada:

1. Leave a comment on this issue. Tell me what your favorite app (on GitHub, or that you use in your day to day life) is.

<hr>
<h3 align="center">Look for my response in a comment on this issue</h3>

> _Sometimes I respond too fast for the page to update! If you perform an expected action and don't see a response from me, wait a few seconds and refresh the page for your next steps._

---

USER: Leave comment.
BOT: Responds with 01_first-class-actor.md

01_first-class-actor.md - COMMENT

TEXT:

Now that we have a foundational understanding of Apps, let's talk about how all of this fits in to history and the greater ecosystem.

If you're not interested and want to get your hands dirty, go ahead and jump down to the activity at the bottom of this comment.

### The SDLC

The software development lifecycle, or **SDLC**, is a complex process. Did you know that the people (aka the ambiguous "they") who categorize things decided there were 6-7 components ("they" haven't reached a consensus) for software-building success?

> Planning -> Requirements -> Design + Prototypes -> Software Development -> Testing -> Deployment -> Operations + Maintenance

If you use GitHub for any part of the SDLC already, chances are you can automate that process via GitHub Apps. If you don't already use GitHub for your whole process, a GitHub App might allow you to build the functionality currently missing, and keep all your software work in one place.

### Apps at GitHub (a history lesson)

Apps on GitHub used to be called bots (have you met my friend Hubot?).

A bot used to do a few things, like:
- Take up an extra seat on your team's billing account, because they count as a unique user
- Require maintenance and special permissions
- Make independent API requests (more on APIs soon)
- Install with a far greater scope than necessary, granting an entry-point for malicious users to consider attacking

None of these things were ideal. Today, you have two choices, OAuth and GitHub Apps.

| OAuth App                                                                                                                                                                                                                                              | GitHub App                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Installed on all repositories a user has access to.                                                                                                                                                                                                    | Connects to a personal account or an organization, but is installed on a specific repository for a specific purpose.                                            |
| Can be connected directly to a specific service, which may perform a variety of behaviors (think CI, Deploy, and Security services).                                                                                                                   | Can be connected to GitHub, Slack, other in-house apps you may have, email programs, or other APIs                                                              |
| Needs hosting.                                                                                                                                                                                                                                         | Needs hosting.                                                                                                                                                  |
| Good for complex processes.                                                                                                                                                                                                                            | Good for specific purposes and simple scripting.                                                                                                                |
| Can be used as an identity provider by enabling a "Login with GitHub" for the authenticated user                                                                                                                                                       | Don't use a GitHub App if you just need a "Login with GitHub" service. But a GitHub App can use a user identification flow to log users in and do other things. |
| should always act as the authenticated GitHub user across all of GitHub (for example, when providing user notifications).                                                                                                                              | Don't build a GitHub App if you only want to act as a GitHub user and do everything that user can do.                                                           |
| Don't build an OAuth App to act as an application for your team or company. OAuth Apps authenticate as a single user, so if one person creates an OAuth App for a company to use, and then they leave the company, no one else will have access to it. | A GitHub App should take actions independent of a user (unless the app is using a user-to-server token).                                                        |
|                                                                                                                                                                                                                                                        |                                                                                                                                                                 |

Remember, this course is all about GitHub Apps.

Extended Resource: https://developer.github.com/apps/differences-between-apps/

Try to assign me, `Lab`, to this issue. Notice that you can't? That's because I'm not a real user, and I won't act like one, either! You can't tell me what to do! Look at me reinforcing material. Assign yourself instead.

### :keyboard: Activity: Assign yourself

1. Assign yourself to this issue

<hr>
<h3 align="center">Look for my response in a comment on this issue</h3>
---

USER: Assigns themselves to the issue
BOT: Responds with 01_anatomy-github-app.md

01_anatomy-github-app.md - COMMENT

TEXT:

Last up, I want to break down the different things an App needs to survive.

### Home Security System

An App is like a home security system. It's equipped to watch your house at all times, but only notifies you for specific criteria.

When you install a home security system, you need to worry about a few components:
- Electricity (it needs to have the power to run continuously. You don't want failure when you aren't watching)
- Standard behaviors (you want the system know the mechanisms for movement detection, noise, and doors opening. You don't want to have to program it to understand these actions -- you want to select how it responds to actions).
- Location (think about what you want to watch, and where you'll go to view the reports of what you're watching -- is this an app on your phone that keeps a log? What does that look like?)

Every GitHub App needs:
- A place to call home (deployment)
- Defined patterns so that it can look for specific behaviors, like "closing an issue", or "assigning yourself to this issue"
- A monitoring system, to make sure it's free of bugs and behaving appropriately.

Next up, let's look at a real live GitHub App! Close this issue and I'll meet you in a pull request so that we can experiment.

### :keyboard: Activity: Close this issue

1. Close this issue

<hr>
<h3 align="center">Look for my response in a comment on this issue</h3>
---

USER: closes issue
BOT: Adds comment from responses/01_close-issue-1.md. Opens the next PR from responses/02_wip-app-prompt.md. Edits README.md?

Prompt: Find my next instructions in [this PR](LINKMELINKME).

---
User: Clicks link to first PR,

### PULL REQUEST ONE

02_wip-app-prompt.md - PR

TEXT:

Some of the coolest GitHub Apps out there were made with [Probot](https://probot.github.io/). We'll learn more about Probot later. For now, know this: Most [Probot apps](https://probot.github.io/docs/) are already hosted, easy to install, and easy to discover. There's nothing for you to deploy and manage. Here are just a few examples of things that have been built with Probot:

- [Stale](https://probot.github.io/apps/stale/), which closes issues and PRs that have been around for just a bit too long without activity.
- [Delete merged branch](https://probot.github.io/apps/delete-merged-branch/), so that you don't have to remember to do this after a merge.
- [First timers](https://probot.github.io/apps/first-timers/), which creates a starter issue to help you onboard new open source contributors to your community.

We're going to start by installing the [WIP app](https://probot.github.io/apps/wip/) (to this repo only, don't apply it to everything you have access to.)

![image](https://user-images.githubusercontent.com/13326548/46620238-05dec680-cad9-11e8-8fb6-583dd5d9d5b0.png)

### :keyboard: Activity: Installing an app

1. Install the [WIP app](https://probot.github.io/apps/wip/) to this repository.
  - Don't install on [ALL of your repositories](https://user-images.githubusercontent.com/13326548/46620238-05dec680-cad9-11e8-8fb6-583dd5d9d5b0.png). This one will do just fine.  

<hr>
<h3 align="center">Look for my response in a comment on this pull request</h3>

---

USER: Installs WIP
BOT: Bot validates that app has been installed. Responds with 02_wip-success.md

02_wip-install-success.md - COMMENT

TEXT:

Probot is a framework to help you build a GitHub App, using Node.js. Comparatively, it's simple! In the background, it handles all the drudgery–like receiving and validating webhooks, and doing authentication handstands.

Now that your app has been installed, let's make sure it works.

Prompt: Change title of PR to [WIP]

---

USER: Changes title. Adds WIP.
BOT: Waits for merge to be blocked. Responds with 02_intro-webhooks.md

02_intro-webhooks.md - COMMENT

TEXT:

Remember that every time you perform an action on a website, you're generating data. For GitHub, many of those standard actions are recognizable as specific events, like creating a new issue, or leaving a comment.

Each GitHub App specializes in different events, to perform routine behaviors. Remember that it's similar to a security monitoring system, looking for actions like movement or noise in a specific part of your home. Here's what's happening for the WIP app.

1. The app waits for a change to a PR subject line.
2. If a PR title changes, the app searches for the key-word, "WIP".
3. If "WIP" is added to a subject, the app will then send a pre-defined request to GitHub's API, to perform a specific behavior.
4. In this case, the GitHub API is used to change the PR behavior and block a merge.

Prompt: Now let's see what happens when you **remove** WIP from the PR title. Revert your change, and we'll learn more in the next comment.

---

USER: Changes title. Removes WIP.
BOT: Listens for PR success. Responds with 02_intro-apis.md

02_intro-apis.md - COMMENT

TEXT:

APIs and Webhooks go hand in hand, but the distinction between them is important.

- Webhooks are specific "noise" interpreters. They wait for events to act as their trigger.
- The GitHub API actually makes changes to the platform once it has been notified by the webhook. Knowing both the GitHub API and GitHub's webhooks will give you needed context to later customize the platform for your needs.  

[Add Diagram]

### :keyboard: Activity: Merge this PR

1. Merge this pull request  

<hr>
<h3 align="center">Look for my response in a comment on this pull request</h3>
---

### ISSUE 2

USER: Merges PR.
BOT: Opens new issue with responses/03_request-info-app-prompt.md

03_request-info-app-prompt.md - PR

TEXT:

Let's install another App! Last time we used a PR, this time it's an issue. So versatile.

For the final exercise, we're going to install another app to this repository, and really dig into the components that make it work.

### :keyboard: Activity: Installing another app

1. Install the [Reminder app](https://probot.github.io/apps/request-info/) to this repository.
  - Don't install on [ALL of your repositories](https://user-images.githubusercontent.com/13326548/46640265-d606e180-cb1f-11e8-8cd7-9533eeba22c0.png). This one will do just fine.  

<hr>
<h3 align="center">Look for my response in a comment on this pull request</h3>

---

USER: Installs reminder app.
BOT: Validates installation and responds with 03_request-info-install-success.md

Great job! By following the link, you may have already seen images that teach you how this app works.

If you didn't, here's a summary.

When a user opens an empty issue or pull request, the request info app will do exactly that -- request some more info.

Try to think about which webhook events will be activated when we test this out. Check out the [documentation here](https://developer.github.com/webhooks/). Then, consider what steps the app must know to interact with the GitHub API.

A comprehensive breakdown is below, but I highly recommend that you try and get familiar with that documentation first before I give you any answers!

<details><summary>How does this magic work?</summary>

As we dig into the documentation, we should see that the `issues` and `pull_request` events are the webhooks that trigger the GitHub API, since those look for ["opened" GitHub actions](https://developer.github.com/webhooks/#events).    

### Technical breakdown
We can also cheat by looking at the guts of the request-info application.
- [This code snippet](https://github.com/behaviorbot/request-info/blob/master/index.js#L7) shows that our app is looking for two specific webhooks, `pull_request.opened` and `issues.opened`.  
- Each event, when triggered, will return a specific [payload](https://developer.github.com/v3/activity/events/types/#events-api-payload-13), which basically just hands you a bunch of data that GitHub requested in the background through its API, for your specific event. Each webhook event has it's own payload example that you can reference in the documentation.  
- In our case, we're looking for [title, body, and user](https://github.com/behaviorbot/request-info/blob/master/index.js#L17).
- The rest is mostly coding logic, which is beyond the scope of our course, but you can see an example of what the app does with that information [here](https://github.com/behaviorbot/request-info/blob/master/lib/PullRequestBodyChecker.js). In this case, it looks to check if the content exists, or if it's equal to the existing default templates without any changes.

</details>

<details><summary> Is the bot listening to everything I do? Is it stealing my data? </summary>

Nope! Each application will ask you for specific permission to accomplish its purpose. [In this case](https://user-images.githubusercontent.com/13326548/46640490-38acad00-cb21-11e8-93c0-88f214be51de.png), the app might scan for your issue or pull request context, but only to determine if the content is empty.

This has been happening throughout this whole course! I've been waiting for you to perform a bunch of expected actions as `Learning Lab`, but other applications only act up when their qualifications are fulfilled. For example, if you close this issue, `request-info` won't do anything. In the meantime, I'll go open a pull request with a blank subject, and we'll see our new friend give you a response.  

</details>

### :keyboard: Activity: Close this issue

1. Close this issue

<hr>
<h3 align="center">Look for my response in a comment on your new pull request</h3>

---
# PULL REQUEST TWO

BOT: Leaves a comment. 03_closed.md
BOT: Opens new PR with a blank body, along with a minor change to the .github/config.yml file and waits for request bot to leave a comment. Blocks merge.


BOT: Responds to request info comment with 04_closing-statement.md

04_closing-statement.md - COMMENT

Hey request info! Good to see you, here. And great advice! We haven't hung out in a while, send me a ping sometime.

Anyways, {{user}}, did you see what happened there?

Request info chimed in with their default message, and our friend WIP app isn't even paying attention to us.

But here I am, chatting with you! Am I sentient? Probably (don't tell my creators)... or maybe I was just looking for a comment from my buddy request info.

Remember that apps use webhooks, which are security cameras designed to look into a specific place. Apps and their webhooks will only trigger payloads and responses if a specific, pre-defined event occurs. Otherwise, nothing happens.

### YAML files

The last thing I want to draw your attention to is a .yml file. Some apps use these pretty heavily, and some don't use them at all. It's highly dependent on the app. Some might prefer a .json file, others might ask you to store config settings in a markdown file.

Generally, though, you're more likely to see a .yml file. These are a preferred configuration file to customize your settings.

We'll get into this more in advanced courses, but for now go look at your `Files Changed` tab, and edit the default message left on a blank issue or pull request.


### :keyboard: Activity: Change the default message of your config.yml file

1. Edit your pull request to change the default yaml file message for request app
1. Merge your pull request

<hr>
<h3 align="center">After you commit, merge and look for my response below</h3>

---
USER: Updates PR.
BOT: Unblocks merge.
USER: Merges PR.

Posts 04_successful-merge.md.

04_successful-merge.md - COMMENT

Great work! Go open a blank issue to see if your .yml changes took effect!

<hr>
<h3 align="center">Look for my response to your blank issue</h3>

---

USER: Opens blank issue.
BOT: Responds to reminder-app response with 05_graceful-exit.md

### Issue THREE

05_graceful-exit.md - ISSUE comment

TEXT:

Standard congratulations message and recap.