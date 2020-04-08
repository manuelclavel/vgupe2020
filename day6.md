# Day 6 #
## Review Homework ##
## Logic tier - Data tier
### Connecting with database ###
- For **Connection** with [local] database. Use JDBC. JDBC
stands for **Java Database Connectivity**. JDBC is a Java API to connect
and execute the query with the database. It is a part of JavaSE (Java
Standard Edition). JDBC API uses JDBC drivers to connect with the
database.

### Basic example ###
    
	public class MySQLAccess {
    // Set the connection's noAccessToProcedureBodies=true property
    // The JDBC driver will then create "INOUT" strings for the arguments without requiring meta data.
    
	private static final String CONNECTION = "jdbc:mysql://localhost:3306/booking_app?noAccessToProcedureBodies=true";

    public Connection getConnect() throws Exception {
        Connection conn = null;
        try {
            //The forName() method of Class class is used to register the driver class.
            //This method is used to dynamically load the driver class.
            // This will load the MySQL driver, each DB has its own driver
			
            Class.forName("com.mysql.cj.jdbc.Driver");
			
            // Setup the connection with the DB
            // Properties for user and password. 
			
            Properties p = new Properties();
            p.put("user","<your-db-user>");
            p.put("password","<the-db-user-password");
            // Now try to connect
            // The getConnection(String url, Properties info) method of Java DriverManager class
            // attempts to establish a connection to the database by using the given database url.
            
            conn = DriverManager.getConnection(CONNECTION, p);

            System.out.println("It works !");

            return conn;
        } catch (Exception e) {
            throw e;
        }

    }


### Executing stored procedures ###

- To execute stored procedures. Use **Callable Statements** .
A java.sql.CallableStatement is used to call stored procedures in a database.
A stored procedure is like a function or method in a class, except it
lives inside the database. Some database heavy operations may benefit
performance-wise from being executed inside the same memory space as
the database server, as a stored procedure.

You create an instance of a CallableStatement 
by calling the **prepareCall()** method on a connection object.

Once created, a CallableStatement is very similar to a
PreparedStatement. For instance, you can set **parameters** into the SQL,
at the places where you put a ? .

Once you have set the parameter values you need to set, 
you are ready to **execute** the CallableStatement.

The **executeQuery()** method is used if the stored procedure returns a 
**ResultSet**.

If the stored procedure just updates the database, 
you can call the **executeUpdate()** method instead.

A stored procedure may return **OUT parameters**. That is, values that are
returned instead of, or in addition to, a ResultSet. After executing
the CallableStatement you can then access these OUT parameters from
the CallableStatement object.


### Basic example ###

    DROP FUNCTION IF EXISTS isValidId;
    DELIMITER //
    CREATE FUNCTION isValidId(id varchar(100))
    RETURNS INT DETERMINISTIC
    BEGIN
    DECLARE result INT DEFAULT 0;
    DECLARE courtid INT DEFAULT -1;
    
    SELECT id REGEXP '^[A-Za-z0-9]+$' INTO result;
    
    RETURN(result);
    END //
    DELIMITER ;



    DROP PROCEDURE IF EXISTS CreateCity;
    DELIMITER //
    CREATE PROCEDURE CreateCity(
    IN cityId varchar(100),
    OUT result int)
    BEGIN

    /* identifier is a string of alphanumeric characters */
    IF isValidId(cityId) = 0
    THEN
	   SET result = 501;
    /* city name exists */
    ELSEIF EXISTS(SELECT 1 FROM city WHERE name = cityId)
    THEN
      SET result = 502;
    ELSE
      INSERT INTO city (name) VALUES (cityId);
      SET result = 200;
    END IF;
    SELECT result;
    END //
    DELIMITER ;



### Presentation tier - Logic tier

#### Discussion: framework vs frameworless REST API

**Article borrowed from:**

https://medium.com/consulner/framework-less-rest-api-in-java-dd22d4d642fa

>> Java ecosystem is packed with **frameworks** and **libraries***.  
>> For sure not as many as in JavaScript world and they don't get old as quickly too
>> but still this fact causes that I dare to think that we've already
>> forgotten how to **create a completely framework-less applications**.

>> You may say: **Spring** is a standard, why to re-invent a wheel. **Spark** is
>> a nice small REST framework. **Light-rest-4j** is yet another.

>> I tell you, sure, you're right.

>> You **get a lot of bells and whistles** with a framework, but you also get
>> **a lot of magic**, **learning overhead**, **additional features** which you'll
>> most likely not use and **bugs** as well. The more external code is there
>> in your service the bigger chance that its developers have made some
>> mistakes.

>> Open source community is active and there's a great chance that these
>> bugs in the framework will be fixed soon, but still I'd like to
>> encourage you to **re-think if you really need a framework**.

>> If you're doing a small service or a console application maybe you can live without it.

>> What you could gain (or loose) by sticking to pure java code? Think of these:

>> - your code could be much cleaner and predictable (or a complete mess 
if you're a bad coder)

>> - you'd have more control over your code, you won't be constrained by a framework 
>> (but you'd have to often write own code for what framework gives you out of the box)

>> - your application would deploy and start much quicker, because 
>> the framework code does not need to initialise dozen of classes 
>> (or not start at all, if you messed up the stuff, e.g. multi-threading)
    
>> - if you deploy your app on Docker, your images could be much slimmer 
>> because your jar would be slimmer too

>> I did a little experiment and tried developing a framework-less REST API.

>> I thought it could be interesting from learning perspective and a bit refreshing.

>> When I started building this I often came across situations when 
>> I missed some features which Spring provides out of the box.

>> At that times, instead of enabling another Spring capability, 
>> I had to rethink it and develop it myself.

>> It occurred that for real business case I would probably still prefer 
>> to use Spring instead of reinventing a wheel.

>> Still, I believe the exercise was a pretty interesting experience.


## No Homework for Day #7
