RPA manages entry into Trackwise, populates fields from SharePoint
	Sends e-mails - confirmation, missing information, additional instructions
	Handled in bulk (phases), e-mail then Trackwise entry
	Other RPA processes (similar, for Trackwise population)
What is the Trackwise system? 
	Can be used for entry (if not used for RPA)
	Tools work on top of Trackwise for efficiency

Intake
	Gaps that currently exist - what does the ideal intake process look like?
		There are different products/events that look different from each other
			Minimal low risk vs high risk (revision surgery) vs middle ground
			Lots of variance between the risk profiles
		Master file - specific set of devices
		Amazon example (UI for complaint, e.g. shipped item broken vs. the backend for the customer reps)
			Strategies for JR to interrogate based on the intake form
			Some more complex cases require phone calls (can we surface these w/o an agent?)
		AI Agent would need to capture expertise of case agent
			Existing form is good basis to start
	AI Goal - fill out all the information for the record at the end of intake
		Skip the questions you don't need to ask
		Don't miss information that needs to be captured
		Need to follow up on some information
		Some information may already be included in description
			Sometimes multiple issues reported at a time - could the system chunk out the items into multiple issues?
	Do we need to keep the Sharepoint record as the Source of Truth?
		Only if we are keeping the current RPA tool (can interface directly w/Trackwise, do want to have error tracking report separate from Trackwise)
			Benefit for review prior to entry into Trackwise (1st customer contact), control what goes into system
		Information can be scattered across Trackwise screens - RPA condenses into one screen (right information in right place)
		Define what needs to be reviewed by specialist and what can continue automatically
	Ability for AI to learn and adapt based on outputs (feed back to improve model)
		How hard is it to build in the agentic learning?
		Sometimes SOP may change
	