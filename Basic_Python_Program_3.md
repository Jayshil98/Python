# Probability

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSWtSV9K1aRNeHXbVnIcduuQJmYCk5ixbOMYudlGm3Y0wmXUC87&s)


```python
#sample space
cards = 52

#event outcome
aces = 4

ace_probability = aces/cards

print(round(ace_probability,2)*100,"%")
```

    8.0 %
    


```python
def event_prob(event_outcomes, sample_space):
    probability = (event_outcomes/sample_space)
    return round(probability,1)

#sample space
cards = 52

#Probability of drawing a Heart
hearts = 13
heart_prob = event_prob(hearts,cards)

#Probability of drawing a Face card
face_card = 12
face_prob = event_prob(face_card,cards)

#Probability of drawing the queen of hearts
queen_hearts = 1
queen_heart_prob = event_prob(queen_hearts,cards)

print("Probability of drawing a Heart is: "+str(heart_prob)+"%")
print("Probability of drawing a Face card is: "+str(face_card)+"%")
print("Probability of drawing the queen of hearts is: "+str(queen_hearts)+"%")
```

    Probability of drawing a Heart is: 0.2%
    Probability of drawing a Face card is: 12%
    Probability of drawing the queen of hearts is: 1%
    


```python
![]()
```


```python
#Mutually Exclusive Events
#P(Event_A U Event_B)=P(Event_A)+P(Event_B)

#sample space
cards = 52

#Calculate the Probability of drawing a heart or a club
hearts = 13
clubs = 13
heart_or_club = event_prob(hearts,cards) + event_prob(clubs,cards)

#Calculate the Probability of drawing an ace, king, or a queen
aces = 4
kings = 4
queens = 4
ace_king_or_queen = event_prob(aces,cards) + event_prob(kings,cards) + event_prob(queens,cards)

print("Probability of heart or club is: "+str(heart_or_club)+"%")
print("Probability of drawing an Ace, King, or a Queen is: "+str(ace_king_or_queen)+"%")
```

    Probability of heart or club is: 0.4%
    Probability of drawing an Ace, King, or a Queen is: 0.30000000000000004%
    

# Intersection of independent Events

