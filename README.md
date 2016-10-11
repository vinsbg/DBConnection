# DBConnection
Simple class for database connection

# Instructions

```
# Place your database credentials
private static $dbName = '';
private static $dbHost = '';
private static $dbUsername = '';
private static $dbUserPassword = '';
```
# Usage

```
include 'dbConnection.inc.php';

// establish connection 
$pdo = Database::connect(); 

    // selecting from database with prepared statements
    $value = $pdo->prepare('SELECT * FROM table WHERE id= ?);
    
    // binding parameter
    $value->bindParam(1, $id, PDO::PARAM_INT); 
    
    // executing
    $value->execute();
    
    // fetching results
    $result = $value->fetch();

    if( $result > 0) {
        // working with results
    }
    else {
        // working without results
    }
    
// closingnnection to database    
Database::disconnect(); 
