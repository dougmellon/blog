---
title: "Developing an open MLS API"
date: 2021-07-06T12:01:02-06:00 draft: false
---
*This is a living document for the project

### About the project

One of my priorities for the next year is to build a better understanding of API development. As is common with junior
developers, I continue to find myself in tutorial hell - repeating the same principles in different languages and
frameworks - which limits my ceiling of knowledge. To escape this cycle and build on my foundation, I have decided to
embark on a personal journey of developing an API that serves data concerning Major League Soccer.

Sports analytics has taken off in the past half-decade and access to data has become a limiting factor in terms of
exploration and study. The soccer world is dominated by a few companies charging thousands of dollars for access with no
pathway for students or those looking to dig in as a hobby. While these services are top-notch and provide exactly what
clubs around the world require, there is a space that can be filled for those not making front-office decisions.

I am hoping this project can help fill that void.

### Developing a database scheme

One of the first issues I have run into is a personal fault in that I keep trying to create a DB schema that is way too
complex. There is a lot of data available for parsing and, rather than start simple and work my way through, I keep
stopping and starting when I find new data to add. I think there are a few issues here but mainly, lack of experience
and my desire to provide as much information as possible.

To try and simply things, I am going to outline the data I want to begin with and work through everything before coming
back and adding more. There may be reasons as to why this is bad practice or others as to why it's good - but I'm
ignorant to both sides. So here we are.

###v1 data (postgres):

- Season table.
    
    - id: serial
    - year: smallint
    
- Teams table:

    - id: serial
    - name: varchar(255)
    
- Matches table:
    
    - id: serial
    - season_id: smallint (foreign key: seasons table id)
    - home_club_id: smallint (foreign key: teams table id)
    - away_club_id: smallint (foreign key: teams table id)
    - round: varchar(255)
    - date: varchar(255)
    - start_time: varchar(255)
    - home_xg: 
    

Note: Currently digging into the best way to solve this with the data format

