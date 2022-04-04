# HolidayMates - (Group) Project 3
 
In a team of three, with [@olliecal09](https://github.com/ollie09cal) and [@jvickers123](https://github.com/jvickers123), we wanted to build a full-stack application where you can connect with your mates, holidays and finally, your mates' holidays.
 
![HolidayMates - Main image](https://i.imgur.com/l5BXcRT.png)
 
 
 
## Deployment
 
The app is deployed on Heroku, [click here](https://holidaymates.herokuapp.com/) to try it out.
 
## Technologies used
 
**Client:** React, SASS, Chakra, React MapBox
 
**Server:** Node, Express, MongoDB, Mongoose
 
 
## Features
- Connection between friends through a code
- Map with your friends' and your holidays
- Search feature to explore all posted holidays and activities
- Posting holidays as virtual cards
- Add activities to holidays
 
 
## Brief
 
The brief for this project was to build in 10 days a full-stack application using **React**, **Node.js**, **Express** and **MongoDB**.
 
In our team, we decided to build an application where you can share your holidays and see your friends' holidays all in one place.
 
## Process and key dates
 
- Day 1 - Planning
- Day 2-3 - Building backend
- Day 4-6 - Building frontend and achieving MVP
- Day 7-8 - Styling with SASS
 
#### Day 1 - Planning
 
We started off the planning by thinking what could be our MVP and what features would be great if we had extra time in our hands during the project.
 
Once we were set in the scale of our product, we set a Trello Board to keep us on track and as a place to share any links, logos and imagery all in place.
 
![HolidayMates - trello](https://i.imgur.com/3jd8ouY.png)
 
Then we moved on to wireframing. The idea we had for our project was very user-focused that we wanted to focus on delivering a great and rich experience with many features.
Main one being sharing holidays which would show up on a map that you share with your friends and their holidays.
 
![HolidayMates - wireframe](https://i.imgur.com/TVv2tMN.jpg)
 
 
#### Day 2-3 Building backend
 
As our project required a lot of information stored in the backend, not only from each user but also all the connections and references between tables, we decided to pair-programme through our backend code.
This allowed us to have a clear idea of the data once we would move on to building components on the frontend separately.
 
To start, we coded our three models: holiday, holiday type and user. We approached each model with the idea of putting as many fields as we could think of so building new features in the future would be quick and easy.\
Below is our holiday schema, the main model for our project.
 
![HolidayMates - holiday model](https://i.imgur.com/voyPCjT.png)
 
One of our biggest struggles were creating a *delete* route for holidays as it not only had to delete the holiday but all the holiday types that were referenced.
We solved this by creating a *forEach* loop with a function inside that would find each holiday type added and delete them.
 
![Code snippet - forEach](https://i.imgur.com/VQdjNBG.png)
 
 
#### Day 4-6 Building frontend and achieving MVP
 
It was finally time to start frontend and use our own data. We started off choosing the pages each of us wanted to work on and what components we would use from Chakra style library.\
My choice was to take the responsibility of building authentication, home page and one of our main features called MatesMap that used **React MapBox** to display user's and their friends' holidays.
 
 
I started with the authentication because at the time it seemed like the hardest task and a lot of our features relied on having a logged in user so you'd be able to test that from the very beginning.
 
Next I moved on to my biggest task, MatesMap. As Jonny had started with another map feature earlier, I thought I was being clever and saving time by copying some of his code but quickly realised I needed to build it from scratch regardless as the data for the map needed to be handled differently to his map feature and the data for it.\
As much as it felt I wasted time, I was glad I had to do it from scratch as it gave me the opportunity to really delve deep into our own database and find creative ways to display the data.
 
One of the blockers was when I had to filter the data to only display friends' and the user's holidays as we had only built a route that gets all posted holidays.
The way I solved this was by using the user's data to find the friends that were connected with this user and then use that to get each friend's holidays. Often I would use *useEffect* to make sure I'd only make these requests when I needed to.
 
![code snippet - mates holidays](https://i.imgur.com/mmWuEsH.png)
 
![code snippet - mates holidays](https://i.imgur.com/DS7vOhL.png)
 
![code snippet - mates holidays](https://i.imgur.com/AQvKs3X.png)
 
Unfortunately, we didn't have time to add many extra features as we noticed we had a lot of pages to do in the first place and we wanted to prioritise making them work bug free as possible.
 
#### Day 7-8 Styling with SASS
 
Whilst we built our frontend we realised that our user would be more likely to use the application on their mobile versus their browser so we had to adapt the wireframe to a more mobile friendly design first. Fortunately we had been using **Chakra** throughout our components so any changes were quickly made.
 
We decided to switch to screen sharing for a moment so we could build one of our forms together. This helped us to have a guide to follow when it came to spreading our tasks to style the components we had built.
 
As the design was mobile-first we still wanted to keep the application responsive. This became tricky when I moved on to styling the MatesMap feature as the map was all you really needed but on the browser it really looked funny on it's own.\
I played around with backgrounds and size of the map but ended up adding a popup modal that would show up each time you open the MatesMap. The modal briefly told what the page was about without needing to have the description float around the map and possibly blocked some of the content.
 
## Bugs and Challenges
 
For me the biggest challenge during this project was when I was building the map feature displaying users’ and their friends’ holidays. To do this multiple trials and errors I ended up chaining useEffects to process the api requests one after the other to ensure all of the data was saved in states first before mapping and displaying the information.

## Wins
 
As this was the first time I had built a back end for a project, the greatest feeling came when we had finished our MVP and we were able to use our own database to register users and get the information we had stored ourselves. 
 
 
## Future add-ons
- Public/private feature for holidays
- Collaboration between friends: shared holidays
- More connections between users like chat rooms and private messaging
- Animations for better user experience
- Browsing features for users that haven't registered yet
 
## Key learnings
 
I really enjoyed our team dynamic and the way we communicated through this project, it really allowed us to have an open conversation of our struggles so everyone was able to learn from them even if you didn't have to deal with that code.
This is something that I'd love to bring with me to my first role as a developer.
 
On a more technical level, some of the great things I learned during this project was building maps and user authentication. Both were new topics at the time and I am glad I took the opportunity to code both as it really grew my confidence when they worked and they didn't feel like these scary big things of responsibility.
