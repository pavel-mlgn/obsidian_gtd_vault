
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
#project
- [ ] {{title}}

# Todo List
> [!todo] Active
> ```dataview
>  task
>  from [[]]
>  where !completed
> sort file.ctime desc
> ```

> [!todo] Completed
> ```dataview
>  task
> from [[]]
>  where completed
>   sort file.ctime desc
>   limit 10
> ```

# Links


# Description


