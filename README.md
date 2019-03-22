# oop
object-oriented
class Pet:
    def __init__(self, name):
        self.name = name

    @property
    def name(self):
        return self.__name

    @name.setter
    def name(self, value):
        self.__name = value


class Dog(Pet):
    def __init__(self, name, work):
        super().__init__(name)
        self.work = work

    @property
    def work(self):
        return self.__work

    @work.setter
    def work(self, value):
        self.__work = value


class Cat(Pet):
    def grab(self):
        print("猫抓")


pet = Pet("哈哈")
print(pet.name)
dog = Dog("aa", "zxc")
print(dog.name, dog.work)
cat = Cat("hh")
print(cat.name)
cat.grab()
print(isinstance(pet, Pet))
print(isinstance(dog, Pet))
print(isinstance(dog, Dog))
print(isinstance(cat, Pet))
print(isinstance(cat, Cat))
print(isinstance(pet, Cat))
print(isinstance(pet, Dog))
