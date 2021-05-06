---
title: 'Frontend Static Setup'
date: '2021-05-06'
---

## Setup
As stated before, we will be using Next.JS and React as our main frontend framework. From previous implementation practice, we have the static signup page, and onboarding pages implemented. However, since the final design has been given to us this week, there are some tweeks that need to be accomplished. I'll be meeting with Muhammad (our other full stack developer) to work on the frontend together. The design team is currently experiencing finals week at their university so we won't be able to get the icons/colors/font/etc from them. Currently I've been creating the static pages from eye (so I can get the basic cards finished). So all font/placement is subject to change.

You can see our Trello Page which displays some attachements of my current work [here](https://trello.com/b/ClGHbaNR/accepted). You can see all of the current progress in the attachments on this Trello board.

## Description of Current Progress

#### Frontend
**Sign Up Page**

Sign up page has been tweaked to reflect the new page. I've been thinking of integrating with google signup, since usually everyone has a sign up page. This would help Walker with his database, and also it ensures that we don't have to create a secure sign up page from the ground up.

**Onboarding Page**

The onboarding process needs more information to develop. Currently, we have a step progress bar, but the final designs show a gradient bar which I'll implement in the future.

**Home Dashboard**

The static page with nothing in it is fully designed (and responsive).

**Messages**

The messages page is fully designed (and responsive), however we need to connect the Slack API and figure out where to host this. Currently AcceptED said their budget is $220 a year, which for now I'm unsure how much the current cost will be. Since we will be using PostgreSQL + Hosting the Next app + the other APIs (such as slack) this may go over budget.

**Profile Page**

The current cards with dynamic data has been added. Modals have been created aswell.

#### Backend

I'm creating a Heroku PostgreSQL database for my testing purposes only. (I won't overstep Walker's domain). However, with these current pages I have implemented I can try adding the dynamic data from the postgresql database. 


