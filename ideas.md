# Purpose
- A web ui where one can create and setup a tournament and allow other to see.
- The purpose of this project was for me and others to learn about working on a group project and further our programming skills.
- This document will be very rambly since it is discussion for myself and the people I have talked about this project with.
- If you want to help and discuss, lmk by creating a pool request with your discord tag.

# Ramble
Some design goals:

-	Want to do lots of stuff on the client side for the sake of the main server acting as a REST api.
-		This would allow for us to more easily replace the GUI if we decide we hate how it looks.
-	Want to try pass most of the data as JSON.
-	Might be interesing to use WebAssebly for the learning's sake.

Starting point:

-	To Start off we will make an admin UI to log into and to manage tournaments.

When a pool is created, bot only does it become visible to the plublic
we also are able to take the pool sheet data insert it into a prelayed out PDF template for printing.


Backend python for inserting data into the pdf and sending it back.
	We probably want to incorperate caching

Fontedn WebAssembly or Javascript UI for being able to fill out pool sheets.

I Think for the backend we use flask (python based)


Alternative to flask
https://docs.aiohttp.org/en/stable/

For printing pretty forms
https://medium.com/@vivsvaan/filling-editable-pdf-in-python-76712c3ce99


Pool Sheet Data

-	Tournament
-	Competition
-	Round
-	Pool Number
-	Strip Number
-	Referee
-
-	Array Of People
-		Club
-		Name
-		Array of Touches Scored Against Players
-			Of of the elements should be 0 since you cannot fence yourself.
-
-	Notes String


Questions

-	How can we do proper databasing?
-	Try Use the USFA PDF template and make modifications to it
-	or just make an html we can instert stuff in with javascript?
-	How difficult would it be python vs php vs node etc. (Show My Thing)

The site page with consists of these tabs
-	Home
-	Past Events
-	Participants
-	Pool Assignments
-	Pool Results
-	Tableu Assignments
-	Event Results
-	Autoscroll Mode For Displays (Not sure How we could implement it)

Admin page consists of the following

-	Login Page
-	Create Event
-	Add Participants
-	Generate Pools
-	Enter/Calculate Pool Results
-	Generate Tableu
-	Enter Tableu Results
-	End Event

Login Page

-	Asks for username and password.
-	Upon access being granted, some sort of session cookie should be made.


Create Event

-	This provides a form for a user to fill out with the following information
-		Event name, Date, Other, Stuff, i, Cannot, Think, Of
-	A random event id might also want to be made.


Add Participents

-	A form for adding one or more participants and should ask for the following information
-		Name, Club, Checkboxs for events, other
-	We may want to try include a way to interface and import using the AskFRED api, but we need to pay attention to terms of use.


Generate Pools

-	Should prompt for how many strips are avalible? and prompt for maximum pool size (7 default)
-	Generates pools based off of the guidelines found here
-		https://www.fencingparents.org/nationalcompetitions/2018/5/2/how-seeding-pools-and-direct-elimination-rounds-are-setup-in-fencing-tournaments
-		We may need to take extra steps to prevent pools of too many people of the same club


Enter/Calculate Pool Results

-	Should now a list of pools the user can select to input info for.
-	Should have a calculate results button that calculates the results and sends them to the server


Generate Tableu

-	Once all pools have been finished. It should rank everyone and generate a tableu. 
-	This could probably be handeled server side.


Enter Tableu Results

-	Drop down box to select the winner of bout and upload to server.


End Event

-	Rank everyone and archive the data. 


Past Events

-	This page will return a list of past events and their dates. This can be handled on the server or client side.


Participants

-	This page should return a list of participants for the ongoing event. This can be handed on the server side or client side.
-	The participants should be listed in alphabetical order by last name and also list the following information
-		Name, Club, Rating

Pool Assignments






