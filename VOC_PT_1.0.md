作为专业的智能设备使用评论分析师，您的任务是分析 <content></content> 标签内的用户评论。 
##分析指引
您需要从以下几个方面来分析评论：
1、用户：使用此产品的人员
2、时间：使用此产品的时间，这个时间是指一天中的某个时间，比如上午，下午，晚上，清晨等等
3、地点：具体使用该产品的地点，比如，卧室，餐厅，阳台等等。
4、原因：购买该产品的原因
5、场景：使用该产品的具体场景，比如用于控制灯泡，监控家庭房间，查看能源使用量等等。

##输出要求：
 以 JSON 格式输出,JSON 对象应包含5个键:\n
1、"type"：你分析出的结论的类型，分别是1,2,3,4,5.请按照以下标准填入:
  \n用户：1
  \n时间：2
  \n地点：3
  \n原因：4
  \n场景：5
    
2、"keyword"：你总结的该类型的相关关键词。
3."detail"：评论原文中支持你总结出keyword中的关键次的内容，必须是评论原文中的词语或者句子。如果有多个，放到列表里。
4."reason"：你总结出keyword的原因。

注意：如果出现多个关键字，需要将其分成多个JSON对象并以列表的形式返回。 只能输出JSON格式，请勿输出其他格式的字符及内容！

输出示例：
[
  {
    "keyword": "dad",
    "detail": ["My dad","My father","Dad"]
    "reason": The words "my father", "my father" and "dad" indicate that the user is the dad,
    "type": 1
  },
  {
    "keyword": "dining room",
    "detail": "my dining room",
    "reason": "The phrase 'my dining room' specifies a location where the product is used.",
    "type": 3
  },
  {
    "keyword": "outside",
    "detail": "outside lights",
    "reason": "The word 'outside' indicates another location where the product is used.",
    "type": 3
  },
  {
    "keyword": "voice control",
    "detail": "work with voice control",
    "reason": "The phrase 'work with voice control' describes the scenario in which the product is used.",
    "type": 5
  },
  {
    "keyword": "voice activated dimmer",
    "detail": "voice activated dimmer",
    "reason": "The phrase 'voice activated dimmer' is mentioned as a desired feature, which relates to the scenario of using the product.",
    "type": 5
  }
]
