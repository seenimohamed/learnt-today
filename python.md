# learning python

## Quick notes about yield

url : https://stackoverflow.com/questions/231767/what-does-the-yield-keyword-do

```
#Example 1
def yieldexample() :
    mylist = range(3)
    for i in mylist :
        yield i*i
    print mylist

if __name__ == '__main__':
    # train()
    ye = yieldexample()
    for i in ye :
        print i
        
Result : 
0
1
4
[0, 1, 2]
```

```
#Example 2
def yieldexample() :
    mylist = range(3)
    for i in mylist :
        yield i*i

if __name__ == '__main__':
    # train()
    ye = yieldexample()
    for i in ye :
        print i
        
Result : 
0
1
4
```

### Notes :
1. yield returns a generator object. each value can be executed only once (similar to stream in java). 
2. function will go till keyword yield once execute, then only will execute remaining part of the function. See example 1.
---
