
> [!note] Meetings
> ```dataview
> task
> from #meeting  and -"Templates"    
> where !completed
> sort file.ctime desc

> [!important] Projects
> ```dataview
> task
> from #project and -"Templates"    
> where !completed
> sort file.ctime desc

> [!todo] Tasks
>> [!todo] Now
>> ```dataview
>> task
>> from #task/now and -"Templates"  
>> where !completed
>> sort file.ctime desc
>> ```
>
>> [!todo] Next
>> ```dataview
>> task
>> from #task/next and -"Templates"  
>> where !completed
>>  sort file.ctime desc
>>  ```
>
>> [!todo] Waiting
>> ```dataview
>> task
>> from #task/waiting and -"Templates"  
>> where !completed
>> sort file.ctime desc
>> ```
>
>> [!todo] Someday
>> ```dataview
>> task
>> from #task/someday and -"Templates"  
>> where !completed
>> sort file.ctime desc

> [!done] Completed
> ```dataview
> task
> from #task 
> where completed
> sort file.ctime desc
> limit 10
> ```
