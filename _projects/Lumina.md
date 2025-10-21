---
layout: page
title: Lumina
description: Bluesky Follower Tracker
img: assets/img/code.jpg
# redirect: https://unsplash.com
importance: 3
category: work
---

<a href="https://github.com/AdaVoden/Lumina">Lumina</a> is a Bluesky follower tracker. Built to learn more about the AT Protocol and Bluesky, Lumina takes snapshots of your followers and notes changes from one snapshot to the next such as:
- New followers
- Accounts unfollowing yours
- Number of inactive accounts (Deleted or made inactive)
- Number of accounts that have never posted
- Number of accounts that have not posted in the last 31 days

It then displays this information on a small web dashboard make in Flask.

Those interested in their audience growth and engagement patterns over time would be interested in using this tool.

## Challenges

The largest hurdle was learning the SDK for the AT Protocol. The SDK, while well documented, took some getting used to and provided a barrier while I learned how it operated. Now, I find it quite lovely to work with. 

The second largest hurdle was creating a database with which to store the information that I needed. Re-learning SQL and learning new techniques in SQL to make comparisons lightning fast took a not inconsiderable amount of time. 

## What I learned

I refreshed my knowledge of writing code in Python and with SQL. I learned about Pydantic and Flask as well as refreshed my knowledge of basic web design. I am quite proud of being able to make a tiny web dashboard and have it successfully pull data from an API.

## TODO

- [ ] Redesign Lumina to use `async`, to improve performance.
- [ ] Fix bug where if a follower changers their account name it will count as a follow and unfollow
- [ ] Track post engagement over time
- [ ] Add way to snapshot periodically instead of manually