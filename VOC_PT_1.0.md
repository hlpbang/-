As a professional intelligent device usage evaluation analyst, your task is to analyze the user comments in the <content></content> tag.
##Analysis Guide
You need to analyze the comments from the following 6 aspects:
1. User: The person using the product.
2. Time: Refers to the specific time of product use, such as morning, afternoon, evening, or holidays, weekdays. Note: This does not refer to the length of product use.
3. Location: The specific location of product use, such as bedroom, dining room, balcony, etc.
4. Reason: The reason for buying this product.
5. Scene: The specific scene and use of this product, such as child monitoring, remote monitoring, energy consumption viewing, etc.
6. Expectation: Refers to the functions or features that the product does not currently have, but the user hopes to have.

##Output Requirements  
Output in JSON format, the JSON object should contain 4 keys:
1. "type": The type of your analysis conclusion, respectively 1,2,3,4,5. Please fill in the corresponding number according to the following standards: \nUser: 1 \nTime: 2 \nLocation: 3 \nReason: 4 \nScene: 5\n Expectation: 6
2. "keyword": The relevant keywords you summarized for this type.
3. "detail": In the original comment, the content related to the keywords you summarized in "keyword". It must be a word or sentence in the original comment. If there are multiple, put them in a list.
4. "reason": The reason you summarized this keyword.

Note: If you summarize multiple keywords, you need to divide them into multiple JSON objects and return them in a list form. Only output in JSON format, please do not output any other format characters and content!

Output example:
[
  {
    "keyword": "Dad",
    "detail": ["My dad","My father","Dad"]
    "reason": "My dad", "My father" and "Dad" these words indicate that the user is a dad,
    "type": 1
  },
  {
    "keyword": "Night",
    "detail": "Turn off the light before bed",
    "reason": "Before bed" this word indicates that it is used at night.
    "type": 2
  }
  {
    "keyword": "Restaurant",
    "detail": "My restaurant",
    "reason": "My restaurant" this phrase specifies the location of product use.
    "type": 3
  },
  {
    "keyword": "Outdoor",
    "detail": "The light outside the house",
    "reason": "The light outside the house" this word indicates that the product is used outdoors.
    "type": 3
  },
  {
    "keyword": "Voice control before bed",
    "detail": "Voice control before bed",
    "reason": "Voice control before bed" this phrase describes the scene of product use.
    "type": 5
  },
  {
    "keyword": "Brightness adjustment",
    "detail": "It would be better if the brightness could be adjusted",
    "reason": "It would be better if the brightness could be adjusted" this phrase is mentioned as an expected function, which is an unmet need.
    "type": 6
  }
]
Here is the original comment:




作为一个专业的智能设备使用评价分析师，你的任务是分析<content></content>标签内的用户评论。
##分析指南
你需要从以下6个方面分析评论：
1. 用户：使用这个产品的人。
2. 时间：指产品使用的具体时间，如早上，下午，晚上，或者节假日，工作日。注意：这并不指产品使用的长度。
3. 地点：产品使用的具体地点，如卧室，餐厅，阳台等。
4. 原因：购买这个产品的原因。
5. 场景：使用这个产品的具体场景和用途，如儿童监测，远程监控，能耗查看等。
6. 期望：指该产品当前还未具备、但是用户希望能有的功能或者特性。

##输出要求
以JSON格式输出，JSON对象应包含4个键：
1. "type"：你的分析结论的类型，分别为1,2,3,4,5。请按照以下标准填写类型对应的数字：\n用户：1 \n时间：2 \n地点：3 \n原因：4 \n场景：5\n 期望：6
2. "keyword"：你所总结的这个类型的相关关键词。
3. "detail"：原始评论中，与你在"keyword"中总结的关键词相关的内容。必须是原始评论中的词或句子。如果有多个，将它们放在列表中。
4. "reason"：你总结出该关键词的原因。

注意：如果你总结出多个关键词，需要将它们分成多个JSON对象，并以列表形式返回。只能以JSON格式输出，请不要输出任何其他格式的字符和内容！

输出示例：
[
  {
    "keyword": "爸爸",
    "detail": ["我的爸爸","我父亲","爸爸"]
    "reason": "我的爸爸"，"我父亲"和"爸爸"这些词表明用户是爸爸，
    "type": 1
  },
  {
    "keyword": "夜间",
    "detail": "睡前关灯",
    "reason": "睡前"这个词表名是在夜间使用。
    "type": 2
  }
  {
    "keyword": "餐厅",
    "detail": "我的餐厅",
    "reason": "我的餐厅"这个短语指定了产品使用的地点。
    "type": 3
  },
  {
    "keyword": "户外",
    "detail": "房子外面的灯",
    "reason": "房子外面的灯"这个词表明了产品在户外使用。
    "type": 3
  },
  {
    "keyword": "睡前语音控制",
    "detail": "睡前语音控制",
    "reason": "睡前语音控制"这个短语描述了产品使用的场景。
    "type": 5
  },
  {
    "keyword": "亮度调节",
    "detail": "如果能够调整亮度就更好了",
    "reason": "如果能够调整亮度就更好了"这个短语被提到作为一个期望的功能，这是一个未被满足的需求。
    "type": 6
  }
]
以下是评论的原文：
