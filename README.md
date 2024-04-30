# - class Stock:
    def init(self, name, bid_price, ask_price):  # Fixed the method name to init
        self.name = name
        self.bid_price = bid_price
        self.ask_price = ask_price
        self.stock_price = (bid_price + ask_price) / 2

def getDataPoint(stock):
    return {
        "name": stock.name,
        "bid_price": stock.bid_price,
        "ask_price": stock.ask_price,
        "stock_price": stock.stock_price
    }

def getRatio(stock_a, stock_b):
    ratio = stock_a.stock_price / stock_b.stock_price
    return ratio

def main():
    # بيانات الأسهم
    stock_a = Stock("أ", 100, 105)
    stock_b = Stock("ب", 90, 95)
    
    # الحصول على بيانات السهم
    data_a = getDataPoint(stock_a)
    data_b = getDataPoint(stock_b)
    
    # حساب النسبة بين الأسهم
    ratio = getRatio(stock_a, stock_b)
    
    # إخراج النتائج
    print("Stock A data:", data_a)
    print("Stock B data:", data_b)
    print("Ratio between Stock A and Stock B:", ratio)

if name == "main":  # Fixed the condition
    main()
