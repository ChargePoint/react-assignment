
# ChargePoint Frontend Assignment
---
![](https://imgs.xkcd.com/comics/self_description.png)

This repository holds the ChargePoint React assignment. In this project, you will find the description regarding the assignment for you to do. This assignment represents what we do on a day-to-day basis. We receive raw data from vehicles, store it in a database, and send it to browser apps via web socket.

---

## Getting Started
First of all, fork the repository at:

`https://github.com/ChargePoint/react-assignment`

Then open up your terminal and clone the forked repository

<sup>Replace [YOUR_USERNAME] with your name</sup>

`git clone https://github.com/[YOUR_USERNAME]/react-assignment.git`

Enter the directory

`cd react-assignment`

Install all the dependencies

`yarn`

Run the app

`yarn start`

---

## The Assignment
We have provided you with a starter kit that broadcasts vehicle data via a web socket. You can find the HTTP server on `src/server/app.js`, it's a bare minimum setup containing an express server to serve the HTML page and ws server that broadcasts raw data. What you need to build is a front-=end application that should look like below:

![](https://github.com/viriciti/frontend-assignment/raw/master/sketch.png)

The whole front-end application should be built with React, but you're free to choose how it's built and composed. Data that is needed to render all those components is provided via the web socket connection.

### Get Creative!
You can also extend the functionality for both the front-end and back-end. For example, making a more informative front-end, incident for vehicles that went too fast on the road (this can be done both in the front end and back end, double points for back end implementation ;) )

Please code in TypeScript and demonstrate your understanding of TypeScript. 
Bouns for CSS using styled-components - if you're not familiar with styled components, use whatever you're comfortable with. 
Make sure your UI is responsive and take some liberties with the UX (which only shows design for desktop screens).
Bonus for showing knowledge of Accessibility - ChargePoint driver team is committed to WCAG 2.2 compliance for everything we create, so, if you are familiar with what it takes to create Accessible UI, now's your time to show that off. 
Bonus for taking localization into account when displaying numbers, dates, etc. Feel free to hard-code the actual UI strings. We use i18next in ChargePoint, but you do not need to go that far in this project.

### The data
The websocket stream data should look like this:

```JS
{
  time: 1511512585495,
  energy: 85.14600000000002,
  gps: ["52.08940124511719","5.105764865875244"],
  odo: 5.381999999997788,
  speed: 12,
  soc: 88.00000000000007
}
```

* time - Unix timestamp of the moment the datapoint was recorder
* energy - Energy used in kWh
* gps - Latitude and longitude where the datapoint was recorded
* odo - The distance driven in km
* speed - The speed the vehicle was going in km/h
* soc - The state of charge (battery) of the vehicle in %

## Read up material
Looking to level up your knowledge and skills? These are some good articles/courses that you can check out.
* [Chartjs](https://www.chartjs.org/)
* [Node.js WebSocket](https://flaviocopes.com/node-websockets/)
### General
* Learn [Node.js and its modules](http://nodeschool.io/#workshoppers)

Good luck with the assignment!
