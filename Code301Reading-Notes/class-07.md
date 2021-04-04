# What Google Learned From Its Quest to Build the Perfect Team
* Google’s most effective teams :were composed of friends who socialized outside work.
* Others were made up of people who were basically strangers away from the conference room.
* Some groups sought strong managers. Others preferred a less hierarchical structure.
* `‘‘group norms.’’` Norms are the traditions, behavioral standards and unwritten rules that govern how we function when we gather: One team may come to a consensus that avoiding disagreement is more valuable than debate; another team might develop a culture that encourages vigorous arguments and spurns groupthink.
* Some groups said that teammates interrupted one another constantly and that team leaders reinforced that behavior by interrupting others themselves.
* other teams, leaders enforced conversational order, and when someone cut off a teammate, group members would politely ask everyone to wait his or her turn.
*  There were teams that contained outsize personalities who hewed to their group’s sedate norms, and others in which introverts came out of their shells as soon as meetings began.
* the researchers wanted to know if there is a collective I. Q. that emerges within a team that is distinct from the smarts of any single member.
* To accomplish this, the researchers recruited 699 people, divided them into small groups and gave each a series of assignments that required different kinds of cooperation.
*  teams that did well on one assignment usually did well on all the others. Conversely, teams that failed at one thing seemed to fail at everything. 
* the good teams all had high ‘‘average social sensitivity’’ — a fancy way of saying they were skilled at intuiting how others felt based on their tone of voice, their expressions and other nonverbal cues
* companies try to optimize everything, it’s sometimes easy to forget that success is often built on experiences — like emotional interactions and complicated conversations and discussions of who we want to be and how our teammates make us feel — that can’t really be optimized.

# How I explained REST to my brother
* Roy Fielding helped write the first web servers, that sent documents across the Internet , he helped write the HTTP
* http  it is capable of describing the location of something anywhere in the world from anywhere in the world.
* The whole world wide web is built on an architectural style called “REST”
* REST provides a definition of a “resource”, which is what those things point to (Resources are just concepts. URLs)
*  A web page is a “representation” of a resource
* URLs tell the browser that there's a concept somewhere >  the browser asks for the web page representation of the concept .
* a resource has only a single representation
* Web Services” or "APIs" the basic concept of it is that computers can use those same protocols to send messages back and forth to each other.
* redirect :  one machine tell another machine about a resource that might be on yet another machine through URLs
* “polymorphism”: means all machines are considered nouns  that different nouns can have the same verb applied to them.
* when you go to a web page, the browser does an HTTP GET on the URL you type in and back comes a web page.
* very different kinds of nouns can be treated the same. Whether the noun is an image, text, video, an mp3, a slideshow, whatever. I can GET all of those things the same way given a URL
* every URL would have a human readable and a machine readable representation
* HTTP GET: requests a representation of the specified resource. Requests using GET should only be used to request data (they shouldn't include data)
* HTTP POST: POST is used to send data to a server to create/update a resource.
* HTTP PUT: The HTTP PUT request method creates a new resource or replaces a representation of the target resource with the request payload.
* A PATCH : request is considered a set of instructions on how to modify a resource. Contrast this with PUT; which is a complete representation of a resource.