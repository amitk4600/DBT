create table temp1
(
S1 char (15),
S2 char (20),
ans char (15)

);

delimiter  //

create procedure xyz1 (S1 char (15),S2 char (20))

begin 
 declare a int (4);
 set a = locate (s1,s2 );
 if (a != 0 )then
 insert into temp1 values (s1, s2 ,'present' );
 else 
  insert into temp1 values (s1, s2 ,'absent' );
  end if;
  end ;//
  delimiter ;
  
  call xyz('amit','kumar' );
    call xyz('cdac','mumbai' );
  call xyz('amit','berwal' );
  
  select * from temp1 procedure xyz;
  drop table temp;


