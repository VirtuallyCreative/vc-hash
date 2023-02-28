# Development Time Machine

There are things that I would have benefited from learning early on in my development journey to make me a better freelance developer that no code tutorial or Bootcamp (that I'm aware of) has taught me.

I've been a freelance developer for over 12 years. I'm primarily self-taught and want to help others follow a similar path, learn from my experiences, and take a shorter route to success than I had to.

Development is so much more than just writing code. In this article, I've included some smaller tips I've learned on the job; effective development habits to embed in your development routines - whether you're working on email templates, single-page apps or even complete enterprise solutions.

* [**Learn Why Something Is A "Best Practice" - Then Use It**](https://dev.to/vip3rousmango/learn-why-something-is-a-best-practice-then-use-it). I think this quote from Michael Jordan sums it up best,
    
    > "You can practise shooting eight hours a day, but if your technique is wrong, then all you become is very good at shooting the wrong way. Get the fundamentals down and the level of everything you do will rise."
    
    Make sure you know why something is a best practice or "fundamental" before you use it. Once you learn, uphold those best practices until something better is identified.  
    
* **Add helpful code comments explaining what you try to do with the code**. Try it out, write complex code on Friday, come back two weeks later, and try to explain it to yourself or a co-worker. If you can't, *write better comments so you can*.  
    
* **When naming things -&gt; longer is better**. I should be able to read the name of your function, class, variable, whatever and know from its name WHAT IT DOES OR RETURNS.
    

```js
addTwoNumbers(a, b)
// will always be better than ...
mathFunc(a, b)
aTN(a,b)
// ^^ not helpful!!
```

* **Companies hire you to solve problems, not to memorize code**. Learn how to search well. [Learn the custom search operators on Google](https://www.semrush.com/blog/google-search-operators/) and the [!bang operators on DuckDuckGo](https://duckduckgo.com/bang), the [AI assistant on You.com](https://you.com/code) and the new [Bing](https://www.bing.com/) to be a "power searcher" developer.  
    
* **The business/client rarely cares about the "how - you get it done." They want to hear the "why - you're doing this" and the "what - value it brings" to the business.** I've fallen into this trap, too, getting too technical and seeing a client's eyes gloss to the back of their head as I spit out technical terms.  
    
* **Google isn't the only place to find answers**! Go on Twitter, [Spectrum.chat](http://Spectrum.chat) or IRC Freenode, code forums, etc... and seek out other developer communities! You'll have to look far and wide for answers sometimes on unknown errors, or you're the first one posting the question, so make it good, then others come back and use YOUR post as the solution moving forward!  
    
* **Master your IDE well**. You will spend so much time in this application that even something new you learn that saves you 5 seconds repeatedly over the lifetime of your developer career will **save you loads of time** and make you more efficient. I spent the money on [@mrahmadawais](https://twitter.com/mrahmadawais)'s [VS Code pro course](https://vscode.pro), and it was worth every. Single. Penny. If you're a VS Code user, I highly recommend it.  
    
* **Be proactive with bugs/errors**. Just like how the hero in a video game knows they're going in the right direction when he sees enemies. Developers are "going in the right direction" when they get errors. This sounds counter-intuitive, I know, but hear me out. Errors are your code's way to attempt to give you insight into the issue you're experiencing, so listen to your error codes and output and what they tell you to defeat them. Some of the best developers I've met embraced errors in a way I never did, and I learned quickly to do so.  
      
    Always handle your errors. ([Rollbar](https://rollbar.com), [Sentry.io](http://Sentry.io), ["Application Insights" - Azure Monitor](https://azure.microsoft.com/en-us/services/monitor/), [New Relic](https://newrelic.com), etc.. are fantastic services to help report, log, flag and visualize all that).  
    
* **Also, speaking about being proactive, don't be scared to break things on purpose (that aren't production)**. "Sometimes, you have to break a few eggs to master an omelette - just make sure your eggs have error reporting turned on first..."  
    
* **Be patient, and use distractions effectively as a technique to your advantage**. Sometimes you'll get stuck or hit a complex problem. Make sure you have something that can distract you enough that *you stop thinking about the problem* for a good set time (for me, at least an hour) before trying to come back with a fresh idea.  
    
* **Inclusive design/development is for *everyone***. If you include a11y design principles as a guiding principle to uphold, all tasks are fundamentally easier than trying to turn something inaccessible accessible.  
    
* **Strongly avoid deploying to production at the end of the business day on Friday**. Trust me on this. It is asking for trouble. Even the client wants to pay double.  
    
* **Do not book vacation time the day after a significant deployment**. Looking back, that was not an intelligent plan. Give yourself a buffer to be available for your clients, dev team, and a raging server fire... you know - whatever might happen after a significant deployment.  
    
* **"Measure twice, cut once" isn't just for carpentry,** and I now hold the mantra "test twice, deploy thrice." Between Staging and Production, having a 1:1 clone of production (I called it P.A.T. - production acceptance testing) to be sure pushing to prod will go as planned has saved me countless times in hitting an unknown configuration issue or something unforeseen that if I went straight to production would not have been a fun time.  
    

Well, that's the growing list I've compiled so far! What have you learned on the job that no course or tutorial can prepare you for? Comment below and help share the knowledge!

Stay hungry, and be humble. 🤗🤗