# hello-word

2017年05月06日17:14:10  阅读了有关 npm 的一些知识 网址：http://www.runoob.com/nodejs/nodejs-npm.html

//链接数据哭的一些代码
test.js 文件代码：
var mysql      = require('mysql');    //链接MySQL 
var connection = mysql.createConnection({
  host     : 'localhost',    
  user     : 'root',       //数据库的用户
  password : '123456',    //数据库的密码
  database : 'test'       //数据库的名称
});
 
connection.connect();
 
connection.query('SELECT 1 + 1 AS solution', function (error, results, fields) {
  if (error) throw error;
  console.log('The solution is: ', results[0].solution);
});
