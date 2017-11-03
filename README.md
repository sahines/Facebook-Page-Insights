# Facebook-Page-Insights
SM.Insights Web Api :
SM.Insights/api/Users : it contains all details about the user of our application
SM.Insights/api/Pages : it contains all details about user pages and roles which provide him the access to the page insights
SM.Insights/api/PageInsights : it contains all Facebook page insights which we’ve retrieve it with GraphApi I used 4 metrics between public and in public details : - Page_fans : Public : Total number of Likes //Public - Page_daily_adds : The number of new people who have liked your Page - page_posts-impressions : The number of impressions that came from all of your posts. - Page_total_views : The number of times a Page's profile has been viewed by logged in and logged out people.
PS: - Any valid access token can be used for publicly available metrics
- A user access token with read_insights permission can retrieve metrics for all pages owned by this user.
- A page access token with read_insights permission can retrieve all metrics for that Page.
SM.Insights/api/Dashboard: it contains all filters ( DateFrom, DateTo, ListOfPages and Metricname) which will be used to return metric data to plot.
SM.Insights/api/Dashboards/GetFanInsights: it returns total number of fans and net likes to the dashboard according to the Dashboard filters using the stored procedure “GetNbFans”.
SM.Insights/api/Dashboards/ GetViewInsights: it returns total number of people views to the page to the dashboard according to the Dashboard filters using the stored procedure “GetNbViews”.
SM.Insights/api/Dashboards/ GetPostInsights: it returns total number of impressions of all page posts to the dashboard according to the Dashboard filters using the stored procedure “GetNbImpression”.
SM.Insights/api/FBPagePosts: it contains all posts published on the user page with some details about them.
SM.Insights/api/FBPostInsights: it contains all Facebook Post Insights retrieved with Graph Api. I used those metrics : - post_impressions : The number of impressions for your Page post - post_engaged_users : The number of people who clicked anywhere in your posts - post_fan_reach : Post reach by people who like your page. - post_reactions_by_type_total : Total post reactions by type.
SM.Insights/api/Dashboards/ GetTotalPostInsights: it returns total number of all Post Insights (TotalPostsImpression, TotalPostsEngagement, TotalPostsReach) to the dashboard according to the user filters using the stored procedure “GetPostInsights”.
