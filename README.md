# SQL_Time_Range


因為 Sql 的 between min And  max  是 value >=min &&  value <= max (包含)的意思

所以精確的不寫死寫法是

MaxTime = theDate.AddDays(1).AddSeconds(-1);
MinTime = theDat

select * from table_name between MinTime and MaxTime;

