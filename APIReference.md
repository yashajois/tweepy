|<b>Method</b>|<b>Description</b>|
|:------------|:-----------------|
|<b>Timeline methods</b>|                  |
|[#public\_timeline](#public_timeline.md)|Returns the 20 most recent public statuses|
|[#home\_timeline](#home_timeline.md)|Returns the statuses of user and friends with retweets|
|[#friends\_timeline](#friends_timeline.md)|Returns the statuses of user and friends|
|[#user\_timeline](#user_timeline.md)|Returns the statuses of the user|
|[#mentions](#mentions.md)|Returns the mentions of the user|
|[#retweeted\_by\_me](#retweeted_by_me.md)|Returns the retweets posted by the user|
|[#retweeted\_to\_me](#retweeted_to_me.md)|Returns the retweets posted by the user's friends|
|[#retweets\_of\_me](#retweets_of_me.md)|Returns the tweets of the authenticated user that have been retweeted by others.|
|<b>Status methods</b>|                  |
|[#get\_status](#get_status.md)|Returns a single status specified by the ID|
|[#update\_status](#update_status.md)|Update the user's status (aka post a tweet)|
|[#destroy\_status](#destroy_status.md)|Destroy the status specified by the ID|
|[#retweet](#retweet.md)|Retweets a tweet  |
|[#retweets](#retweets.md)|Returns retweets of a specified tweet|
|<b>User methods</b>|                  |
|[#get\_user](#get_user.md)|Returns information about the specified user|
|[#me](#me.md)|Returns the authenticated user's information|
|[#friends](#friends.md)|Returns an user's friends|
|[#followers](#followers.md)|Returns an user's followers|
|[#search\_users](#search_users.md)|Performs an user search|
|<b>Direct Message methods</b>|                  |
|[#direct\_messages](#direct_messages.md)|Returns direct messages sent to the authenticating user|
|[#sent\_direct\_messages](#sent_direct_messages.md)|Returns direct messages sent by the authenticating user|
|[#send\_direct\_message](#send_direct_message.md)|Sends a new direct message to the specified user|
|[#destroy\_direct\_message](#destroy_direct_message.md)|Destroy a direct message|
|<b>Friendship methods</b>|                  |
|[#create\_friendship](#create_friendship.md)|Create a new friendship with the specified user|
|[#destroy\_friendship](#destroy_friendship.md)|Destroy a friendship with the specified user|
|[#exists\_friendship](#exists_friendship.md)|Checks if friendship exists between users|
|[#show\_friendship](#show_friendship.md)|Returns detailed information about a relationship between users|
|<b>Social Graph methods</b>|                  |
|[#friends\_ids](#friends_ids.md)|Returns array of IDs of users being followed by specified user|
|[#followers\_ids](#followers_ids.md)|Returns array of IDs of users following the specified user|
|<b>Account methods</b>|                  |
|[#verify\_credentials](#verify_credentials.md)|Verify supplied user credentials are valid|
|[#rate\_limit\_status](#rate_limit_status.md)|Query remaining API requests available|
|[#set\_delivery\_device](#set_delivery_device.md)|Set which device to deliver updates to for authenticating user|
|[#update\_profile\_colors](#update_profile_colors.md)|Update profile color scheme|
|[#update\_profile\_image](#update_profile_image.md)|Update authenticating user's profile image|
|[#update\_profile\_background\_image](#update_profile_background_image.md)|Update authenticating user's background image|
|[#update\_profile](#update_profile.md)|Update authenticating user's profile|
|<b>Favorite methods</b>|                  |
|[#favorites](#favorites.md)|Returns the favorite statuses for an user|
|[#create\_favorite](#create_favorite.md)|Creates a new favorite status|
|[#destroy\_favorite](#destroy_favorite.md)|Destroy a favorite|
|<b>Notification methods</b>|                  |
|[#enable\_notifications](#enable_notifications.md)|Enables device notifications|
|[#disable\_notifications](#disable_notifications.md)|Disables device notifications|
|<b>Block methods</b>|                  |
|[#create\_block](#create_block.md)|Blocks the specified user|
|[#destroy\_block](#destroy_block.md)|Un-blocks the specified user|
|[#exists\_block](#exists_block.md)|Checks if an user is blocked|
|[#blocks](#blocks.md)|Returns array of users that are blocked|
|[#blocks\_ids](#blocks_ids.md)|Returns array of user IDs that are blocked|
|<b>Spam Reporting methods</b>|                  |
|[#report\_spam](#report_spam.md)|Report an user as spammer|
|<b>Saved Searches methods</b>|                  |
|[#saved\_searches](#saved_searches.md)|Returns the authenticated user's saved search queries.|
|[#get\_saved\_search](#get_saved_search.md)|Retrieve the data for a saved search|
|[#create\_saved\_search](#create_saved_search.md)|Creates a saved search|
|[#destroy\_saved\_search](#destroy_saved_search.md)|Destroys a saved search|
|<b>Help methods</b>|                  |
|[#test](#test.md)|Invoke the test method|
|<b>Search API methods</b>|                  |
|[#search](#search.md)|Execute a search query|
|[#trends](#trends.md)|Returns the top ten topics that are currently trending on Twitter|
|[#trends\_current](#trends_current.md)|Returns the current top 10 trending topics on Twitter.|
|[#trends\_daily](#trends_daily.md)|Returns the top 20 trending topics for each hour in a given day.|
|[#trends\_weekly](#trends_weekly.md)|Returns the top 30 trending topics for each day in a given week.|
|<b>List methods</b>|                  |
|[#create\_list](#create_list.md)|Creates a new list for the authenticated user.|
|[#destroy\_list](#destroy_list.md)|Deletes the specified list.|
|[#update\_list](#update_list.md)|Updates the specified list.|
|[#lists](#lists.md)|List the lists of the specified user.|
|[#lists\_memberships](#lists_memberships.md)|List the lists the specified user has been added to.|
|[#lists\_subscriptions](#lists_subscriptions.md)|List the lists the specified user follows.|
|[#list\_timeline](#list_timeline.md)|Show tweet timeline for members of the specified list.|
|[#get\_list](#get_list.md)|Show the specified list.|
|[#add\_list\_member](#add_list_member.md)|Add a member to a list.|
|[#remove\_list\_member](#remove_list_member.md)|Removes the specified member from the list.|
|[#list\_members](#list_members.md)|Returns the members of the specified list.|
|[#is\_list\_member](#is_list_member.md)|Check if a user is a member of the specified list.|
|[#subscribe\_list](#subscribe_list.md)|Make the authenticated user follow the specified list.|
|[#unsubscribe\_list](#unsubscribe_list.md)|Unsubscribes the authenticated user form the specified list.|
|[#list\_subscribers](#list_subscribers.md)|Returns the subscribers of the specified list.|
|[#is\_subscribed\_list](#is_subscribed_list.md)|Check if the specified user is a subscriber of the specified list.|

## public\_timeline ##
Returns the 20 most recent statuses from non-protected users who
have set a custom user icon. The public timeline is cached for 60
seconds so requesting it more often than that is a waste of resources.

<b>Parameters:</b> None

<b>Returns:</b> list of Status objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses-public_timeline)

## home\_timeline ##
Returns the 20 most recent statuses, including retweets, posted
by the authenticating user and that user's friends. This is the
equivalent of /timeline/home on the Web.

<b>Parameters:</b> since\_id, max\_id, count, page

<b>Returns:</b> list of Status objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses-home_timeline)

## friends\_timeline ##
Returns the 20 most recent statuses posted by the
authenticating user and that user's friends.

<b>Parameters:</b> since\_id, max\_id, count, page

<b>Returns:</b> list of Status objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses-friends_timeline)

## user\_timeline ##
Returns the 20 most recent statuses posted from the
authenticating user. It's also possible to request another
user's timeline via the id parameter.

<b>Parameters:</b> (id or user\_id or screen\_name), since\_id, max\_id, count, page

<b>Returns:</b> list of Status objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses-user_timeline)

## mentions ##
Returns the 20 most recent mentions (status containing @username)
for the authenticating user.

<b>Parameters:</b> since\_id, max\_id, count, page

<b>Returns:</b> list of Status objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses-mentions)

## retweeted\_by\_me ##
Returns the 20 most recent retweets posted by the authenticating user.

<b>Parameters:</b> since\_id, max\_id, count, page

<b>Returns:</b> list of Status objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses-retweeted_by_me)

## retweeted\_to\_me ##
Returns the 20 most recent retweets posted by the authenticating user's friends.

<b>Parameters:</b> since\_id, max\_id, count, page

<b>Returns:</b> list of Status objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses-retweeted_to_me)

## retweets\_of\_me ##
Returns the 20 most recent tweets of the authenticated user that have been retweeted by others.

<b>Parameters:</b> since\_id, max\_id, count, page

<b>Returns:</b> list of Status objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses-retweets_of_me)

## get\_status ##
Returns a single status specified by the ID parameter.

<b>Parameters:</b> id (Required)

<b>Returns:</b> Status object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses%C2%A0show)

## update\_status ##
Update the authenticated user's status. Statuses that are duplicates or too long will be silently ignored.

<b>Parameters:</b> status (Required), in\_reply\_to\_status\_id, lat, long

<b>Returns:</b> Status object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses%C2%A0update)

## destroy\_status ##
Destroy the status specified by the id parameter. The authenticated user must be the author of the status to destroy.

<b>Parameters:</b> id (Required)

<b>Returns:</b> Status object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses%C2%A0destroy)

## retweet ##
Retweets a tweet. Requires the id of the tweet you are retweeting.

<b>Parameters:</b> id (Required)

<b>Returns:</b> Status object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses-retweet)

## retweets ##
Returns up to 100 of the first retweets of the given tweet.

<b>Parameters:</b> id (Required), count

<b>Returns:</b> list of Status objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses-retweets)

## get\_user ##
Returns information about the specified user.

<b>Parameters:</b> id OR screen\_name OR id (One of these is Required)

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-users%C2%A0show)

## me ##
Returns the authenticated user's information.

<b>Parameters:</b> None

<b>Returns:</b> User object

## friends ##
Returns an user's friends ordered in which they were added 100 at a time. If no user is specified by id/screen name, it defaults to the authenticated user.

<b>Parameters:</b> id OR screen\_name OR user\_id, cursor

<b>Returns:</b> list of User objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses%C2%A0friends)

## followers ##
Returns an user's followers ordered in which they were added 100 at a time. If no user is specified by id/screen name, it defaults to the authenticated user.

<b>Parameters:</b> id OR screen\_name OR user\_id, cursor

<b>Returns:</b> list of User objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-statuses%C2%A0followers)

## search\_users ##
Run a search for users similar to Find People button on Twitter.com; the same results returned by people search on Twitter.com will be returned by using this API (about being listed in the People Search).  It is only possible to retrieve the first 1000 matches from this API.

<b>Parameters:</b> q (Required. The query.), per\_page, page

<b>Returns:</b> list of User objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-users-search)

## direct\_messages ##
Returns direct messages sent to the authenticating user.

<b>Parameters:</b> since\_id, max\_id, count, page

<b>Returns:</b> list of DirectMessage objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-direct_messages)

## sent\_direct\_messages ##
Returns direct messages sent by the authenticating user.

<b>Parameters:</b> since\_id, max\_id, count, page

<b>Returns:</b> list of DirectMessage objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-direct_messages%C2%A0sent)

## send\_direct\_message ##
Sends a new direct message to the specified user from the authenticating user.

<b>Parameters:</b> user (Required), text (Required)

<b>Returns:</b> DirectMessage object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-direct_messages%C2%A0new)

## destroy\_direct\_message ##
Destroy a direct message. Authenticating user must be the recipient of the direct message.

<b>Parameters:</b> id (Required)

<b>Returns:</b> DirectMessage object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-direct_messages%C2%A0destroy)

## create\_friendship ##
Create a new friendship with the specified user (aka follow).

<b>Parameters:</b> id OR screen\_name OR user\_id (One of these is required)

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-friendships%C2%A0create)

## destroy\_friendship ##
Destroy a friendship with the specified user (aka unfollow).

<b>Parameters:</b> id OR screen\_name OR user\_id (One of these is required)

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-friendships%C2%A0destroy)

## exists\_friendship ##
Checks if a friendship exists between two users. Will return True if user\_a follows user\_b, otherwise False.

<b>Parameters:</b> user\_a (Required), user\_b (Required)

<b>Returns:</b> True/False

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-friendships-exists)

## show\_friendship ##
Returns detailed information about the relationship between two users.

<b>Parameters:</b> source\_id OR source\_screen\_name (One of these is required), target\_id OR target\_screen\_name (One of these is required)

<b>Returns:</b> Friendship object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-friendships-show)

## friends\_ids ##
Returns an array containing the IDs of users being followed by the specified user.

<b>Parameters:</b> id OR screen\_name OR user\_id (One of these is required)

<b>Returns:</b> list of Integers

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-friends%C2%A0ids)

## followers\_ids ##
Returns an array containing the IDs of users following the specified user.

<b>Parameters:</b> id OR screen\_name OR user\_id (One of these is required)

<b>Returns:</b> list of Integers

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-followers%C2%A0ids)

## verify\_credentials ##
Verify the supplied user credentials are valid.

<b>Parameters:</b> None

<b>Returns:</b> User object if credentials are valid, otherwise False

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-account%C2%A0verify_credentials)

## rate\_limit\_status ##
Returns the remaining number of API requests available to the requesting user before the API limit is reached for the current hour. Calls to rate\_limit\_status do not count against the rate limit.  If authentication credentials are provided, the rate limit status for the authenticating user is returned.  Otherwise, the rate limit status for the requester's IP address is returned.

<b>Parameters:</b> None

<b>Returns:</b> JSON object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-account%C2%A0rate_limit_status)

## set\_delivery\_device ##
Sets which device Twitter delivers updates to for the authenticating user.  Sending "none" as the device parameter will disable SMS updates.

<b>Parameters:</b> device (Required. Valid values: sms OR none)

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-account%C2%A0update_delivery_device)

## update\_profile\_colors ##
Sets one or more hex values that control the color scheme of the authenticating user's profile page on twitter.com.

<b>Parameters:</b> profile\_background\_color, profile\_text\_color, profile\_link\_color, profile\_sidebar\_fill\_color, profile\_sidebar\_border\_color

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-account%C2%A0update_profile_colors)

## update\_profile\_image ##
Update the authenticating user's profile image. Valid formats: GIF, JPG, or PNG

<b>Parameters:</b> filename (Path to image file. Required)

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-account%C2%A0update_profile_image)

## update\_profile\_background\_image ##
Update authenticating user's background image. Valid formats: GIF, JPG, or PNG

<b>Parameters:</b> filename (Path to image file. Required), tile

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-account%C2%A0update_profile_background_image)

## update\_profile ##
Sets values that users are able to set under the "Account" tab of their settings page.

<b>Parameters:</b> name, url, location, description

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-account%C2%A0update_profile)

## favorites ##
Returns the favorite statuses for the authenticating user or user specified by the ID parameter.

<b>Parameters:</b> id, page

<b>Returns:</b> list of Status objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-favorites)

## create\_favorite ##
Favorites the status specified in the ID parameter as the authenticating user.

<b>Parameters:</b> id (Required)

<b>Returns:</b> Status object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-favorites%C2%A0create)

## destroy\_favorite ##
Un-favorites the status specified in the ID parameter as the authenticating user.

<b>Parameters:</b> id (Required)

<b>Returns:</b> Status object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-favorites%C2%A0destroy)

## enable\_notifications ##
Enables device notifications for updates from the specified user.

<b>Parameters:</b> id OR screen\_name OR user\_id (One of these is required)

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-notifications%C2%A0follow)

## disable\_notifications ##
Disables notifications for updates from the specified user to the authenticating user.

<b>Parameters:</b> id OR screen\_name OR user\_id (One of these is required)

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-notifications%C2%A0leave)

## create\_block ##
Blocks the user specified in the ID parameter as the authenticating user. Destroys a friendship to the blocked user if it exists.

<b>Parameters:</b> id OR screen\_name OR user\_id (One of these is required)

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-blocks%C2%A0create)

## destroy\_block ##
Un-blocks the user specified in the ID parameter for the authenticating user.

<b>Parameters:</b> id OR screen\_name OR user\_id (One of these is required)

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-blocks%C2%A0destroy)

## exists\_block ##
Checks if the authenticated user is blocking the specified user.

<b>Parameters:</b> id OR screen\_name OR user\_id (One of these is required)

<b>Returns:</b> True/False

[API Wiki](http://apiwiki.twitter.com/Twitter+REST+API+Method%3A-blocks-exists)

## blocks ##
Returns an array of user objects that the authenticating user is blocking.

<b>Parameters:</b> page

<b>Returns:</b> list of User objects

[API Wiki](http://apiwiki.twitter.com/Twitter+REST+API+Method%3A-blocks-blocking)

## blocks\_ids ##
Returns an array of numeric user ids the authenticating user is blocking.

<b>Parameters:</b> None

<b>Returns:</b> list of Integers

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-blocks-blocking-ids)

## report\_spam ##
The user specified in the id is blocked by the authenticated user and reported as a spammer.

<b>Parameters:</b> id OR screen\_name OR user\_id (One of these is required)

<b>Returns:</b> User object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-report_spam)

## saved\_searches ##
Returns the authenticated user's saved search queries.

<b>Parameters:</b> None

<b>Returns:</b> list of SavedSearch objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-saved_searches)

## get\_saved\_search ##
Retrieve the data for a saved search owned by the authenticating user specified by the given id.

<b>Parameters:</b> id (Required)

<b>Returns:</b> SavedSearch object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-saved_searches-show)

## create\_saved\_search ##
Creates a saved search for the authenticated user.

<b>Parameters:</b> query (Required)

<b>Returns:</b> SavedSearch object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-saved_searches-create)

## destroy\_saved\_search ##
Destroys a saved search for the authenticated user. The search specified by id must be owned by the authenticating user.

<b>Parameters:</b> id (Required)

<b>Returns:</b> SavedSearch object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-saved_searches-destroy)

## test ##
Invokes the test method in the Twitter API. Return True if successful, otherwise False.

<b>Parameters:</b> None

<b>Returns:</b> True/False

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-help%C2%A0test)

## search ##
Returns tweets that match a specified query.

<b>Parameters:</b> q (Required. The search query string.), lang, locale, rpp, page, since\_id, geocode, show\_user

<b>Returns:</b> list of SearchResult objects

[API Wiki](http://apiwiki.twitter.com/Twitter-Search-API-Method%3A-search)

## trends ##
Returns the top ten topics that are currently trending on Twitter.  The response includes the time of the request, the name of each trend, and the url to the Twitter Search results page for that topic.

<b>Parameters:</b> None

<b>Returns:</b> JSON object

[API Wiki](http://apiwiki.twitter.com/Twitter-Search-API-Method%3A-trends)

## trends\_current ##
Returns the current top 10 trending topics on Twitter.  The response includes the time of the request, the name of each trending topic, and query used on Twitter Search results page for that topic.

<b>Parameters:</b> exclude

<b>Returns:</b> JSON object

[API Wiki](http://apiwiki.twitter.com/Twitter-Search-API-Method%3A-trends-current)

## trends\_daily ##
Returns the top 20 trending topics for each hour in a given day.

<b>Parameters:</b> date, exclude

<b>Returns:</b> JSON object

[API Wiki](http://apiwiki.twitter.com/Twitter-Search-API-Method%3A-trends-daily)

## trends\_weekly ##
Returns the top 30 trending topics for each day in a given week.

<b>Parameters:</b> date, exclude

<b>Returns:</b> JSON object

[API Wiki](http://apiwiki.twitter.com/Twitter-Search-API-Method%3A-trends-weekly)

## create\_list ##
Creates a new list for the authenticated user. Accounts are limited to 20 lists.

<b>Parameters:</b> name (Required), mode (public/private default: public)

<b>Returns:</b> List object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-POST-lists)

## destroy\_list ##
Deletes the specified list. Must be owned by the authenticated user.

<b>Parameters:</b> slug (Required. May also be the list ID.)

<b>Returns:</b> List object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-DELETE-list-id)

## update\_list ##
Updates the specified list. **Note: this current throws a 500. Twitter is looking into the issue.**

<b>Parameters:</b> slug (Required. May also be the list ID.), name, mode (public/private)

<b>Returns:</b> List object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-POST-lists-id)

## lists ##
List the lists of the specified user. Private lists will be included if the authenticated users is the same as the user who's lists are being returned.

<b>Parameters:</b> cursor

<b>Returns:</b> list of List objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-GET-lists)

## lists\_memberships ##
List the lists the specified user has been added to.

<b>Parameters:</b> cursor

<b>Returns:</b> list of List objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-GET-list-memberships)

## lists\_subscriptions ##
List the lists the specified user follows.

<b>Parameters:</b> cursor

<b>Returns:</b> list of List objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-GET-list-subscriptions)

## list\_timeline ##
Show tweet timeline for members of the specified list.

<b>Parameters:</b> owner (Required.), slug (Required. May also be the list ID.), since\_id, max\_id, count, page

<b>Returns:</b> list of Status objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-GET-list-statuses)

## get\_list ##
Show the specified list. Private lists will only be shown if the authenticated user owns the specified list.

<b>Parameters:</b> owner (Required.), slug (Required. May also be the list ID.)

<b>Returns:</b> List object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-GET-list-id)

## add\_list\_member ##
Add a member to a list. The authenticated user must own the list to be able to add members to it. Lists are limited to having 500 members.

<b>Parameters:</b> slug (Required. May also be the list ID.), id (Required. ID of user to add.)

<b>Returns:</b> List object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-POST-list-members)

## remove\_list\_member ##
Removes the specified member from the list. The authenticated user must be the list's owner to remove members from the list.

<b>Parameters:</b> slug (Required. May also be the list ID.), id (Required. ID of user to remove.)

<b>Returns:</b> List object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-DELETE-list-members)

## list\_members ##
Returns the members of the specified list.

<b>Parameters:</b> owner (Required.), slug (Required. May also be list ID.), cursor

<b>Returns:</b> list of User objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-GET-list-members)

## is\_list\_member ##
Check if a user is a member of the specified list.

<b>Parameters:</b> owner (Required.), slug (Required. May also be list ID.), id (Required. User to check if is a member on the list or not.)

<b>Returns:</b> User object if user is a member of list, otherwise False.

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-GET-list-members-id)

## subscribe\_list ##
Make the authenticated user follow the specified list.

<b>Parameters:</b> owner (Required.), slug (Required. May also be list ID.)

<b>Returns:</b> List object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-POST-list-subscribers)
http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-GET-list-subscribers-id
## unsubscribe\_list ##
Unsubscribes the authenticated user form the specified list.

<b>Parameters:</b> owner (Required.), slug (Required. May also be list ID.)

<b>Returns:</b> List object

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-DELETE-list-subscribers)

## list\_subscribers ##
Returns the subscribers of the specified list.

<b>Parameters:</b> owner (Required.), slug (Required. May also be list ID.), cursor

<b>Returns:</b> list of User objects

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-GET-list-subscribers)

## is\_subscribed\_list ##
Check if the specified user is a subscriber of the specified list.

<b>Parameters:</b> owner (Required.), slug (Required. May also be list ID.), id (Required. User to check if subscribed to the list.)

<b>Returns:</b> User object if user is subscribed to the list, otherwise False.

[API Wiki](http://apiwiki.twitter.com/Twitter-REST-API-Method%3A-GET-list-subscribers-id)