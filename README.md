# WELCOME 
### people who cant find anything usefull on the internet

So I am trying to figure out how to build a Twitch extension, however I have pretty much no web-programming experience.
Things I know:    
							* Java	  	  
              * some JavaScript  
              * how to fake to know things

**Follow along my journey to the unknown lands of Twitch full stack developement** (but not really full stack, because in this application I really do not want to have to host a server.)

Ok so first of all I tried to read the [Twitch docs](https://dev.twitch.tv/docs/), which I did.
But there are a lot of problems for me: I find them very confusing.  I also find that important things are simply missing.

Then I tried the [Twitch developers' forum](https://discuss.dev.twitch.tv/). I did not find answers to my problems and even my own topic did not get a satisfying reply(yet). There is this guy(I will not tell his name), who replies to a lot of topics and seems to know what he is talking about. But I find his answers very downlooking onto those people seeking help and he barely gives a good answers/he barely answers the question instead talking around it.

Well so I took a step back and followed along [HassanSaleh's tutorials](https://hassansaleh.info/p/5)([his github](https://github.com/hassansaleh31) his site is down very often but the tutorials are very very good).  
  -> Well I dont have Windows Pro edition so docker was no option and I got quite frustrated
  
  Now this leads to the interesting part:  
  I was frustrated, so I wanted to start from a different direction: I programmed the frontend HTML/CSS without any JavaScript or functionality whatsoever. ***Beautiful sweet relaxation***. If you ever get stuck just start playing with some design stuff, this really helps making your mind free, but also come up with new ideas and maybe even a better one for your app.
 
 #### I went back to the docs, googled everything I could and came up with this:
 
 - [A 101 tutorial](https://dev.twitch.tv/docs/tutorials/extension-101-tutorial-series/introduction) giving some more insights how this whole thing works
 - [A site](https://aaronparecki.com/oauth-2-simplified/) where I finally started to understand Authentication (actually its [two](https://developer.okta.com/blog/2019/05/01/is-the-oauth-implicit-flow-dead))
 - [Some explanation](https://hackernoon.com/an-overview-of-frontend-and-backend-interaction-48l031ba) on how frontend and backend interact
 - [A site](https://www.upwork.com/hiring/development/a-beginners-guide-to-back-end-development/) with no code but very good explanation on what the full stack is and how it works
 - [HTTP requests in JavaScript](https://www.freecodecamp.org/news/here-is-the-most-popular-ways-to-make-an-http-request-in-javascript-954ce8c95aaa/)
 - [Understanding JWT (Web Tokens)](https://blog.hasura.io/best-practices-of-using-jwt-with-graphql/) for authentication
 
 #### Meanwhile the forum had not slept
 
 I received an answer pretty much telling me how stupid I am and that its an 'impractical way' how I want to do it. Ok...uhm yeah. This did not give any clearance other than telling me, if I want to access the authentication-required parts of the Twitch API (servers) I absolutely need a backend hosted by me.  
 Oh and *another thing*:   
 Twitch decided to change the whole thing to: You want something from Twitch? Athenticate! So every call now needs that.  
 
 #### So fresh start of thinking (again)
 
 I thought of really hosting some authentication service myself at home, but this would kind of suck. You need a server(even if its just on your PC), you will get a lot of requests on that -> slow internet, you would probably get hacked.   
 
 Well I honestly thought of going into a super different direction like a website that can be integrated to Streamlabs/OBS -> same server problem, and I do not want to go into a different environment with the same problems **(I did not look that up yet, so maybe this would be an approach I think as I am writing that)**  
 Or I could make an extension, where no Twitch call is needed, like integrating something like game-statstics, a website, or showing emotes of a streamer (and putting them into the files myself, because we cant make API calls and don't want a backend)
