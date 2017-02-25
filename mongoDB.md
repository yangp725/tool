### 常用shell命令

####进入数据库 mongo

show dbs

use database

show collections

####查询：

db.arch.find({'name':'ATION'})

.limit()

.skip()

设置参数，{\$gt:},(\$gte, \$lt, \$lte)



####导入导出

mongoimport -d arch -c cleaned --type json --file final.json
mongoexport --db test --collection traffic --out traffic.json



####使用mongoDB生成的_id的时间信息：

    // This function returns an ObjectId embedded with a given datetime
    // Accepts both Date object and string input
    
    function objectIdWithTimestamp(timestamp) {
        // Convert string date to Date object (otherwise assume timestamp is a date)
        if (typeof(timestamp) == 'string') {
            timestamp = new Date(timestamp);
        }
    
        // Convert date object to hex seconds since Unix epoch
        var hexSeconds = Math.floor(timestamp/1000).toString(16);
    
        // Create an ObjectId with that hex timestamp
        var constructedObjectId = ObjectId(hexSeconds + "0000000000000000");
    
        return constructedObjectId
    }
    
    db.arch.find({_id: { $gt: objectIdWithTimestamp("2016/12/01")
