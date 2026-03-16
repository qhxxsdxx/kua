import threading
import time

# 父类：动物
class Animal:
    def eat(self):
        pass

    def drink(self):
        pass

    def sleep(self):
        pass

    def shout(self):
        pass

# 猪
class Pig(Animal):
    def eat(self):
        print("猪吃：拱食吃")

    def drink(self):
        print("猪喝：喝水")

    def sleep(self):
        print("猪睡：躺平睡")

    def shout(self):
        print("猪叫：哼哼哼")

# 狗
class Dog(Animal):
    def eat(self):
        print("狗吃：啃狗粮")

    def drink(self):
        print("狗喝：舔水")

    def sleep(self):
        print("狗睡：趴着睡")

    def shout(self):
        print("狗叫：汪汪汪")

# 猫
class Cat(Animal):
    def eat(self):
        print("猫吃：吃猫粮")

    def drink(self):
        print("猫喝：舔水")

    def sleep(self):
        print("猫睡：蜷着睡")

    def shout(self):
        print("猫叫：喵喵喵")

# 多态演示函数
def demo(animal: Animal):
    animal.eat()
    animal.drink()
    animal.sleep()
    animal.shout()
    print("-" * 20)

if __name__ == "__main__":
    pig = Pig()
    dog = Dog()
    cat = Cat()

    # 创建三个线程，分别运行猪、狗、猫
    t1 = threading.Thread(target=demo, args=(pig,))
    t2 = threading.Thread(target=demo, args=(dog,))
    t3 = threading.Thread(target=demo, args=(cat,))

    # 启动线程
    t1.start()
    t2.start()
    t3.start()

    # 等待所有线程结束
    t1.join()
    t2.join()
    t3.join()

    print("所有动物都演示完毕！")
