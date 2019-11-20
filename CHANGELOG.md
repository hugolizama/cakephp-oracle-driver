# Changelog

## 1.0.1 - Tested in Cakephp 3.6.14
*  #### Changes
    * **src\Database\Dialect\OracleDialectTrait.php:** quoteIdentifier function added to treat those names of tables with more than 30 characters.
    * **src\Database\Schema\OracleSchema.php:** convertForeignKeyDescription function modified to convert all column names to uppercase.
    * **src\Database\Statement\OracleStatement.php:** fetch function replaced to use un-auto-shorten identifiers, which is done in OracleDialectTrait "quoteIdentifier".


*  #### Deprecated fixes
    * **src\Database\Schema\OracleSchema.php:** Cake\Database\Schema\Table --> Cake\Database\Schema\TableSchema and change every use of Table to TableSchema; index() to getIndex(); constraint() to getConstraint().
    * **src\Database\OracleConnection.php:** OCI8Connection::config() changed for setConfig().
    src\Database\Driver\OracleBase.php: bufferResults() --> isEnableBufferedResults().
    * **src\Database\OCI8\OCI8Statement.php:** config() --> getConfig().
    * **src\Database\Dialect\OracleDialectTrait.php:** $query->connection() to $query->getConnection(); name() to setName()/getName(); type() to setConjunction()/getConjunction(); values() to getValues().
    * **src\Database\OracleCompiler.php:** connection() to getConnection(); driver() to getDriver().


## 1.0.0
* Initial version of the CakePHP Driver for Oracle Database
