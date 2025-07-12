#functions within functions
def sum_sub():
    a=int(input())
    b=int(input())
    c=a+b,a-b
    print(c)
    def mul_div():
        g=a*b,a/b
        print(g)
        def pow_er():
            f=a**2
            print(f)
        pow_er()
    mul_div()
sum_sub()

#with argument passing and no return value
def sum_sub(a,b):
    c=a+b,a-b
    print(c)
    def mul_div():
        d=a*b,a/b
        print(d)
    mul_div()
sum_sub(2,3)

#with  argument passing and return value
def sum_sub(a,b):
    c=a+b,a-b
    def mul_div(a,b):
        d=a*b,a/b
        return d
    print("answer:",mul_div(a,b))
    return c
print(sum_sub(2,3))

#with no argument passing with return value
def sum_sub():
    a=int(input())
    b=int(input())
    c=a+b,a-b
    def mul_div():
        d=a*b,a/b
        return d
    print(mul_div())
    return c
print(sum_sub())

def mul_by(n):
    def inner(x):
        return x*n
    return inner
times_2=mul_by(2)
times_3=mul_by(3)
print(times_2(5))
print(times_3(5))

#functions within functions by strings
def greet(text):
    def inner(name):
        return f"{text} {name}..!"
    return inner
hi=greet('welcome')
print(hi("python"))
