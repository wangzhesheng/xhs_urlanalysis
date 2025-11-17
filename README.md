import requests
import base64
# 测试请求
url='https://www.xiaohongshu.com/explore/691482100000000004014e92?app_platform=ios&app_version=8.94.2&share_from_user_hidden=true&xsec_source=app_share&type=normal&xsec_token=CBkeMoLRmwGx3Q1R-IkMnCvEpWymvlifkQ_7uw18L5jEE=&author_share=1&xhsshare=CopyLink&shareRedId=ODw5M0g9Nk82NzUyOTgwNjdFOTg6SEg7&apptime=1763278392&share_id=eef3622c4ccb4f89b2c4029b4d18cc31'
longstr = str(base64.b64encode(url.encode("utf-8")).decode("utf-8"))
res=requests.get('http://127.0.0.1:5000/api/v1/'+longstr)
print(res)
print(res.text)
