# foxittydef add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "خطا: تقسیم بر صفر مجاز نیست!"
    return x / y

def main():
    print("ماشین حساب ساده")
    print("1. جمع")
    print("2. تفریق")
    print("3. ضرب")
    print("4. تقسیم")

    choice = input("یکی از گزینه‌ها رو انتخاب کن (1/2/3/4): ")

    try:
        num1 = float(input("عدد اول: "))
        num2 = float(input("عدد دوم: "))
    except ValueError:
        print("لطفاً عدد وارد کن!")
        return

    if choice == '1':
        print("نتیجه:", add(num1, num2))
    elif choice == '2':
        print("نتیجه:", subtract(num1, num2))
    elif choice == '3':
        print("نتیجه:", multiply(num1, num2))
    elif choice == '4':
        print("نتیجه:", divide(num1, num2))
    else:
        print("گزینه نامعتبر!")

if __name__ == "__main__":
    main()
