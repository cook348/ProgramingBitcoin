# Chapter 1 - Finite Fields
Settying up Jupyter in VS Code is pretty neat.  That prevents me from having to go back and forth with the browser.  

A finite field is a set of numbers and two operations (addition and multiplication) that meet 4 criteria:
1. the set is closed (a+b and a*b are in the set)
2. additive identity
3. multiplicative identity
4. additive inverse
5. multiplicative inverse

Addition and mutliplication can be defined in a different way than we typically think of it in order to satisfy these requirements.  This can be done using modulo for example.  

a +f b = (a+b)%p
-f a = (-a)%p
a -f b = (a-b)%p

multiplication is very similar:
a *f b = (a * b) % p

and from there exponentiation:

a ^f b = (a^b) % p

Division is also closed, meaning that dividing any two numbers in the set results in another number in the set, which is a little wild.  

Fermat's little therom is used to derive division in the finite field.  
n^(p-1) % p = 1  where p is prime

Optimization note: in Python the pow function that takes a third argument applies the modulo of that argument after each round of multiplication, which is more efficient for some reason.  

The redefining exponentiation stuff went a little over my head, but hopefully that isn't important.  


# Chapter 2 - Elliptic Curves

The ellpitic curve is:
y^2 = x^3 + a*x + b 