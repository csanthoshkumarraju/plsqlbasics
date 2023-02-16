# plsqlbasics
-- pl/sql basic syntax
declare
  i number := 2;
begin
  dbms_output.put_line(i);
end;

-- **********************************************************
-- pl/sql operators
declare
b number := 2;
d number := 4;
begin
dbms_output.put_line(b|| '+' || d || '=');
dbms_output.put_line(b+d);
dbms_output.put_line(d || '-' || b || '=' );
dbms_output.put_line(d-b);
dbms_output.put_line(b || '*' || d || '=' );
dbms_output.put_line(b*d);
dbms_output.put_line(d || '/' || b || '=' );
dbms_output.put_line(d/b);
dbms_output.put_line(b || '**' || d || '=' );
dbms_output.put_line(b**d);
-- dbms_output.put_line(b|| '+' || d || '=' || b+d); -- here getting error ORA-06502: PL/SQL: numeric or value error: 
-- character to number conversion error ORA-06512: at line 15
-- ORA-06512: at "SYS.DBMS_SQL", line 1721
end;

-- *************************************************
-- pl/sql conditions
declare
 b number := 6;
 d number := 1;
 begin
    if b>d then
        dbms_output.put_line(b || '>' || d);
    elsif b<d then
        dbms_output.put_line(b || '<' || d);
    else
        dbms_output.put_line(b || '=' || d);
    end if;
end;

-- ************************************************************************
--  pl/sql case
declare
day varchar2(100) := 'THU';--case sensitive assign same case either lower/upper case letters
begin
case day
when 'MON' then  dbms_output.put_line('MONDAY');
when 'TUE' then  dbms_output.put_line('TUESDAY');
when 'WED' then  dbms_output.put_line('WEDDAY');
when 'THU' then  dbms_output.put_line('THURSDAY');
when 'FRI' then  dbms_output.put_line('FRIDAY');
when 'SAT' then  dbms_output.put_line('SATURDAY');
when 'SUN' then  dbms_output.put_line('SUNDAY');
else dbms_output.put_line('NOT A DAY');
end case;
end;
 
--  *******************************************************
-- pl/sql loops
-- pl/sql basic loop
declare
b number := 0;  
begin   
    loop
    dbms_output.put_line(b);
    b := b+1;
    if b > 15 then 
    exit;
    end if;
    end loop;
end;
-- pl/sql for loop
declare
b number :=0;
begin
    for b in 0..10 loop
      dbms_output.put_line(b);
      end loop;
end;
-- pl/sql while loop
declare
b number := 0;
begin
 while b<20 loop
 dbms_output.put_line(b);
 b := b+1;
 end loop;
end;






   
 




