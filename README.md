# FinancialLiteracy

## import 包
"database/sql"
_ "github.com/denisenkom/go-mssqldb" 微软sql server数据库


var db *sql.DB sql包Db类型

数据库的连接字符串： ConnStr :=

sql.open函数（数据库驱动名，
db ,err := sql.Open("sqlserver", conStr)

err

连接到数据库：
加载目标数据库的驱动，包含造作逻辑
sql.Open() 参数： 数据库的驱动名称，数据源名称(不连接数据库，不验证参数，把数据库所需的structs设置好）

sql.DB 用来操作数据库，由sqk包维护（不是实际的连接，是用来处理数据库的），

如何获得驱动：
sql.Register() 函数，数据库驱动的名称和一个实现了driver.Driver 接口的struct，来注册数据库的驱动
sql.Register("sqlserver", &drv{}} 没写但能驱动（sql server的驱动，是这个包被引入的时候自我注册的）

驱动自动注册：
go-mssqldb 包引入，init函数(导入包启动database、sql）

安装驱动： go get github.com/denisenkom/go-mssqldb  


db.PingContext() 验证数据库的连接是否有效  
context.Background()

增删改查：  
查询：  
query  
QueryRow  
Queryontext  
QueryRowContext  

type Rows strcut{} (query/Queryontext)  
func(rs *Rows)Close()error
func(rs *Rows)ColumnTypes()(*ColumnType,error)
func(rs *Rows)Columns()(string,error)
func(rs *Rows)Err() error
func(rs *Rows)Next() bool
func(rs *Rows)NextResultSet() bool
func(rs *Rows)Scan(dest ..interface{}) error

quertRow
type Row strcut{}
func(r *Row
