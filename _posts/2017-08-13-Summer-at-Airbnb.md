---
layout: post
title: The Magical Summer
---

A review of the people I have met, lessons learned, and adventures travelled
during my summer of 2017 in SF.

## The people

There were a few groups of people I met this summer. In no particular order, I
met the Acts2Fellowship seniors + staff, Airbnb interns (Airterns), the Payments
team and full time Airbnb Christians. Here are my thoughts on each group of
them.

### Acts2Fellowship Seniors

These were the first people I met because I asked to live with them. This group
of people taught me so much what it meant to engage in deeper relationships
with each other - more than just surface layer interactions but also deeper
more personal interactions. I've mentioned to them many times this fact, so I
know that they know what I'm talking about. 

Now, this teaching wasn't necessarily them telling me. Because the summer is
typically a period of time where we transition into new structures, there is
always some kind of transition. Because leaders change and people move, students
often have different leaders. People do take it roughly, but from what I saw
these seniors didn't really take an off-period to gather themselves. They (or
their leader) immediately setup time to get to know each other on a deeper level
(or at least a level in which normal daily interaction wouldn't achieve). With
student leadership and ministry looming over our heads, I thought this was an appropriate response to the situation at hand.

### The Airterns

The Airbnb interns (or Airterns because at Airbnb, we like to add the word 
"Air" everywhere possible) was such an interesting group of people. I still
remember the first day of Cohort 2, we were gathered around the Eatrium 
awkwardingly greeting each other as most would when they first meet each other.
Then, we (as interns) pretty much hit it off pretty well. We met each other,
met our teams, and learned about the platform/product. 

Other than the interns I already knew from UT, I got to know Tanay, Dan, Selina, 
Victor, and Nick (Yifan) pretty well. I know my interactions with most of them were
relatively spontaneous, but through those situations, we were able to share more
about our lives and aspirations in life. Don't forget me when you're famous!! (:

### Christians at Airbnb

These people are just ordinary Airbnb employees who have a love for Jesus like 
I do. I was able to find them on their Slack channel, and subsequently was able
to meet them because they decided to have a lunch meetup. I was kind of
surprised because there wasn't any activity for the past few weeks (ever since
Passion Week, I think). I was able to meet the core group of Christians who tried to start a weekly lunch meet up just to share what happened in the past week. From the words of one of the full-timers "We (him and Brett) are very encouraged by you and have a bigger flame to keep fighting the fight at Airbnb and in SF" - Cory Mead. It's encouraging to see how my simple attendance to these weekly lunchs can do. 

### The Payments Team

How can I not talk about my team and the people I worked with in a post about
meeting new people at my summer internship? My direct manager was Brian Lin, 
and he would be the person who I would always ask for opinions on objective
design decisions. He was a great resource to talk to about design paradigms, career, life at Google and Airbnb, and future aspirations. Of course, there were times when we seemed to be on different pages, but after feedback during the midpoint review, it was all resolved (: 

The next few people (in sorted order) that I worked a lot with helped me understand the bigger design principles of the payments infrastructure and product: 
[Emily Cheng](https://www.linkedin.com/in/emcheng/),
[Ninad Khisti](https://www.linkedin.com/in/ninadkhisti/),
[Mai Leduc](https://www.linkedin.com/in/maileduc/),
[Leo Li](https://www.linkedin.com/in/leoxli/),
[Fei Nan](https://www.linkedin.com/in/feinan/),
[Justin Park](https://www.linkedin.com/in/justindoit/),
[Mengfei Ren](https://www.linkedin.com/in/mengfei-ren-43869854/),
[Sean Safahi](https://www.linkedin.com/in/ssafahi/),
[Rajen Shah](https://www.linkedin.com/in/rajenshah/),
[Virat Singh](https://www.linkedin.com/in/singhvirat/),
[Kevin Sun](https://www.linkedin.com/in/kevin-sun-1b7b2720/),
[Patrick Tiet](https://www.linkedin.com/in/patrick-tiet-3978b33b/),
[Michel Weksler](https://www.linkedin.com/in/michelweksler/),
[Sam Wyman](https://www.linkedin.com/in/sam-wyman-aa716b14/),
[Haochen Zhao](https://www.linkedin.com/in/haochen-zhao-65597988/).


## Lessons learned about work

1. Rewriting history on git commits must be done with precaution. 
  * Ideally, we should have 1 commit per pull request (PR). This way it becomes very intuitive to knowing how to revert the particular PR, and makes it easier to search PRs for a particular code change.
  * ```git reflog``` and ```git rebase -i``` are very useful commands for when one messes up when modifying the git history. 
2. Validate your assumptions.
  * There is a balance between validating assumptions and writing your feature's actual code.
  * In my case, one of the crucial mistakes I made was to not validate the text output of a particular API that I was using. Due to the midleading wording, this ultimately led to me changing APIs to something more appropriate. This change put me back one week because I had to redesign my architecture to fit the new API.  
3. When making schema changes via OSC or some other method, ensure that the code base and database are in sync with each other. 
  * Essentially, when the database and code build become out of sync, many writes or reads will no longer be possible because the code base representation of the db might be different than the actual representation of the codebase.
  * Separate ```DROP [column]``` and ```ADD [column]``` so that you can safely run the schema change with a particular protocol to ensure no service outage. 
    * When ```DROP [column]```, ensure that all usages of this particular column is removed and that these columns are ignored when auto-generating the code representation of the db.
    * When ```ADD [column]```, make sure that all code changes that would use these columns aren't used until AFTER these columns are successfully added into the db.

## Lessons learned about my life and faith

1. **Relationships are hard.** Whether it's between friends, loved ones, or leaders, they all involve time and intentionality. This summer, I've been trying to keep up with a few friends who graduated and moved out of Austin to other cities. Maintaining some contact was hard even during the summer when I don't really have that much to do. It's going to be a big challenge for me to maintain these relationships during the school year and beyond especially because I inherently don't talk to people I don't see on a day-to-day basis. 
2. **Following Christ is hard.** There were many times during the summer when I would not be able to hang out with other interns because I live in Berkeley. In particular, I decide to live in Berkeley (and have an almost 1 hour commute time) because I wanted to 1) have some sort of accountability around me so that I could grow in my faith and 2) get to know my Berkeley peers. The cheaper rent was a bonus on top of these two listed reasons. This meant that unless I had an intern event or something relatively big, I could not stay in the city for too long before it got dark. Ultimately, even though I missed out on these opportunities to hang out with the other Airterns, there were many opportunities I had to relate with the Berkeley seniors instead. 
3. **Ministry isn't just meant for when you plan for it.** Jesus calls us to love others the way he has loved us (John 15:12). Loving others - truly something super abstract without context but so real in the moment. I remember one situation when I was memorizing a chapter in the Bible during dinner with an intern where we were slightly interrupted by another intern. Instead of being annoyed because things hadn't gone as planned, we decided to talk about what we were doing. We had no idea she was in a seeker's bible study back at CMU, so once we learned of that, we were able to have a long conversation about our faith and mini testimonies. Looking back at this encounter, had I just imagined going with the original plan of memorizing Scripture, we would had lost an opportunity to share our testimonies and sow the seed of the gospel. 
4. **I don't always have a good grasp about problems that I have.** To be specific, one time I was having ```git``` issues, and I had a premature prediction that I would be ready to meet up with MR CC in one hour (6pm). However, when 6pm came by, I was not ready at all and had to push our meeting time back to 7pm. But when 7pm came by, I was once again not ready. Ultimately, I wrapped up my issues so that I wouldn't keep my friends waiting for too long. What seemed to be a simple fix was much bigger than I thought, and it was due to my lack of understanding of my lack of understanding of ```git```.

## The Magical Adventures of 2017

[Link to doc](https://docs.google.com/document/d/15owe3Z3pZKipx6B71f6jnL1HFPjAYizodaoiKf9tD_4)

