# SQL_Time_Range


因為 Sql 的 between min And  max  是 value >=min &&  value <= max (包含)的意思

所以精確的不寫死寫法是

    MaxTime = theDate.AddDays(1).AddSeconds(-1);

    MinTime = theDate 時間歸零;

    select * from table_name between MinTime and MaxTime;
    

///
  

    SELECT DATEADD( 時間單位, 時間單位的次數即量 , baseDate);

    beseDate 起始日期

    時間單位如設定為 s

    當天的 s 量為 23 h: 59 m: 59 s = 23 * 60 * 60 + 59 * 60 + 59 

    = 82800 + 3540 + 59 = 86399
    

/// 


    select * 
    from log_table 
    where EventTime 
    between CURRENT_DATE() and DATEADD(SECOND, 86399, CURRENT_DATE());

    SELECT CURRENT_DATE(); --   2009-06-08
    SELECT CURRENT_DATE() + 1; --   2009-06-09
    select date_format(CURRENT_DATE(), '%Y-%M-%D'); -- 2020-June-8th
    select date_format(CURRENT_DATE(), '%Y-%m-%d 00:00:00'); -- 2020-06-08


* mysql 中使用 unix_timestamp 和 FROM_UNIXTIME 可以不用指定日期类型。

///

        %M 月名字(January～December) 
        %W 星期名字(Sunday～Saturday) 
        %D 有英语前缀的月份的日期(1st, 2nd, 3rd, 等等。） 
        %Y 年, 数字, 4 位 
        %y 年, 数字, 2 位 
        %a 缩写的星期名字(Sun～Sat) 
        %d 月份中的天数, 数字(00～31) 
        %e 月份中的天数, 数字(0～31) 
        %m 月, 数字(01～12) 
        %c 月, 数字(1～12) 
        %b 缩写的月份名字(Jan～Dec) 
        %j 一年中的天数(001～366) 
        %H 小时(00～23) 
        %k 小时(0～23) 
        %h 小时(01～12) 
        %I 小时(01～12) 
        %l 小时(1～12) 
        %i 分钟, 数字(00～59) 
        %r 时间,12 小时(hh:mm:ss [AP]M) 
        %T 时间,24 小时(hh:mm:ss) 
        %S 秒(00～59) 
        %s 秒(00～59) 
        %p AM或PM 
        %w 一个星期中的天数(0=Sunday ～6=Saturday ） 
        %U 星期(0～52), 这里星期天是星期的第一天 
        %u 星期(0～52), 这里星期一是星期的第一天 
        %% 一个文字% 


