# pHarmr

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```
### What is the name of your project?
```
pHarmr
```

### Describe your project!
pHarmr is a Hydroponics set up with extensive monitoring software.  With the help of pHarmr, users can monitor the health of their plants from miles away. In dangerous climates, where minimal interaction with the crops is paramount, pHarmr allows users to adjust their crops' environment without needing to interact (and possibly contaminate) the plants.  Additionally, pHarmr can teach people with little to no experience in growing their own food how to provide their plants with the healthiest environment.  In the future, harvesters could simply share scripts--including the basic environmental needs of a plant--to teach other users how to grow a particular plant.

### Who made this amazing Hack?
James Cunningham, Rishab Nayak, Jason Smith, Emily Vogelsperger

### What inspired you to make this?
James: I have a long time interest in agriculture and humanitarianism. This type of project allowed me to pursue a technically challenging project and one that could make a very real different in the lives of people in war zones and communities under siege throughout the world. I was lucky to have such fantastic team members and thoroughly enjoyed the experience of helping to develop these systems

Rishab: I joined the project as a web developer, with experience with progressive web apps and hardware interfacing. We got along well as a team, working together to solve the challenges we faced, starting from getting the Pi to communicate with the cloud, to writing async functions. Overall, I learnt a lot, and it was a great experience.

Jason: I sincerely believe that a new and efficient way to farm is needed to feed our growing population amidst an increasingly changing climate. The world needs new systems all around. I had this idea but not nearly enough skillsets to complete it. I put it out on our slack channel and a wonderfully amazing and diverse group of people with awesome ideas stepped up. I got to immerse myself in a world of backend DBs and learn some new and valuable coding skills.

Emily: I was inspired to join this project because I personally have no experience in hydroponics and I was interested in joining a very diverse group.  Each person in this group brought specific talents that were unique to the rest of the group.  It was incredibly rewarding to take an idea (of which I knew none of the background) and hear so many different points of view on how to tackle this problem.  Also, I got exposure to some interesting hardware, which I know nothing about.

### What does your project do?
pHarmr uses multiple sensors--pH, temperature, moisture--and feeds the real-time values through a Raspberry Pi
to a pub/sub, to which we subscribe, to extract data.  Our web application polls the server once every 30s for these values and displays them on the screen.  
If the user adjusts any of the sensors, the same path is used to communicate with the Pi.

### How did you build it?
Hardware: NFT hydro system with an LED grow light. Designed to be easily automated and require minimal maintenance.

Software: The web application was built with Vue, Firebase and Node.JS. We used Adafruit-IO as the cloud pub/sub server, which connects directly to the Raspberry Pi.

### What challenges did you face?
None of us had worked with a server that extensively before!  We all spent a considerable amount of time learning Google IoT, Cloud Firestore,
and Adafruit-IO in order to get this project up and running.  While learning this very complicated and extremely new skill
was daunting and frustrating at times, we are all ecstatic that we were able to accomplish something big we had never
done before.

Additionally, we all ran into lots of trouble while figuring out how to poll our server, send HTTP requests, and feed
these values into our web application. Again--these were all things we hadn't done before!  All-in-all, it was
an incredibly rewarding experience.

Finally, we had a lot of trouble actually displaying the values we got from out polled data.

### What accomplishments are you proud of?
Definitely receiving that first 200 response from our HTTP request (and it actually contained the correct values)!  
Another big accomplishment was setting up our Raspberry-Pi with the Adafruit server.  This is mainly because we spent
almost all of the beginning stages of the hackathon trying to learn Google Cloud IoT and Cloud Firestore and we were
glad to see some progress.
Finally figuring out how to poll the server on JavaScript--WITHOUT causing a stack overflow--was probably our greatest accomplishment of the night.  This was a problem we spent many hours on and asked many mentors for help with.  

### What did you learn while building this?
A lot of the software we were working with are extremely finicky.  It was very difficult to debug--especially since this
was all of our first times actually implementing this!  We all learned the importance of starting small first.  We
continually created small goals for the team which kept us from thinking too big, too fast, and in turn motivated us
because we were actually accomplishing things!

### What's next for your project?
We hope to fully flesh this project out so that it can be available for people in harsh climates, impoverished areas,
and those who simply enjoy growing their own food!

Instead of polling the server, we would love to find a way to rework the backend so that we can push the real-time data
to our web application.  Without monetary limitations, we could improve our hardware so that more sensors could be
added without overloading the Raspberry Pi.  In future implementations, pHarmr would allow users to create and share
their environment scripts with others, sharing their first-hand knowledge growing that particular plant.

### What did you build it with?
Our Front-End was built with Vue.js, which runs as a serverless app on Firebase. The IoT server is run by Adafruit.  Our sensors connect to the Pi, which in
turn sends the sensor information to Adafruit.  Using XMLHttpRequests, we are able to poll from the server to retrieve the sensor data.
