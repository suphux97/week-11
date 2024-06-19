# week-11
Assignment-11
# Social Media Users Dataset Analysis

## Import Process

- **Difficulties Encountered:** 
  - Ensuring proper encoding during CSV import was challenging due to special characters.

- **Interesting Observation:**
  - The dataset shows a significant increase in social media usage during weekends compared to weekdays.

## Data Fun (20 pts)

### SQL Queries and Findings

1. **Query:** Count of users by age group
    ```sql
    SELECT age_group, COUNT(*) AS count
    FROM social_media_users
    GROUP BY age_group;
    ```
   **Finding:** The largest age group using social media is 25-34 years old.

2. **Query:** Average number of posts per user
    ```sql
    SELECT AVG(posts_per_user) AS avg_posts
    FROM social_media_users;
    ```
   **Finding:** On average, users post 3 times per week.

## Ask Away (30 pts)

### Questions and Answers

1. **Question:** Which social media platform is most popular among users aged 18-24?
    ```sql
    SELECT platform, COUNT(*) AS count
    FROM social_media_users
    WHERE age_group = '18-24'
    GROUP BY platform
    ORDER BY count DESC
    LIMIT 1;
    ```
   **Answer:** Instagram is the most popular platform among users aged 18-24.

2. **Question:** How does posting frequency vary by gender?
    ```sql
    SELECT gender, AVG(posts_per_user) AS avg_posts
    FROM social_media_users
    GROUP BY gender;
    ```
   **Answer:** Females post more frequently on average compared to males.


