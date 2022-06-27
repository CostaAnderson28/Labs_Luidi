a = eval(input())

def v(x, y=0):
    n = 0
    if y < len(x):
        while n < len(x):
            if x[y]<x[n]:
                n += 1
            else: 
                y=n  
                n+=1
        return x[y]
            
def ord(x,y=0):
    c = x[y:]
    i = v(c)
    if i < c[0]:
        x[y] ,x[c.index(i)+y] = x[c.index(i)+y], x[y]
    if y < len(x)-1:
        return ord(x,y+1)
    else: return x

print(ord(a))
