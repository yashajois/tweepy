# Introduction #

Here is some code snippets to help you out with using Tweepy.
Feel free to contribute your own snippets or improve the ones here!

|<b>Name</b>|<b>Description</b>|
|:----------|:-----------------|
|[#BasicAuth](#BasicAuth.md)|Using basic authentication|
|[#OAuth](#OAuth.md)|Using OAuth authentication|
|[#Pagination](#Pagination.md)|Performing pagination with the Cursor object|
|[#FollowAll](#FollowAll.md)|Script that follows back all followers|

## BasicAuth ##
```
auth = tweepy.BasicAuthHandler("username", "password")
api = tweepy.API(auth)
```

## OAuth ##
```
auth = tweepy.OAuthHandler("consumer_key", "consumer_secret")

# Redirect user to Twitter to authorize
redirect_user(auth.get_authorization_url())

# Get access token
auth.get_access_token("verifier_value")

# Construct the API instance
api = tweepy.API(auth)
```

## Pagination ##
```
# Iterate through all of the authenticated user's friends
for friend in tweepy.Cursor(api.friends).items():
    # Process the friend here
    process_friend(friend)

# Iterate through the first 200 statuses in the friends timeline
for status in tweepy.Cursor(api.friends_timeline).items(200):
    # Process the status here
    process_status(status)
```

## FollowAll ##
This snippet will follow every follower of the authenticated user.
```
for follower in tweepy.Cursor(api.followers).items():
    follower.follow()
```