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
## Interesting facts
### Fact - 1
Out of approximately 30,006 repositories created by 602 developers, covering 189 distinct programming languages, the top 12 languages alone account for nearly 80% of all repositories. This subset represents just about 6% of the total languages used. Additionally, there is a strong correlation between the number of repositories and stargazers, with the average stargazer count exceeding 40% for the top programming languages.

|   Language | Repo Count  | Cumulative %  | Total Stargazers | Average Stargazers |
| ---------- | ----------- | ------------- | ---------------- | ------------------ |
| JavaScript | 6467        | 21.55         |  304633          |  47.11             |
| Python     | 3513        | 33.26         |  265671          |  75.63             |
| Go         | 1883        | 39.54         |  142227          |  75.53             |
| TypeScript | 1696        | 45.19         |  248025          |  146.24            |
| Ruby       | 1571        | 50.42         |  67225           |  42.79             |
| HTML       | 1505        | 55.44         |  37013           |  24.59             |
| Rust       | 1505        | 60.45         |  110992          |  73.75             |
| Java       | 1418        | 65.18         |  123035          |  86.77             |
| PHP        | 1033        | 68.62         |  48544           |  46.99             |
| Shell      | 1013        | 72.00         |  47098           |  46.49             |
| C++        | 969         | 75.23         |  83991           |  86.68             |
| C          | 871         | 78.13         |  40460           |  46.45             |

### Fact - 2
The correlation between followers and the number of public repositories is low, at just 0.016, indicating that the number of repositories has little impact on follower count. However, when examining the distribution of repositories in the top 80% most popular languages, we see that users with higher follower counts tend to have over 45% of their repositories in these top languages.

|     login      | # public_repos  | # followers | % top languages |
| -------------  | --------------- | ----------- | --------------- |
| tiangolo       | 73              | 26424       |  53.42          |
| schacon        | 215             | 13755       |  23.26          |   
| rwieruch       | 151             | 8616        |  49.67          |
| shuding        | 149             | 6751        |  48.99          |
| android10      | 79              | 6714        |  46.84          |
| marijnh        | 54              | 6522        |  72.22          |
| mxmnk          | 7               | 6458        |  71.43          |
| nikic          | 110             | 6230        |  47.27          |
| greenrobot     | 32              | 5507        |  72.73          |
| sebastianruder | 22              | 5465        |  51.13          |

## Recommendation
### Recommendation - 1
The table below highlights users with the highest number of public repositories, their follower counts, and their contributions to the top 80% of popular languages. This aligns with the low correlation observed between repository count and follower count. Based on this, developers concentrating on popular skill sets are likely to attract more followers than those simply increasing their repository count. While contributions in other languages are valuable, they appear to have less impact on attracting followers.

|     login      | # public_repos  | # followers | % top languages |
| -------------  | --------------- | ----------- | --------------- |
| blueyed        | 595             | 494         |  7.56           |
| derhuerst      | 582             | 766         |  15.29          |   
| ff6347         | 518             | 431         |  12.55          |
| wolfv          | 492             | 583         |  3.86           |
| mr-c           | 474             | 280         |  2.53           |
| janpio         | 471             | 654         |  2.34           |
| localheinz     | 452             | 618         |  13.27          |
| skade          | 420             | 708         |  8.33           |
| jpkrohling     | 393             | 387         |  8.14           |

### Recommendation - 2
Contributing to top niche skills results in more stargazers and watchers. Unique and specialized skills consistently attract a greater number of followers and watchers.

### Recommendation - 3
The overall trend for the top 5 to 7 programming languages shows that the number of repositories for each language rose consistently until 2016-2018. Since then, there has been a significant decrease in new repositories, indicating a decline in contributors in recent years. Increasing contributions in this area is anticipated to lead to a notable increase in followers and stargazers.
![](https://github.com/23f1000647/tds-project-1/blob/main/top_7_language_trend_per_year.png)
