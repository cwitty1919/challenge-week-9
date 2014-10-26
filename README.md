# Name

Chris Wittenberg

# How many points have you earned?

86/100

(Make your own calculation and replace the number 0 with the points you think you've earned.)

# How many hours have you spent on this?

8

# When did you first start working on this week's learning challenges?

Thursday.

# What is the most difficult part about this week's challenge?

Getting MongoDB to work again. That alone took me about 2 hours.

# Show and tell (8 points)

## Link (2 points)

[title-of-the-article](http://link-to-an-article-about-machine-learning-use-for-big-data)

## Discuss how you may apply the machine learning technique mentioned in this article to another interesting problem (6 points).

fill-in-your-answer

# D3 IV

## Checkpoints (3 points x 4 = 12 points)

# 1. (3 points)

![image](C9Checkpoint1.png?raw=true)

[checkpoint](C9Checkpoint1.html)

# 2. (3 points)

![image](C9Checkpoint2.png?raw=true)

[checkpoint](C9Checkpoint2.html)

# 3. (3 points)

![image](C9Checkpoint3.png?raw=true)

[checkpoint](C9Checkpoint3.html)

# 4. (3 points)

![image](C9Checkpoint4.png?raw=true)

[checkpoint](C9Checkpoint4.html)

## Challenges (4 points x 3 = 12 points)

# 1. (4 points)

![image](C9Challenge1.png?raw=true)

# 2. (4 points)

![image](C9Challenge2.png?raw=true)

# 3. (4 points)

![image](C9Challenge3.png?raw=true)

[challenge3](C9Challenge3.html)



# MongoDB II

## Checkpoints (6 points x 2 = 12 points)

### 1 (6 points)

[mongodb js code collecting github events about our course](Mongoscript.js)

### 2 (6 points)

![terminal output of mongodb query](C9MCheckpoint1.png?raw=true)

## Challenge 1 (4 points x 10 = 40 points)

### 1 (4 points)

> db.github_repo_data.findOne({"actor.login": "doubleshow"});

![screenshot](C9MCheckpoint2.png?raw=true)

### 2 (4 points)

> db.github_repo_data.findOne({"actor.login": "doubleshow"}, {"actor": 1});

![screenshot](screenshot.png?raw=true)

### 3 (4 points)

> db.github_repo_data.findOne({"actor.login": {$in: ["doubleshow", "chrisbopp"]}}, {"actor.login": 1, "created_at": 1});

![screenshot](screenshot.png?raw=true)

### 4 (4 points)

> db.github_repo_data.find({'type': 'PushEvent'});

![screenshot](screenshot.png?raw=true)

### 5 (4 points)

> db.github_repo_data.findOne({'type': 'PushEvent'}, {"payload.commits.author.name": 1});

![screenshot](screenshot.png?raw=true)

### 6 (4 points)

> db.github_repo_data.findOne({"type": 'IssuesEvent'}, {payload: 1});

![screenshot](C9Challenge1.6.png?raw=true)

### 7 (4 points)

> db.github_repo_data.find({"type": "IssuesEvent"}, {"payload.issue.user.login": 1});

![screenshot](C9Challenge1.7.png?raw=true)

### 8 (4 points)

> db.github_repo_data.find({"type": 'IssuesEvent', "payload.issue.state": 'closed'}, {"payload.issue.id": 1, "payload.issue.state": 1});

![screenshot](C9Challenge1.8.png?raw=true)

### 9 (4 points)

> db.github_repo_data.find({"type": 'IssuesEvent', "payload.issue.state": 'open'}, {'payload.issue.user.login': 1, 'payload.issue.state': 1});

![screenshot](C9Challenge1.9.png?raw=true)

### 10 (4 points)

> db.github_repo_data.find({"type": 'IssuesEvest', "payload.issue.comments": {$gt: 0} }, {"payload.issue.user.login": 10, "payload.issue.comments": 10});

![screenshot](C9Challenge1.10.png?raw=true)


## Challenge 2 (8 points x 2 = 16 points) 

### 1 (8 points)

How many issues have I had?

> db.github_repo_data.count({"type": 'IssuesEvent', "payload.user.login": "cwitty1919"});

![screenshot](C9Challenge2.1.png?raw=true)

### 2 (8 points)

Which issues were the hardest to solve (had the most comments)?

> db.github_repo_data.find({"type": 'IssuesEvent'}, {"payload.issue.user.login": 10, "payload.issue.comments": 10}).sort("payload.issue.comments": -1);

![screenshot](screenshot.png?raw=true)
