# nodejs_buildcode
快速生成nodejs下mysql mssql数据库的底层方法,方便创建应用,无需写基本方法
# MYSQL文档地址 
http://zhouxiang.decadework.com:3001/article/1020
（注:mysql提供的默认模板里,部分SQL语法有错误,自行修改）
# MSSQL文档地址
http://zhouxiang.decadework.com:3001/article/1002
（注:mssql提供的模板已经过商用,无BUG,可自行添加默认方法）
# 文件说明
DAL:默认方法
例子:代码太多不显示
Partial：扩展方法（用于你生成后添加方法）
例子:
/**
 * sqlconn
 * 周祥 该文件放置routes 跟目录下
*/
var sqlserver = require('./../mysqlserver.js');
var util = require('util');
/**
 * 继承
*/
var hltx_adminMain = require('./DAL/hltx_admin');
/**
* hltx_admin 扩展
* 周祥
*/
var hltx_adminDAL = function () {
	/**
 	* 继承
	*/
	hltx_adminMain.call(this);
	/**
 	* 下面可增加自由扩展方法 扩展方法不要去基础里增加 免得下次生成 被覆盖了
	*/
	
}
util.inherits(hltx_adminDAL, hltx_adminMain);
exports = module.exports = hltx_adminDAL;
# 其它见文档地址页 有详细说明 不懂可以找博客找到我QQ加我 进行咨询
