# SQL_Time_Range


因為 Sql 的 between min And  max  是 value >=min &&  value <= max (包含)的意思

所以精確的不寫死寫法是

MaxTime = theDate.AddDays(1).AddSeconds(-1);

MinTime = theDate 時間歸零;

select * from table_name between MinTime and MaxTime;




SELECT DATEADD( 時間單位, 時間單位的次數即量 , baseDate);

beseDate 起始日期

時間單位如設定為 s

當天的 s 量為 23 h: 59 m: 59 s = 23 * 60 * 60 + 59 * 60 + 59 

= 82800 + 3540 + 59 = 86399

