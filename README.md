# tds-project-1

## Scraping the data
Please refer TDS_Project_1.ipynb
Used python requests api to scrap the data from github. First generated the API token required for authentication and fetched the list of users in Berlin location who has more than 200 followers. Did this iteratively page by page by pulling 100 users data per page.
Once the users data is fetched, iterate over the users and fetch repositories for each user and pull the required information as per instruction

```ruby
[URL to fetch users from Berlin with 200+ followers]
https://api.github.com/search/users?q=location:Berlin+followers:>200&per_page={per_page}&page={page}

[URL to fetch individual user details]
https://api.github.com/users/{user_login}

[URL to fetch latest 500 repositories for given user]
https://api.github.com/users/{user_login}/repos?sort=pushed&per_page=500
```
