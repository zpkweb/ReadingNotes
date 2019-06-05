1：文本
2：富文本
3：单选
4：多选
5：输入框
6：文本域
7：下拉
8：按钮（热点）
9：图片
10：视频


0  未知
1  单选
2  多选
3  判断
4  填空
5  阅读理解
6  问答（简答）
7  完型填空
8  匹配（矩阵）
9  上传
10 组合
11 组合单选
12 组合多选
13 排序
14 拖拽--中博自有题型
15 多任务--中博自有题型




框架
  4.22-4.30
    搭建题库整体布局，调通单选题型流程。
开发
  5.5-5.10
    张文斌：多任务
    林敏：组合+矩阵，拖拽

    赵知博：问答（简答）
    李乐：填空

  5.13-5.17
  
  5.20-5.24

  5.27-5.31

测试
  6.3-6.7

  6.10-6.14

  6.17-6.21

预留
  6.24-6.28



0 未知
1  单选
2  多选
3  判断
4  填空
5  阅读理解
6  问答（简答）
7  完型填空
8  匹配（矩阵）
--9  上传
10 组合
11 组合单选
12 组合多选
13 排序
14 拖拽--中博自有题型
15 多任务--中博自有题型

单选，多选，判断，填空，阅读理解，问答，完型填空，匹配，上传，组合，组合单选，组合多选，排序，拖拽，多任务

2周

张文斌：5(阅读理解)，10(组合)，11(组合单选)，12(组合多选)，15(多任务),
林敏：3(判断)，8(匹配)，13(排序)，14(拖拽)

赵知博：4(填空)，6(问答)，7(完型填空)
李乐：1(单选)，2(多选)，列表


问题：
  界面，需求





录题工具-前端工作安排   
  人员：
    前端负责人-张文斌
    前端开发人员-张文斌，林敏，李乐，赵知博
  功能：
    登录(用户权限)-
    试题列表(筛选，排序，审核)
    试题-单选，多选，判断，填空，阅读理解，问答，完型填空，匹配，上传，组合，组合单选，组合多选，排序，拖拽，多任务
      创建- 保存
      编辑（服务器数据）-更新
    试题预览
  时间：
    
    
  
张文斌：5(阅读理解)，10(组合)，11(组合单选)，12(组合多选)，15(多任务),
林敏：3(判断)，8(匹配)，13(排序)，14(拖拽)

赵知博：4(填空)，6(问答)，7(完型填空)
李乐：1(单选)，2(多选)，列表

#录题

登录(用户权限)-

试题列表(筛选，排序)

审核试题

试题
  创建- 保存

  编辑（服务器数据）-更新

  *组合+矩阵，拖拽，多任务

数据持久化

实时预览（RN）


#做题

新窗口
*试题预览，做题（新窗口-未保存本地数据，已保存服务器数据）
pc,mobile,pad,minipad






文档化

用户行为埋点

用户权限





单选-
多选-
判断-
填空-
问答-
矩阵（匹配）-
拖拽-
其他-

组合
多任务





中博教育-教学项目-前端开发讨论

单选-下拉

单选-富文本

单选-文本

单选-热点


post
创建，做题
get
不带答案，带答案的json


展示json

做题json

解析带答案的json

录题传后台json

