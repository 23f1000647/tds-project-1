# tds-project-1

## Colab link
https://colab.research.google.com/drive/1i9YTj98DBqgfL9umJDKXlgfEjPRQzqpf?usp=sharing

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
| JavaScript | 6437        | 21.51         |  304326          |  47.28             |
| Python     | 3511        | 33.24         |  265850          |  75.72             |
| Go         | 1885        | 39.54         |  142291          |  75.49             |
| TypeScript | 1665        | 45.10         |  248075          |  148.99            |
| Ruby       | 1571        | 50.35         |  67237           |  42.80             |
| HTML       | 1506        | 55.38         |  37013           |  24.59             |
| Rust       | 1504        | 60.41         |  111104          |  73.87             |
| Java       | 1416        | 65.14         |  123045          |  86.90             |
| PHP        | 1033        | 68.59         |  48560           |  47.01             |
| Shell      | 1006        | 71.59         |  47039           |  46.76             |
| C++        | 969         | 75.19         |  83036           |  86.72             |
| C          | 868         | 78.09         |  40474           |  46.63             |

### Fact - 2
The correlation between followers and the number of public repositories is low, at just 0.016, indicating that the number of repositories has little impact on follower count. However, when examining the distribution of repositories in the top 80% most popular languages, we see that users with higher follower counts tend to have over 45% of their repositories in these top languages.

|     login      | # public_repos  | # followers | % top languages |
| -------------  | --------------- | ----------- | --------------- |
| tiangolo       | 73              | 26440       |  53.42          |
| schacon        | 215             | 13756       |  23.26          |   
| rwieruch       | 151             | 8618        |  49.67          |
| shuding        | 149             | 6755        |  48.99          |
| android10      | 79              | 6716        |  46.84          |
| marijnh        | 54              | 6523        |  72.22          |
| mxmnk          | 7               | 6460        |  71.43          |
| nikic          | 110             | 6232        |  47.27          |
| greenrobot     | 22              | 5506        |  72.73          |
| sebastianruder | 32              | 5466        |  51.13          |

## Recommendation
### Recommendation - 1
The table below highlights users with the highest number of public repositories, their follower counts, and their contributions to the top 80% of popular languages. This aligns with the low correlation observed between repository count and follower count. Based on this, developers concentrating on popular skill sets are likely to attract more followers than those simply increasing their repository count. While contributions in other languages are valuable, they appear to have less impact on attracting followers.

|     login      | # public_repos  | # followers | % top languages |
| -------------  | --------------- | ----------- | --------------- |
| blueyed        | 595             | 494         |  7.56           |
| derhuerst      | 582             | 766         |  15.29          |   
| ff6347         | 518             | 431         |  12.55          |
| wolfv          | 493             | 584         |  3.85           |
| mr-c           | 476             | 280         |  2.52           |
| janpio         | 471             | 654         |  2.34           |
| localheinz     | 452             | 618         |  13.27          |
| skade          | 420             | 708         |  8.33           |
| jpkrohling     | 393             | 387         |  8.14           |

### Recommendation - 2
Contributing to top niche skills results in more stargazers and watchers. Unique and specialized skills consistently attract a greater number of followers and watchers.

### Recommendation - 3
The overall trend for the top 5 to 7 programming languages shows that the number of repositories for each language rose consistently until 2016-2018. Since then, there has been a significant decrease in new repositories, indicating a decline in contributors in recent years. Increasing contributions in this area is anticipated to lead to a notable increase in followers and stargazers.
![](https://github.com/23f1000647/tds-project-1/blob/main/top_7_language_trend_per_year.png)
