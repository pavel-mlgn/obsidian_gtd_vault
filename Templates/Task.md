
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

 #task/now %% now | next | waiting | someday %%
- [ ] {{title}}


# Links


# Description
