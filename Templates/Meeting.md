
**OUTGOING**
```dataview
	LIST without id
	link(meta(out).path)
	WHERE file.name = this.file.name
	flatten file.outlinks as out
```
**BACKLINKS**
```dataview
	LIST without id
	link(meta(in).path)
	WHERE file.name = this.file.name
	flatten file.inlinks as in
```
#meeting
- [ ]  {{title}} (@{{date}} {{time}})


# Links


# Attendees

# Agenda
%%  Write down the main topic to discuss %%


# Notes
%%  Cover any key information discussed in the meeting %%

