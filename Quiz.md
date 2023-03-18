# KBC-Quiz-Game-in-python

# Create KBC Quiz game

name = input("Enter your name: ")
age = int(input("Enter your age: "))
if(age > 15):
    print("You can play Quiz ")
else:
    print("You cannot play Quiz")

print("*****LET'S PLAY KBC QUIZ*****\n")

questions = [
    [
        "Q1.Which language was used to create facebook?","Python","French","JavaScript","PHP","NONE",4 # PHP
    ],
    [
        "Q2.Which language was used to create instagram?","Python","JavaScript","C","C++","NONE",1  #  Python
    ],
    [
        "Q3.Which language was used to create Discord?","JavaScript","C","C++","Java","NONE",3   #  C++
    ],
    [
        "Q4.Which language was used to create Google?","JavaScript","Go","C++","Java","NONE",2    #  Go
    ],
    [
        "Q5.Which language was used to create whatsapp?","ERLANG","C","C++","Java","NONE",1    #  ERLANG
    ],
    [
        "Q6.Which language was used to create YouTube?","Python","C","HTML","Java","NONE",3    #   HTML
    ],
    
]

levels = [1000,2000,3000,4000,5000,6000]
money = 0
for i in range(0,len(questions)):
    question = questions[i]
    print(f"\n\nQuestion for Rs.{levels[i]}")
    # print(questions)
    print(f"a.{question[1]}        b.{question[2]}")
    print(f"c.{question[3]}        d.{question[4]}")
    reply=int(input("Enter your answer(1 to 4) or 0 to quit:\n"))
    if(reply==0):
        money=levels[i-1]
        break
    if(reply==question[-1]):
        print(f"Correct answer,you have won Rs.{levels[i]}")
    if(i==2):
        money = 2000
    elif(i==4):
        money = 4000
    else:
        print("Wrong answer!")
        break

print(f"Your take home money is{money}")