data: [{
    "itemBodyContent": "Q= <select><option>A</option>-<input />=<input />.",
    "textEntryInteractions": [
        {
            "correctResponseValues": {
                "Your Answer C": 1.5
            },
            "expectedLength": 10
        },
        {
            "correctResponseValues": {
                "Your Answer C": 2.5
            },
            "expectedLength": 12
        },
        {
            "correctResponseValues": {
                "Your Answer C": 3.5
            },
            "expectedLength": 13
        }
    }
]



{
  baseInfo:{
    "typeId":"8", //试题类型
    "title":"矩阵题",//标题
    "prompt": "<p><span>Background</span><img src="532c.JPG" alt="" /></p>",// 子标题，background
    "score":1,// 分数
    "isSubjective":0,// 是否是主观题
    "source": "", // 试题来源
    "terminal": [1,2], // 终端,0:pc,1,mobild,2:pad
    "analysis": "",
  },
  content:{
    //根据不同题型来展示
    analysis: "",
    // 1:单选，2:多选
    "layoutType": 1, //展示类型
    "styles": [1,3], //样式
    "data":[{
      id: 0,
      value: true,
    },{
      id: 1,
      value: false,
    }]

    // 4:填空，
    "layoutType": 4, //展示类型
    "styles": [1,3], //样式
    "data": "p=<input /> - <input />Q",
    

    // 6:问答
    "layoutType": 4, //展示类型
    "styles": [1,3], //样式
    "data":[{
      id: 0,
      value: "答案",
    }]

    //矩阵
    "data":[{
      // 矩阵行列
      "size":[3,3],
      "cells":[[{
        "id":0,
        "x":"0",
        "y":"1",
        "title":"A",
        "isShow":true,
      },{
        "id":1,
        "x":"0",
        "y":"1",
        "title":"B",
        "isShow":true
      },{
        "id":2,
        "x":"0",
        "y":"1",
        "title":"C",
        "isShow":true,
      }],[{
        "id":3,
        "x":"0",
        "y":"1",
        "title":"1",
        "isShow":true,
      },{
        "id":4,
        "x":"0",
        "y":"1",
        "title":null,
        "isShow":true,
        "layoutType":1, //下拉
        "data":[{
          value: "A",
        },{
          value: "B",
        }{
          value: "C",
        }]
      },{
        "id":5,
        "x":"0",
        "y":"1",
        "title": null,
        "isShow":true,
        "layoutType":2, //填空
      }]]
    }]
  },
  "rule"：{
    //行为规则
    "behavior"：[[4,5],[4,5]], 
    //判分规则
    "score": [{
      "item: [{
        "id": 1,
        "score": 2,
        "answer": true
      }]
    },{
      "item: [{
        "id": 2,
        "score": 2,
        "answer": "D"
      }]
    }]
  }
}
switch (types) {
  case 'radio':
    title = '单选题';
    break;
  case 'checkbox':
    title = '复选题';
    break;
  case 'blank':
    title = '填空题';
    break;
  case 'question':
    title = '简答题';
    break;
  case 'matrixRadio':
    title = '矩阵单选题';
    break;
  case 'matrixCheckbox':
    title = '矩阵复选题';
    break;
  case 'matrixBlank':
    title = '矩阵填空题';
    break;
  case 'multiTask':
    title = '多任务题';
    break;
}


组合
拖拽
下拉
判断
计算


单选题
https://api.zbgedu.com/api/teachsource/examen/getNidExerciseDetail/data?verTT=1555487639949&exerciseId=ff8080814bee5fde014bf45e568b0048

{
  "data" : [ {
    "id" : "ff8080814bee5fde014bf45e568b0048",
    "createDate" : 1425733998000,
    "modifyDate" : 1425903107000,
    "accuracy" : 0,
    "answerResolution" : "The demand curve in a perfect market is horizontal, because they can sell as much as they want at the prevailing market price and nothing at all at a higher price. ",
    "background" : null,
    "context" : "[{\"title\":\"It is diagonal&nbsp;\",\"isChecked\":false},{\"title\":\"It is horizontal&nbsp;\",\"isChecked\":true},{\"title\":\"It is vertical\",\"isChecked\":false}]",
    "exerciseState" : "publish",
    "questionTypes" : "radio",
    "sn" : 1035,
    "title" : "Which of the following statements is true in relation to the average revenue function of a business in a perfect market?&nbsp;",
    "difficultyId" : "ff8080814ab43431014ac3a0b53729eb",
    "sourceId" : "ff8080814ab43431014ac8354fe62f28",
    "versionId" : "ff8080814bee5fde014bf45e568b0048",
    "fileName" : null,
    "sheetName" : null,
    "nid" : 988,
    "isAudit" : 1,
    "isExercise" : 0,
    "createUser" : "",
    "modifyUser" : "",
    "score" : 1,
    "template" : "normal",
    "examenItemScore" : null,
    "sectionType" : null
  } ],
  "state" : "success",
  "msg" : null,
  "code" : null
}



编辑多任务题 试卷-大题

  
  Exercise
    task1
      type
      type
    task1

  多任务题-题干  api
    任务-题干--小题 api
    任务-题干--小题 api

  



  编辑-题干

  编辑-小题

展示多任务题


提交多任务题


判断多任务题













# 题库项目-前端风险控制


### 流程

### 代码


### 测试

### 文档