![](https://d26tpo4cm8sb6k.cloudfront.net/img/probability/probability-1.png)


```python
#Intersection of independent Events
#P(Event_A () Event_B) = P(Event_A)*P(Event_B)

#sample space
cards = 52

#outcomes
aces = 4

#Probability of one ace 
ace_prob = aces/cards

#Probability of two consecutive independent aces
two_aces_prob = ace_prob*ace_prob

#Two ace prob percent
two_aces_prob_percent = two_aces_prob * 100
print(round(two_aces_prob_percent,1))
```

    0.6
    

# Naive Bayes or Bayes Problem Implemenation

![](https://cdn1.byjus.com/wp-content/uploads/2018/11/maths/2016/03/03054449/Conditional-Probability.jpg)


```python
#sample space
cards =52

#outcomes
kings = 4
face_cards = 12
```


```python
#Probability of King
king_prob = event_prob(kings,cards)
print(f'King Probabiliry is {king_prob}')

#Probability of face card
face_card_prob = event_prob(face_cards,cards)
print(f'Face Card Reader is {face_card_prob}')
```

    King Probabiliry is 0.1
    Face Card Reader is 0.2
    


```python
prob = ((king_prob * face_card_prob) / king_prob) * king_prob / face_card_prob
print(f"Probability that my card is the king, given that the card is the face card: {round(prob,1)}")
```

    Probability that my card is the king, given that the card is the face card: 0.1
    


```python
# Naive_Bayes Theorem
#P(A/B) = P(B/A)*P(A) / P(B)

#sample space
cards =52

#outcomes
kings = 4
face_cards = 12

#Probability of King
king_prob = event_prob(kings,cards)

#Probability of face card
face_card_prob = event_prob(face_cards,cards)

#Probability that my card is the king, given that the card is the face card

#P(KING/FACE) = P(FACE/KING)*P(KING) / P(FACE)

#P(FACE/KING) = P(FACE () KING) / P(KING)

prob = ((king_prob * face_card_prob) / king_prob) * king_prob / face_card_prob

print("Probability that my card is the king, given that the card is the face card: "+str(prob)+"%")
```

    Probability that my card is the king, given that the card is the face card: 7.699999999999999%
    

# PERMUTATION

![](data:image/png;base64,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)


```python
#Permutation:- (nPk = n!/(n-k)!)
#Permutation are the number of ways a subset of a specified size can be arranged from a given set, generally without replacement.
#To find the number of permutations pocket Aces,from which you only pick 2, you'll consider the full set of aces to choose 
#from 4 and you also consider the number of aces that you actually choose 2:

import math
n = 4
k = 2

#Determine permutations and print result
Permutations = math.factorial(n) / math.factorial(k)
print("Permutation is: "+str(Permutations))
```

    Permutation is: 12.0
    

# MANHATTAN DISTANCE

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQtgmYHWkNdHJ7apY4NKbx7D2DI1_F-Lp59VpPH82UwoKEENOFy&s)


```python
def manhattan(x1,x2,y1,y2):
    return abs(x1-x2)+abs(y1-y2) #abs means absolute value that is |a-b| or |a+b|
x1,y1 = map(int,input("Enter first data point: ").split()) #split is used for adding space between two inputs
x2,y2 = map(int,input("Enter second data point: ").split())
print("Manhattan distance: ",manhattan(x1,x2,y1,y2))
```

    Enter first data point: 1 2
    Enter second data point: 3 4
    Manhattan distance:  4
    

# EUCLIDEAN DISTANCE

![](http://distancebetweentwopoints.com/wp-content/uploads/2013/10/distance-formula-example.gif)


```python
def euclidean(x1,x2,y1,y2):
    return ((x1-x2)**2+(y1-y2)**2)**0.5 
x1,y1 = map(int,input("Enter first data point: ").split()) #split is used for adding space between two inputs
x2,y2 = map(int,input("Enter second data point: ").split())
print("Euclidean distance: ",euclidean(x1,x2,y1,y2))
```

    Enter first data point: 1 2
    Enter second data point: 5 6
    Euclidean distance:  5.656854249492381
    

# MAHALANOBIS DISTANCE


```python
#MAHALANOBIS DISTANCE: M = ((x-x_bar)**2/variance)**0.5
def variance(x):
    s = 0 #sum = 0
    mean = sum(x)/len(x) # formula of mean
    for i in x:
        s+=(i-mean)**2 #(x-x_bar)^2
    var = s/(len(x)-1) # formula of variance
    return var

def MD(y):
    su = 0 #sum = 0
    mean1 = sum(y)/len(y) # formula of mean
    for j in y:
        su+=(j-mean1)**2 #(x-x_bar)^2
    var1 = su/(len(y)-1) # formula of variance
    M = (su/var1)**0.5 # formula of mahalanobis distance
    return M

n = []
print("Enter Observations: ")
try:
    while True:
        n.append(int(input()))
except:
    print("\nVariance is: "+str(variance(n))+"\nMahalanobis distance is: "+ str(MD(n)))
```

    Enter Observations: 
    1
    2
    3
    4
    
    
    Variance is: 1.6666666666666667
    Mahalanobis distance is: 1.7320508075688772
    

# INTEGRATION

![](https://cdn1.byjus.com/wp-content/uploads/2018/04/Integration-Formulas-250x340.png)


```python
def integration(pow,val):
    return (val**(pow+1)/(pow+1))
x,y = map(int,input("Enter power and value for integration: ").split())
print("Integration of entered power and value is: ",integration(x,y))
```

    Enter power and value for integration: 4 2
    Integration of entered power and value is:  6.4
    

# DIFFERENTIATION

![](https://www.brainkart.com/media/extra2/K4urYXK.jpg)


```python
#d/dx (x^n) = nx^n-1

def differentiation(pow,val):
    return pow*val**(pow-1)
x,y = map(int,input("Enter power and value for differentiation: ").split())
print("Differentiation of entered power and value is: ",differentiation(x,y))
```

    Enter power and value for differentiation: 4 2
    Differentiation of entered power and value is:  32
    

# DETERMINANT OF MATRIX

![](https://codeforwin.org/wp-content/uploads/2015/08/Determinant-of-2x2-matrix.png)


```python
def det(matrix):
    return abs(matrix[0][0]*matrix[0][1] - matrix[0][1]*matrix[1][0])
matrix = []

print("Enter 2-d matrix rowwise: ")
for i in range(2):
    a=[]
    for j in range(2):
        a.append(int(input()))
    matrix.append(a)
print("Determinant of matrix is: "+str(det(matrix)))
```

    Enter 2-d matrix rowwise: 
    1
    2
    3
    4
    Determinant of matrix is: 4
    

# SIGMOID

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQXRsHStpaf9AnADBKMvZslRHZkqS-zaVqZ0B_-I7CO6AmF9wUl&s)


```python
#sigmoid function: 1/(1+e**(-(wx+b)))

%matplotlib inline
import matplotlib.pyplot as plt
import math
def sig(w,x,b):
    return 1/(1+(math.e)**(-(w*x+b)))
# w,x,b = map(float,input("Enter w,x,b: ").split())
print(sig(w,x,b))

plt.plot([2,3,4,5,6,7])
plt.show()
```

# Tanh

![](https://miro.medium.com/max/1288/1*WNTLbBRWFiHPoXvyZ6s9eg.png)


```python
#Tanh function: 2/(1+e**(-2x)) - 1 or 2sigmoid(2x) - 1

%matplotlib inline
import matplotlib.pyplot as plt
import math
def tanh(x):
    return 2/(1+(math.e)**(-2*x)) - 1
x = int(input("Enter x: "))
print("Value of tanh is: "+str(tanh(x)))

plt.plot(tanh(x))
plt.show()
```

    Enter x: 2
    Value of tanh is: 0.9640275800758169
    


![png](output_40_1.png)


# STANDARD DEVIATION

![](data:image/png;base64,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)

![](data:image/png;base64,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)


```python
import math
def variance(x):
    s = 0 #sum = 0
    mean = sum(x)/len(x) # formula of mean
    for i in x:
        s+=(i-mean)**2 #(x-x_bar)^2
    var = s/(len(x)-1) # formula of variance
    return var
n = []
print("Enter Observations: ")
try:
    while True:
        n.append(int(input()))
except:
    print("\nVariance is: "+str(round(variance(n),1))+"\nStandard Deviation is: "+str(math.sqrt(variance(n))))
```

    Enter Observations: 
    1
    2
    3
    4
    
    
    Variance is: 1.7
    Standard Deviation is: 1.2909944487358056
    

# VARIANCE

![](data:image/png;base64,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)


```python
def variance(x):
    s = 0 #sum = 0
    mean = sum(x)/len(x) # formula of mean
    for i in x:
        s+=(i-mean)**2 #(x-x_bar)^2
    var = s/(len(x)-1) # formula of variance
    return var
n = []
print("Enter Observations: ")
try:
    while True:
        n.append(int(input()))
except:
    print("\nVariance is: "+str(variance(n)))
```

    Enter Observations: 
    1
    2
    3
    4
    5
    a
    
    Variance is: 2.5
    

# COVARIANCE

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAATkAAAChCAMAAACLfThZAAABSlBMVEX///8AAACUlJSLi4t5eXlvb2/8///8/Pz19fXq6ur4+Pi2trb1hADU1NSDg4MjIyOpqanc3Nzv9/rHx8cgnNZfreDOzs7w8PBBQUExpNjg4OCgoKDX19eampqsrq+0tLQQEBAoKCi+vr47Ozv2jh9LS0tlZWUyMjKPTgD4qGUcHBxSUlJra2tfX1/1kjA+Pj74ggD5z63yhgD5uYn99u/5wpf84tH5snn72cH87eMqFgOSVRX1lTtEsOY5hbBRSUT+7uj47tw7kcJIdI4vEwY+EgAWCgBSNRD/myf/kwzPmGbXllmKnqWBoLfNmFi6knNMnce9lWgPoej0ok1aMwCYnJEfBwCYSgBLJwD0nEv2yqL2u4z417T2t3pJru3zolsjcaIhY4oYUGpTRDn94tRIbINAe6BNXWdMWF9MSj9LbnxHgamj0eyCvuaRDLToAAATNElEQVR4nO1d+WPiRpaux6ESQoAYPAiLw0JIZgw+hIwxZBwnuDc7k+xONtOZPWy3p2c3053OZPf//3XfqxKXwdiddmwM+roNQqqSVR/vrMuMRYgQIUKECI8JtTYH67mf6WWgBPMwn/uhXgQAPvvsnz777KvPvvoK3wj/DKnnfqgXAfjDH13362+q//Kvf/r2axfxx99HzD0IxJz+b9/9eet1THcFfnXmlCeo8QSAv7jBN999i8R97d5mTmEKgl7uuclDykwKy5IKf2j5YW/40LJPCfjD13/e+mYicbdkrvN9oB+e3s9K7/TNQ6nje6eE/oOpfutfPfx7eTrAX7797tvt7X8fSdy0nVO6Z35wuXf4Vjw3V0hehKjgIb3LYyqonPpnCp0XwqHwSUM5FwXkeXlXnb4k/UqUkhewHlWlm1NxPqooZXlP77DR2RUC/Mfvf4f4z9+N8V8T5i71wwE+e1cRCskkdUx84FKPRyo9OOnJg9F1WXysyKJw2HZdH3DihbPRLRT5lSijW8iaiiwhmFPGN1wZJLKJGWTx3yie6/vBgMSAnvnq0r3EBlzddLBNJzd95eSte3iMV97c9Pf0bu8aNerNnuvuDRTWu+mcHB4eE1Hd60v3sKMoncvgrBO2XA++lMZueHPo7vXwm7k56aBJuL7uX7p73c7Z4WlXUfqneMf+cUfK3ODmjH7/KuG3nxP++vkEf/38N+G1Y38vPFLe+oenun6jdHxXYQPf/1Lxz44P9VNFOfEDPeh2/LeK8vbw+DLA6z0/8C8DHXntnunuqdtRrnT3OAhC6nS9y0hDu7p/uaf7SB2W10+ZG/hnbuBS1T26L5rXE/9YMtf3904Dv/ccDN2F7a2tn8/Pz7fw53x762/v/3axtTVi7lIfmea+7naVXoBqpus9pRN8ryhDdHpBgC3Ug05X6eh7TBmgqBzi9Z4evGFXdPFaP8NzvKu7A+TzTN5Nd9FH7HWRESToOLhkyNxlt8sOgz2s6h4rfT3geF9iTg+Z412mXAcPcFVPh+2t918gtvDnh/P/xtTrf16PmTsLrsKj0+AG1fYSm7CnX6MAksoO3py4KD0n+lvUPWQOTZ/WvzrT+6yno7voomghj32q3vcvBwPkuRsyRx5iwFwdZajr41ndp2JEOsNvR+GBuO80c4rS65zib1ohIHM/EHM/IXMXt5h761+HMvdWR01TToMT1g/OOHHCbnTfdYOubBwj5pSrwA/cYIo57grFRPnTfV/X/YFkDrkivyO1NtCHzA+GLGROJ+bc28wpwzPfd4MVY46w/XobD15vSYyYuw7OQv9ID8+VvQBDiSC4Eiz56HbHsiGYQyXtK2/HMufrnLv+gKKJjv79oPf3v/ekc5WMsS6KF31CL6SLo0XMhXZOufRvlDf+ajH3+uLdu3evXr/C14uLd6/enU+YG/pk6CgguCYH0HV9DF9Pg8MAo95TbE53xBwXzAm5O5tmDj+dUKDR0w+VSZah+8Scgkx1yJu4HJn7kgnmRMjCBHNXOv7Km5HMkZh3Vk9bPS+0c++/8L54NWEOH9y/6fc6HWWg61fdU/0QAxS04S7GWadI0+lt5g67b/SxtpIBu/KDq0F/gKTsDbr9obxtyBz6ALc3PCNuFjBHvuJNRw9C5gK9MzxbMW19ff7hxx9/3MKfDxfn+PJ+YueYcoz2yfdRYDoBvQ8pT3ApFkFH6/sB2ahrnz52/O+V7iEaM9fvKOhFyfRj85FgrHeiDFzdx29B3JP7/kDe/pRuvocxte4jqQqKNBOHXbKIqKC+fujvKWhuO+JBXP1stXyrBL3ftnMoF91+p9PHZrDum04f24j/v8TgA5OlYacz7A41pTugVncHaJ6wcK877CraAKnhwyGlCSix/WF4H2He5AV5e7zYo+xhSF8JGww1xgd4qNBnruDdON5WGQy6XOldvekOhqvF3Huv3W5v4c9PqK3t9qspmWNhrsnH2VeYTSmTfGzSBxQmXuHLuI4sO11uuttIUSZp7q1S4e8YHa9Y8hVGJT9gVOJJO/ePWeYi3IXtrYv3iC16uaDD84i5hwHt2wXiNb2Iw+8i5h6G6RziHA9/iLT1gdh+TXnrD9sinvsZ7dy7iLmHQWorRiWop/RyMR2VRFgC9BCvEFv48+47zL7+cR4x9zCQtnreT1v48sXPUVTyEaDs68OHH7fx5cPFz+0PtyPhCHdhkntNEDF3PxT2v7+dw/+tWJqzmlg4iBkxFyFChAgRIkSIEGGjwFdwet/TwzQI2u3T+bRRy9xdK3k081EzNnBRSR4gl7PnloQkoFSH9p21GjA+LO4z5kBy84QwD7FFp7OQQvacu2qVJsw16bA4J7TrjxFzTgvAYGwfkmL2bxYsVsAT+RJAljEDsgC7GisjmTXYIeZMD+AoxbAaJCyIMxYHaKKCg9cGu7ABIpiHrJlKsQy0rQOkJQFQVZmUuSQUVbAzcaQuDVCkdwMKeJwm5rREvgC7zGyAaRL9cYhXbDAZMu2A/cytegrkaeVbE1mymImGLYHUELLQrqPxIvkifUxDmaF4TTOHfsFq2FJxiTm7xdgOSinYJLkbsK4pD3GuquyIqEAGE2GbsxAzKqSBFvGgpcnkHcwwp+2CbcOYORXQU5DWQo6N77LWCO1cG1BHoTTFnHiPQYauMcFcaYa5GIpje8IcBw8dBd5sg5iL01sV1bGG7Z4wJyK0IloyCzlJo0TlUZkdtHX7kjnSSJI5D7igv4Q19qG4OcxVyHViStCAJjRVlgzbnJDM4XsTIE8eQryrYkFwjdUBSWzZAMKllol+NJh1SNA6WDa+y1qDp1R5UDDIN5gpGU6M3lnGcPAoDbV0jcJltZZWsYaZElc0IsgxLHETdYcsIzPNqdoR0ncHxRGWxq5OxNwaITIIvxilVo5g1x5aISsrtLK/5lOtFu7rD7x98d4OxM2R1/SyKKdSmD+3s2wrlVT6U59nhaEiNE0NO6/S9t1SwrkKc/2q5dJSsWqtr7/j4SY8Yd+qTS3lbLQbwKjQ6CW7f7s+VEbX5hSZXhz7sR94dYBZcSqVsqSSVjAtSZFcWbNKm7K4uJCHW/w4wEwL5ZVbs0or6mMFDdOhtcUkgeOsWqK+1SLLUJ/XFIpgMJOyRylizDCLYR/ZLrJZJQaLMxUOiGLbQ7dsrLGTKLXCtnG2n8CXdos12mxWiLLAkzm81hSMqlD1PFHBi2H9JtKfYxV1qnwBCsyioD6ReKpmPAO0uiepk0SwFByAynZoQC7lOI6QSN46EOLmlalCMQ12pUgVbIN6WS2GclcWWo4VBOV2gpVJ7uIHz9Oop8GBPRIXwRx1tiIf5CucRqkp1TINggLBnAltyJGkMcEcpy4ci5VJXw2sIBQ6DqydZGvOXGKyu12SGqtCEzRWrY3cpdhSp9kUEUldBmixBto1Ou/FSce9ch35LowrMOq0LgjTl1itNIKHzZk7nVfnzvHKPTF+dcr9kYdgu3UNkqxcmy3Ec0ckXqJsCoqJuriCHoL8R64smZtCiYZOGGsYD2vSU6FcB7DnWMImLGBpN770Vulpr0hRB7lJ9K/l6SZbUMabl9Hnyl+gslFfoxgOrpPUZmeD3h3RBa6uWM9rCWKVynTLQsKaOwsKp2Ce4gksgJyNCDW2vsPSdBPDyU8HYgWDOl1rC3RPjOA1ScmLsxw5grOdxv2teULEpZhw8nKV8BxxhxIzDub5OO6nkOpumI5EWqZfBVhSFr+EuSS1VqehlXnBMoECHH4rzHtuwG4oZAamTa0U+kJSFtAwhxRDaRbGCHKwR4S0sbtnrcznTMVl2mUtmA5U0A5g/qspgAgSzdUizho9aQYZUlsNPIHWvL5PcSzm2G3Wliri5UgcyHCFFffDHLX0uM8TX5DVW4llJuK5kBl1uGeJEgOFrNmmKICVYuJqPOzRoAiVLFBmxJyVkagsuusmYCxzHglPBk1JGeg/a1TpbIK0lLo7NCibZMAzizwuIpl4SqxAXMcZhfNExgFpZQEyFF+18ckOxNO1oBmWSzaEoo6tfjLs4w7tXjb+pHhyohYgG6prTHoGJPEoSSFqnCjJ2uQgWGGHwjuPLF/ZC+tlChKrZbafErwJyfROAj1/KWOI2So1oJCehIuMIPlXEN5CZOkHC2c8/pLfy17+uEK5AdBWmdWGlrB5ZlLkk2jVYqixasJIoXfgUp0fMYzPim678tKY72XCaI6OxPBAUQT4j9hbkQWbrydzrDwSr7RFsdw+5RLG4+3zn23kYuvJ3KwRSsanxl4eBVmvhqq/jsz92sjalPltAHOP7gcxaalB3lh/5h4dlO7V207E3EeDmCtiXvzcz/HyILoYdiFi7qMhmEtFzH08ijvkdgorNigTIUKECBE2Fb80Fdr4PRA4M8rlcnV+r4P8frNUXUZObvdXfKwXgTo0m7m5FQUYV8b2F+xqMDkBR7evbRqaNr2OpiHx8KAs+m1nzoo3Pl5pAKVQYzdWaSVzzPIA2iYmzvtiso8BYpDUqgOU6CxmhUkDf4ixBkBaMMd2gPY62FQ07Xw+r7EcFNPgsQpAloyeCnBQwbd4itYC5wEKyF2xjZIIELdsGsUq0dJYs7R0StJao0lTOlJFkrQDSOUhNPzmrtiEg5kVQVFcLDQvQJmBTaOBNbly3USx29hh0qZNtqtGo8xVyOSllhJQslSzAQ3BXEzMs6FZfjSEmqHl+iXWFhNp1nkl0FJIO+eQgCXAmt4xJw75BGTYAuaoNJ4+AFXTtA33ECloMhNswRGhUmRaAzQPuHmbOcijsOWJuTJtYrK5f+Q7JzsEabagWOUip6gk6GMZz7YAcuIs2bkisofnbbHRQZOmt7Zam9ufaAqh4cxKO+gluSldJS+m0ykaj9/JcFOc5aYm3qFpidUcol4x7Wzg9mm/ELQdSYRfgqZ3f5kIESJEiPDpiIdbbjx4oaoDcjryxveORXgAFq2xGWPReprKsom0vLD++WLYwgWbakzDnltrY82vA5vG7gqsgfi14IXrmeSnbHJpYad1+8w9C0CXr3J82XAgkc9kMqEeYjqtqrR8R51WM66pXJzjYo0AD/8hNJRRKsrV2U2ONVVsC8NXblnw44HWSmfkAaPNSjjLUK8MzM5mT9FM7RJeFIv4WQ1YuHyKpiDSFjEmzMpejJa1JEBjsXVexD+13eQOKW0WtCqo2ozl34F8QZAhtFlrHYTbdFSPqG/RZGlIqdMGz6QeNBsLp+f0e53gtUaNJiIYt3fBYRmxuUamkpEMtkt16k2s0uooo9GGdkl0aNMifgvSbL/EHFpiosoKnB3k8HzxvnXGLx218fhG7Ii0tkBjbRYxkwI7VENL+hDBXL6wD/tyKXeChlIau6S8Ym18BisIhXYgJSawF18Mc4vip3t2jijAePAcDZiQF1TMyuy8gnhLDIJI3+uAEw6JiJ0mDMigwhdmAxAwaO0j7Sz2UmDO86QuDbloOGRUR6wgRnFpNFh+as8vWtdeSKK9Z205NBxjMUtu9EUVVKCNhm4xl20IP7x6HoLHmgAL8shFS7zMZeGtCVMt5uhnVTyB/tWauVHdw4JJxqFyuzbdep9G85xZ5iy5xnbp3gvPAROgWtiZfypzYUhfXbIBAkDpqNFo1GV2kEgwJ46xWLmamt6+o5JFgpy4VrBvV2+T3xCT/POz+YWKNoAv2mrimXE0/ssmqjUdpZcXbm2w7PnL4i/MGGUplqaIUO40jPW5Ad88Jgl5Cu5u19m16TW5avuAVca7XGRB/DWOOknVkce8KuPUB19DG89ZGcR6Q5PlHjzEXVi2N4KZnie1YNVgvtPfbAh/raXVFUv5jVHwWhb7+RtiVXoKdsR+NUV6F7FEimYRIJ9s/9GW0C8gwliQ1WveaAvJFWMuPkqkbfKAXhPt8Q7SyVWx3VSiFbfl5XYd9S893hyzAbbYRohUaMVa9FQYbebDRdhJBhqjUW8facqLsxBODMUAw6FgIi6Ds3CzkowoxIzYUyK+Gp0mhTAQlczRiqIycNRUDSnjFO+Hc304GEkibcGGjZzF95NPiN2VcLKcQU726uTIM5B7SMn1fy2KJZrJMsokp/wo4bVouqLs4mClXJ3QWjWH95Qogm0UnRr60GpK7gvmiYiWdiwso7ewPYwVHHLCtJfJKIANNytxlvxBuwUo3K1nqvPyzGX+AEQOYQDkRAjqtMl6YYKttlHACl7FEDmoSK0+qcPCaGC43CCGGmMPjZ8csUtkKMwvCHzRJ7EZpjH67JGto2iFs6NPSYFIokFMWLOnwo+cmMgsukLXBNZoNiOPa0zLAu2CnPqUaE7IKxxQFjLNnMPqottkTf8KiLpgQ72PRZb2CIR0fXeWOZQ6wdxabrPM+WOEu2JHOzDS6GQWMVeOplvdBfFXSDBszJVC5qxiRvw1T8lcuv6cD7fSgJC5IhQ9wVzcbokMJmLuHkhtxeCj3W5H2voxSOyThyhTJ+/GeIjHgRhpCDsWZpgT3TTrGpU8CigSjlN+p8ZmWCpTp8MaRcKPj3I4fXCeIgx7vOrc2QhjOHdn/FqkqxEiRIgQIUKECBEiRIjwovH/Ov73Me+qoc4AAAAASUVORK5CYII=)


```python
def covariance(x,y):
    s = 0 #sum = 0
    mean = sum(x)/len(x) # formula of mean
    mean1 = sum(y)/len(y)
    for i,j in zip(x,y):
        s+=(i-mean)*(j-mean1) #(x-x_bar)*(y-y_bar)
    covar = s/len(x)-1  # formula of variance: (x-x_bar)*(y-y_bar)/n-1
    return covar
n = []
m = []
print("Enter x: ")
try:
    while True:
        n.append(float(input()))
except:
    print("Enter y: ")
    for i in range(len(n)):
        m.append(float(input()))
    print("\nCovariance of given x and y is: "+str(covariance(n,m)))
```

    Enter x: 
    1
    2
    3
    4
    
    Enter y: 
    1
    2
    3
    4
    
    Covariance of given x and y is: 0.25
    

# MEAN ABSOLUTE ERROR

![](data:image/jpeg;base64,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)


```python
x = [1,2,3,4,5]
mean = sum(x)/len(x)
s = 0
for i in x:
    s += abs(i-mean)
mae = s/len(x)

print(mae)
```

    1.2
    


```python
def MEAN_ABSOLUTE_ERROR(x):
    s = 0 #sum = 0
    mean = sum(x)/len(x) # formula of mean
    for i in x:
        s+= abs(i-mean) #|(x-x_bar)|
    mae = s/len(x) # formula of MAE
    return mae

n=[] #emptylist
l=int(input("Enter length: "))
for i in range(l):
    n.append(float(input()))
print("\nMean Absolute Error is: "+str(MEAN_ABSOLUTE_ERROR(n)))
```

    Enter length: 5
    1
    2
    3
    4
    5
    
    Mean Absolute Error is: 1.2
    

# MEAN SQUARED ERROR

![](data:image/png;base64,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)


```python
def MEAN_SQUARED_ERROR(x):
    s = 0 #sum = 0
    mean = sum(x)/len(x) #formula of mean
    for i in x:
        s+= (i-mean)**2
    mse = s/len(x)
    return mse

n=[]
l=int(input("Enter length: "))
for i in range(l):
    n.append(float(input()))
print("\nMean Squared Error is: "+str(MEAN_SQUARED_ERROR(n)))    
```

    Enter length: 5
    1
    2
    3
    4
    5
    
    Mean Squared Error is: 2.0
    

# ROOT MEAN SQUARE ERROR

![](https://miro.medium.com/max/966/1*lqDsPkfXPGen32Uem1PTNg.png)


```python
def RMSE(x):
    s = 0 #sum = 0 
    mean = sum(x)/len(x)
    for i in x:
        s+=(i-mean)**(0.5)
    rmse = s/len(x)
    return rmse

n=[]
l=int(input("Enter length: "))
for i in range(l):
    n.append(float(input()))
print("\nRoot Mean Squared Error is: "+str(RMSE(n)))    
```

    Enter length: 2
    1
    2
    
    Root Mean Squared Error is: (0.3535533905932738+0.3535533905932738j)
    

# LAPLACE ESTIMATE

# P(A) = A + 0.5 / A + B + 1 


```python
#LAPLACE ESTIMATE:- P(A) = A + 0.5 / A + B + 1 

#The Laplace estimate for the probability distribution of the experiment used to generate a frequency distribution. 

'''The "Laplace estimate" approximates the probability of a sample with count c from an experiment with N outcomes and 
B bins as (c+1)/(N+B).''' 

'''This is equivalent to adding one to the count for each bin, and taking the maximum likelihood estimate 
of the resulting frequency distribution.'''

def event_prob(event_outcomes,sample_space):
    probability = (event_outcomes/sample_space)
    return round(probability,2)

#sample space
cards = 52

#Face Card
face_card = 12

#Probability of drawing a heart
hearts = 13
heart_prob = event_prob(hearts,cards)
print("Probability of heart is: "+str(heart_prob))

#Laplace Estimate
laplace_estimate = (heart_prob + 0.5 / hearts + face_card + 1)
print("Laplace Estimate is: "+str(laplace_estimate))

```

    Probability of heart is: 0.25
    Laplace Estimate is: 13.288461538461538
    

# K - MEANS CLUSTERING ALGORITHM


```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline

df = pd.DataFrame({
    'x': [1,2,3,4,5],
     'y':[1,2,3,4,5]
})

print(np.random.seed(200))
k = 3 #Total number of clusters

#centroids[i] = [x,y]
centroids = {
    i+1: [np.random.randint(0,80),np.random.randint(0,80)]
    for i in range(k)
}

fig = plt.figure(figsize=(5,5))
plt.scatter(df['x'],df['y'],color='k')
colmap = {1:'r',2:'g',3:'b'}
for i in centroids.keys():
    plt.scatter(*centroids[i],color=colmap[i])
plt.xlim(0,80)
plt.ylim(0,80)
plt.show()
```

    None
    


![png](output_65_1.png)



```python

```
