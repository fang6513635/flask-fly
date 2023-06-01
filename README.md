from flask import Flask
app=Flask(__name__) # __name__ 代表目前执行的模组

@app.route("/") # 函式的装饰（Decorator）：以函式为基础，提供附加的功能
def home():
    return "Hello,welcome to my website"

@app.route("/test")
def test():
    return "This is test"

if __name__=="__main__": # 如果以主程式执行
    app.run() # 立刻释放伺服器
