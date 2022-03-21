
# HolidayMates - (Group) Project 3

In a team of three, with [@olliecal09](https://github.com/ollie09cal) and [@jvickers123](https://github.com/jvickers123), 
we wanted to build a full-stack application where you can connect with your mates, holidays and finally, your mates' holidays.

![HolidayMates - Main image](https://i.imgur.com/l5BXcRT.png)

## Deployment

To access this project, dowload the code and follow below command-line commands.


Change directory to *backend*:

```bash
  cd backend
```
Install all the dependencies:

```bash
  yarn
```
Run the server side:

```bash
  yarn serve
```
Open another terminal window,

Change directory to *client*:

```bash
  cd client
```
Install all the dependencies:
```bash
  yarn
```

Lastly, run below command to open the project on your browser:
```bash
  yarn start
```


## Technologies used

**Client:** React, SASS, Chakra, React MapBox

**Server:** Node, Express, MongoBDB, Mongoose


## Features
- Connection between friends through a code
- Map with your friends' and your holidays
- Search feature to explore all posted holidays and activities
- Posting holidays as virtual cards
- Add activities to holidays


## Brief

The brief for this project was to build a full-stack application using **React**, **Node.js**, **Express** and **MongoDB**.

In our team, we decided to build an application where you can share your holidays and see your friends' holidays all in one place. 
## Process and key dates

- Day 1 - Planning
- Day 2-3 - Building backend
- Day 4-6 - Builidng frontend and achieving MVP
- Day 7-8 - Styling with SASS

#### Day 1 - Planning

We started off the planning by thinking what could be our MVP and what features would be great if we had extra time in our hands during the project.

Once we were set in the scale of our product, we set a Trello Board to keep us on track and as a place to share any links, logos and imagery all in place.

![HolidayMates - trello](https://i.imgur.com/3jd8ouY.png)

Then we moved on to wireframing. The idea we had for our project was so user focused that we wanted to focus on delivering great and rich experince with many features.
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


#### Day 4-6 Builidng frontend and achieving MVP

It was finally time to start frontend and use our own data. We started off choosing the pages each of us wanted to work on and what components we would use from Chakra style library.\
My choice was to take the responsibility of building authentication, home page and one of our main features called MatesMap that used **React MapBox** to display user's and thier friends' holidays.


I started with the authentication because at the time it seemed like the hardest task and a lot of our features relied on having a logged in user so you'd be able to test that from the very beginning.

Next I moved on to my biggest task, MatesMap. As Jonny had started with another map feature earlier, I thought I was being clever and saving time by copying some of his code but quickly realized I needed to build it from scratch regardless as the data for the map needed to be handled differently to his map feature and the data for it.\
As much as it felt I wasted time, I was glad I had to do it from scratch as it gave me the opprotunity to really delve deep in to our own database and find creative ways to display the data.

One of the blockers was when I had to filter the data to only display friends' and the user's holidays as we had only built a route that gets all posted holidays.
The way I solved this was by using the user's data to find the friends that were connected with this user and then use that to get each friend's holidays. Often I would use *useEffect* to make sure I'd only make these requests when I needed.

![code snippet - mates holidays](https://i.imgur.com/mmWuEsH.png)

![code snippet - mates holidays](https://i.imgur.com/DS7vOhL.png)

![code snippet - mates holidays](https://i.imgur.com/AQvKs3X.png)

Unfortunately we didn't have time to add many extra features as we noticed we had a lot of pages to do in the first place and we wanted to prioritise
making them work bug free as possible.

#### Day 7-8 Styling with SASS

Whilst we built our frontend we realized that our user would more likely to use the application on their mobile versus their browser so we had to apapt the wireframe to a more mobile friendly
design first. Fortunately we had been using **Chakra** throughout our components so any changes were quickly made.

We decided switch to screen sharing for a moment so we could build one of our forms together. This helped us to have a guide to follow on when it came to spread our tasks to style the components we had built.

As the design was mobile-first we still wanted to keep the application responsive. This became tricky when I moved on to styling the MatesMap feature as the map was all you really needed but on the browser it really looked funny on it's own.\
I played around with backgrounds and size of the map but ended up adding a popup modal that would show up each time you open the MatesMap. The modal briefly told what the page was about without needing to have   
the description float around the map and possibly block someof the content.
## Key learnings

I really enjoyed our team dynamic and the way we communicated through this project, it really allowed us to have an open conversation of our struggles so everyone were able to learn from them even if you didn't have to deal with that code.
This is something that I'd love to bring with me to my first role as a developer.


But on more technical level, some of the great things I learned during this project was building maps and user authentication. Both were new topics at the time and I am glad I took the opportunity to code both as it really grew my confidence when they worked
and they didn't feel like these scary big things of responsibility.

## Future add-ons
- Public/private feature for holidays
- Collaboration between friends: shared holidays
- More connections between users like chatrooms and private messaging 
- Animations for better user experience
- Browsing features for users that haven't registered yet
