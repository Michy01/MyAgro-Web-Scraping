# MyAgro-Web-Scraping

# Problem
A community of 500 members in Canada wants to launch a mentorship program within its peers. The program comes with the following requirements:
Mentors: Every female who is at least 40yo (>=40) and who joined the community before or on the 1st January 2004 (<= 2004-01-01).
Mentorees: Every member who is under 30yo (<=30) and who has a valid ID.

**Step 1:** Write a code that collects 500 records using this API: Random User Generator. In order to retrieve the right dataset of users, you need to make sure to use the ca nationality and the seed myagro.

**Step 2:** Create a class that will be used to create members objects, Every member object should have at least the following information:
- UUID (login UUID)
- Fullname (Firstname + Lastname)
- Email
- Age
- Gender
- Id (Value)
- Registered date (date and time)
- Address (Street + Postcode + City)

**Step 3:** Use the data retrieved in Step 1 to create a list of 500 members' objects

**Step 4:** Create a class that will be used to create mentorships object, every mentorship should have at least the following information:
UUID (randomly generated)
Mentor_uuid (UUID from the member object of the mentor)
Mentoree_uuid (UUID from the member object of the mentoree)

**Step 5:** Use the members' objects to generate mentorships following this model:
Every mentoree is assigned by order of registered date ( first joined is first assigned ). Mentorees will be assigned evenly to mentors following the registered date of the mentors.
For example: given the following input with 2 mentors and 5 mentorees
|Mentor name | Mentor registered date |
|------------|------------------------|
|Colin Matthews | 2001-03-18T11:00:29.000Z|
|Depp Williams | 2002-03-19T10:07:46.000Z|


|Mentoree name | Mentoree registered date|
|--------------|------------------------|
|John Davis | 2005-06-20T10:05:29.000Z|
|Patrick Kart | 2002-01-09T03:06:56.000Z|
| Emma Themp | 2010-02-07T05:04:23.000Z|
| Will Burt | 2011-04-08T06:02:12.000Z|
| Jack Riep | 2020-12-30T00:01:10.000Z|

 The mentorships that will be generated should be in this order:
- Patrick kart to Colin Matthews
- John Davis to Depp Williams
- Emma Themp to Colin Matthews
- Will Burt to Depp Williams
- Jack Riep to Colin Matthew

**Step 6:** Create 1 dataframe that will contain all 500 member objects generated in Step 3, the columns should match the member class properties.

**Step 7:** Create 1 dataframe that will contain all mentorships objects generated in Step 5, the columns should match the mentorship class properties.

**Step 8:** Create a function that will take as parameters the 2 dataframes created in Step 6&7 and return the median age of male mentorees that registered after 2010 (>=2010-01-01).

**Step 9:** Create a function that will take as parameters the 2 dataframes created in Step 6&7. Write a SQL query inside the function that will calculate the total number of mentorees (by gender) who are mentored by a member who is at least 60yo. Then print that number. To execute the query you could use a library such as pandasql.
# Hints

In Step 1: To double-check if your API call is correct, user 1 should be Ariana Denys and user 500 should be Alexis Li.
Few libraries you might need includes pandasql, pandas, uuid, requests, datetime. Generally speaking, you are free to use any library you feel appropriate or helpful.

Using dataclasses might help you save time.

Nice to have (Bonus)

These are not requirements but if you are interested in other ways to shine through this exercise here are a few nice to have:

In Step 9, rather than running a SQL query on the dataframes, you could create and initialize a Postgres or SQLite database, save the data as 2 different tables (mentorships and members), then create a function that will query the database and return the result.
Write unit tests to validate results.

Write a readme file to explain your solution in detail, outline the choices you made, what strategies or best practices you used, and why? any caveats to be aware of?
Language(s)

Python must be used for this exercise (+SQL in Step 9).
# Timeline

The exercise shouldn’t take more than 2-3 hours to complete but you can submit your solution up to 2 days after you received the exercise.
How to submit

Please send us via email your solution in a single ZIP.

