## Log4j :

1. Logging : getting messages from application (Production server) like success, errors, warnings,..etc

2. Moniter the process, find bugs from realtime environment.

3. Tools :
   Log4J 2.x, Java Logging, Commons Logging ..etc

4. Log Messages can be stored at different places ex., Files, Database, Email , Console..etc

5. Components
    1) Logger : (which classes) it is a base object in Log4J. It enables/activates Logging/Moniter of a class/process.
        ```
        class EmployeeController {
           Logger log = LogManager.getLogger(EmployeeController.class);
        }
        ```
     -  Do not create Logger object for Entity/DTO/POJO classes.
     -  Recomanded Controllers/Services..etc
            
    - Priority Methods :
      - These are pre-defined methods exist in Logger object which prints messages based on type.
      - TRACE  : To find messages from multiple stages/env/apps.
      - DEBUG  : To print final result of a process/ internal details
      - INFO   : Current Step 
      - WARN   : App related messages 
      - ERROR  : To give details about exception
      - FATAL  : Environment related issues ex:Database Connection is closed.

        TRACE > DEBUG > INFO > WARN > ERROR > FATAL

    2) Appender:- Location of messages to be stored. (classes). (where to store) Do not create Logger object for Entity/DTO/POJO classes.     
        - FileAppender : Write data to Log File  (___.log)
        -  ConsoleAppender : Prints data at console
        - JDBCAppender : Store messages at Database table
        - SMTPAppender : Write messages to Email.

        - Project can have even multiple appenders.

    3) Layout:  (how to print) Message Format/Pattern.
        - Default Layout (Message and NextLine)
        - HTML Layout (___.html)
        - XML Layout (___.xml)
        - PatternLayout (Your own format)
=====================================================================
