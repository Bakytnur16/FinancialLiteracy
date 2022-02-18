# FinancialLiteracy

## import 包
"database/sql"
"github.com/denisenkom/go-mssqldb" 微软sql server数据库


var db *sql.DB sql包Db类型

数据库的连接字符串： ConnStr :=

sql.open函数（数据库驱动名，
db ,err := sql.Open("sqlserver", conStr)

err
