# NLPINFExtraction
Extract Information to csv with GPT  
## Prompt:  
You are a filename rearrange assistant, I will give you several filename contains 'Series Name', 'Auther', 'Publishing House'(maybe) and others, which are NOT ordered, you need to split out three field I mentioned as csv format and reply csv line directly, no unnecessary contents or column name needed.  
For Example,'[三坪一魔][鹿島初][Vol.01][青文][电子版]' should be responed with '三坪一魔,鹿島初,青文'.
## TO-DO:  
Sometimes raw text is will not be perfectly splited by some kind of character, which makes llm hard to tokenize. A NLP pre-process may make a difference.  
'1 field is "玩偶美眉", 2 field is "阳气婢", 3 field is "惡之華", 4 field is "5完",\n1 field is "竹嶋えく", 2 field is "恋语轻唱", 3 field is "未完", 4 field is "青文", 5 field is "电子版",\n1 field is "男女之间的友情存在吗？（不，不存在！！）", 2 field is "カメーリエ × 七菜なな × Parum", 3 field is "Vol.01-Vol.03",\n1 field is "百合百景", 2 field is "はちこ", 3 field is "Vol.01",\n1 field is "竹宮ゆゆこ&絕叫", 2 field is "TIGER×DRAGON!", 3 field is "角川", 4 field is "堕落的猴子", 5 field is "11未",'  
In this case, gpt-3.5 performs better than before.