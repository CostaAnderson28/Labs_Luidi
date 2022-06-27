class Polinomio:
    "Representa um polinomio de uma variavel"

    def __init__(self, coeficientes=[]):
        "Construtor, onde a lista coeficientes contem os coeficientes para os termos de grau 0, grau 1, etc."
        self.coe = coeficientes

    def __setitem__(self, grau, coeficiente):
        "Altera o coeficiente para o termo do grau dado"
        if len(self.coe) > grau:
            self.coe[grau] = coeficiente 
        else :
            self.coe += [0]*(grau - len(self.coe))
            self.coe.append(coeficiente)

    def __getitem__(self,grau):
        "Retorna o coeficiente para o grau dado"
        return self.coe[grau]

    def grau (self):
        "Retorna o grau do polinomio"
        return (len(self.coe))

    def __mul__(self,p):
        "Retorna o polinomio dado pela multiplicacao deste polinomio por p (tambem um polinomio)"
        c = []
        c += [0]*(self.grau() + p.grau())
        for i in range(len(self.coe)):
            for j in range(len(p.coe)):
                c[i+j] += self.coe[i]*p.coe[j]
        return Polinomio(c)


    def __add__(self,p):
        "Retorna o polinomio dado pela soma deste polinomio com p (tambem um polinomio)"
        c = []
        if len(self.coe) > len(p.coe):
            p.coe += [0]*(len(self.coe)-len(p.coe))
        elif len(self.coe) < len(p.coe):
            self.coe+= [0]*(len(p.coe)-len(self.coe))
        for i in range(len(self.coe)):
            c.append(self.coe[i] + p.coe[i])
        return Polinomio(c)

    def __sub__(self,p):
        "retorna o polinomio dado pela diferenca entre este polinomio e p (tambem um polinomio)"
        c = []
        if len(self.coe) > len(p.coe):
            p.coe += [0]*(len(self.coe)-len(p.coe))
        elif len(self.coe) < len(p.coe):
            self.coe+= [0]*(len(p.coe)-len(self.coe))
        for i in range(len(self.coe)):
            c.append(self.coe[i] - p.coe[i])
        return Polinomio(c)

    def avalia (self,x):
        "Retorna a avaliacao do polinomio avaliado em x."
        p=0
        for i in range(len(self.coe)): 
            p += self.coe[i]*(x**i)
        return p 
    def __repr__ (self):
        return str(self.coe)
    

p, q, x = Polinomio(eval(input())), Polinomio(eval(input())), eval(input())

print(p.avalia(x),q.avalia(x),(p+q).avalia(x),(p-q).avalia(x),(p*q).avalia(x))
