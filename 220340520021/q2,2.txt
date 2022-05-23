create table tempp3(
sidea float,
sideb float,
sidec float,
triangle_status varchar(25)

);
delimiter //
create function FUNC1 (Sa float, Sb float, Sc float)
returns boolean 
deterministic
begin
      if  (Sa+Sb>Sc ) and (Sb+Sc>Sa )
      then
      return true;
      else 
      return false;
      end if ;
      end; //
      delimiter ;

delimiter //
create procedure xyz(a float, b float, c float)
begin 
 if valid_triangle (a,b,c ) then
 insert into tempp3 values (Sa,Sb,Sc, 'valid triangle');
 else
  insert into tempp3 values (a,b,c, 'invalid triangle');
  end if ;
  end; //
  
  
call xyz(7,10,5 );