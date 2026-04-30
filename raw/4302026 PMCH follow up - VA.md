

- What's the purpose of the RPA- what tasks is it handling in the process today? 
	- What are the inputs & outputs of the review process/RPA? 
- What parts of the current solution need to stay the same? (i.e. is SharePoint list to TrackWise a necessity or could this be handled in another way, should we keep SharePoint but do RPA/decisioning somewhere else, etc)
- What are TrackWise's capabilities- what is done in TrackWise? (Edits, reviews, etc.)
	- lots of menus, lots of drop downs, free text fields
	- Don't have to physically copy and paste- use RPA to populate
	- Taking info about record and making decision- RPA is responsible for entry of info into Trackwise and sending confirmation emails 
- What is the ideal output of the intake process? What pieces of information/columns? What does it look like for you guys to have everything you need?
	- different for different products & types of events
	- i.e. no patient harm, just a crack - not a ton of info
	- on the other end of the spectrum- patient harm - need tons of info
	- Master file - specific set of devices 
	- Skipping q's we don't need - making sure there is consistency across answers, there is sufficient detail to make follow up decisions
		- Sometimes there are tons of devices submitted at a time - could we have a system that chunks this into products.
- What is the input to the failure mode classification AI? What is the output? (From the previous call, it sounded like the output isn't just the failure mode but is some sort of form filled out)
- What's the tech stack/architecture of AI failure mode classification today- where does this live?
- Ideally, what would change in the intake process if we knew the failure mode classification during intake? (What are the follow-up questions, are these defined already, etc.)


- Thoughts on having a complaint application for intake and review vs. disjointed intake in a form and RPA for review/decisioning?


For next follow up/if we have time (assuming no, but we can do this stuff once we have confirmation to work on this prototype):
- Can we get access to the full MSFT form?
- Is there additional branching logic/follow-up questions documented anywhere?
- How do we know what is required as a follow-on? Schedule workshops with SMEs to uncover this or is it well documented?
- Can we get access to the data requirements for TrackWise? (All the fields and requirements for the fields)
- Can we get examples of a completed form and final PI in TrackWise?