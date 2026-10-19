
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
- [ ] Team Meeting (@2024-09-01 10:00)


# Links


# Attendees
- [[@Sam]]
- [[@Robert]]
- [[@Mary]]


# Agenda
%%  Write down the nain topic to discuss %%

# Notes
%%  Cover any key information disscused in the neeting %%
