

```
>>> MESSAGE BOARD >>> 

>>>>>>Storage procedures for Message Board >>>>

Authentication :

create user 'forum-client'@'%' identified by 'njit490'; 

Login: forum-client      password: it490
```
```
getForum Procedure 

mysql> delimiter /                                                                                                                                            
mysql> create procedure getForums()                                                                                                        
    -> begin                                                                                                                                                  
    -> select * from forums;                                                                                                    
    -> end;                                                                                                                                                   
    -> /  
```
```
 getThread Procedure 
 
 mysql> delimiter /                                                                                                                                            
mysql> create procedure getThreads(IN ID int(8) )                                                                                                     
    -> begin                                                                                                                                                  
    -> select * from threads where ForumID = ID;                                                                                                 
    -> end;                                                                                                                                                   
    -> /    
``` 
```

 getReplies Procedure 
 
ysql> delimiter /                                                                                                                                            
mysql> create procedure getReplies(IN ID int(8) )                                                                                                    
    -> begin                                                                                                                                                  
    -> select * from replies where ThreadID = ID;                                                                                                 
    -> end;                                                                                                                                                   
    -> /  
```    
```
  Insert Procedure 
  createThread Procedure
`
mysql> delimiter / 
mysql>create procedure createThread(IN ID int(8),nam varchar(80), cont TEXT, usr varchar(80))
 -> begin
->insert into threads(ForumID,Name,Content,User) values ( ID,nam,cont,usr) 
 -> end;                                                                                                                                                   
    -> /  
``` 
```

createReply Procedure 

create procedure createThread(IN ID int(8),nam varchar(80), cont TEXT, usr varchar(80))
begin
insert into threads(ForumID,Name,Content,User) values ( ID,nam,cont,usr) 
end;
```



   
   
    
    
