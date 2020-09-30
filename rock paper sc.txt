'''
1. you give a move first
2. computer give a move next
3. you decide when to quite
4. count no. of wins,draw and losses'''
import random
draw=0
win=0
losses=0
is_ended=False
prompt="choose rock(r), paper(p),scissor(s), or 'q' to quite:"
while True:
    user_choice=input(prompt)
    while user_choice not in['r','p','s','q']:
        user_choice=input(prompt)
    if user_choice=='q':
        break
    else:
        computer_choice=random.choice(['r','p','s'])
        if computer_choice=='r':
            move='rock'
        elif computer_choice=='p':
            move='paper'
        else:
            move='scissors'
        print('computer give a'+move)
        if computer_choice==user_choice:
            print("draw")
            draw+=1
        elif(computer_choice=='r' and user_choice=='p')or\
            (computer_choice=='p' and user_choice=='s')or\
            (computer_choice=='s' and user_choice=='r'):
            print("you win")
            win+=1
        else:
              print('you lose')
              losses+=1
print('you have' +str(wins)+'win',+str(draw)+'draw'and'\' +',str(losses),+ 'losses')

OUTPUT:-
choose rock(r), paper(p),scissor(s), or 'q' to quite:choose rock(r), paper(p),scissor(s), or 'q' to quite:python -u "c:\visual code\rock paper scissor.py"
choose rock(r), paper(p),scissor(s), or 'q' to quite:p
computer give ascissors
you lose
choose rock(r), paper(p),scissor(s), or 'q' to quite:r
computer give ascissors
you win
choose rock(r), paper(p),scissor(s), or 'q' to quite:s
computer give apaper
you win
choose rock(r), paper(p),scissor(s), or 'q' to quite:
            

                      
