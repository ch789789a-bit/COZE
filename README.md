import requests

# 调一个免费的天气API
url = "https://wttr.in/Singapore?format=j1"
response = requests.get(url)
data = response.json()

# 打印新加坡当前温度
temp = data["current_condition"][0]["temp_C"]
desc = data["current_condition"][0]["weatherDesc"][0]["value"]
print(f"新加坡现在 {temp}°C，{desc}")
