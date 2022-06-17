class Matriz:
    def __init__(self, n,m,v):
        k, i, j= 0, 0, m
        M = [] + n*[[0]]
        while i < n:
            M[i] = v[k:j]
            i += 1
            k += m 
            j += m
        self.data = M
        u = list([0]*len(self.data[0]) for x in range(len(self.data)))
        self.vazio = u

    def __repr__(self):
        return (self.data)

    def __add__(self,other):
        for i in range(len(self.data)):
            for j in range(len(self.data[0])):
                self.vazio[i][j] = self.data[i][j] + other.data[i][j]
        return self.vazio

    def __sub__(self,other):
        for i in range(len(self.data)):
            for j in range(len(self.data[0])):
                self.vazio[i][j] = self.data[i][j] - other.data[i][j]
        return self.vazio

    def __mul__(self,other):
        t = list([0]*len(other.data[0]) for x in range(len(self.data)))
        for i in range(len(self.data)):
            for j in range(len(other.data[0])):
                for k in range(len(other.data)):
                    t[i][j] += self.data[i][k]*other.data[k][j] 
        return t

T = str(Matriz(input()))
for i in range(len(T)):
    if (T[i] == '+') or (T[i] == '-') or (T[i] == '*'):
        a = list(eval(T[:i]))
        print(a) 
        b = list(eval(T[i+1:]))
        print(b) 
        c = T[i]
        a = Matriz(a[0],a[1],a[2]) 
        b = Matriz(b[0],b[1],b[2])
        if c == '+':
            print(a+b)
        if c == '-':
            print(a-b)
        if c == '*':
            print(a*b)
        break
