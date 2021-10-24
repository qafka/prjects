import time

print('Welcome to the Void')
playerName = input('What is your name? ')

def chap1():
  global playerName
  
  print('')
  time.sleep(1)
  print(playerName+', this is a game where you get to choose your way in an adventure.')
  time.sleep(1)
  print('In each chapter, you will be given options to decide your fate!!')
  time.sleep(1)
  play = input('Are you ready? (y/n)')
  time.sleep(1)
  if play.upper()=='Y':
    print('')
    print('Loading..................')
    time.sleep(4)
    print('Please wait')
    time.sleep(2)
    print('By the way')
    time.sleep(0.5)
    print('Your breath is really stinky')
    time.sleep(1)
    print("Let's go!")
    time.sleep(1)
    chap2()
  elif play.upper()=='N':
    print('So is that it? You waited all this time and you just quit!!!?')
    endGame()
  else:
    print("-_-")
    time.sleep(3)
    print('Resetting game, please wait...')
    time.sleep(4)
    chap1()
    
def chap2():
  global playerName
  
  print('')
  print('You are minding your own business in TSS, when a sparkle catches your eye.')
  time.sleep(1)
  print('You think to yourself; is this the treasure chest full of pearls I have been looking forever for?')
  play = input('Do you investigate? (y/n): ')
  if play.upper()=='Y':
    print('')
    print('Good choice, brave dragon!')
    time.sleep(1)
    print('You start meandering across the TSS territory...')
    time.sleep(1)
    print('...when...')
    time.sleep(1)
    print (u"\u001b[31mError 404")
    time.sleep(3)
    print("You have crashed the game")
    time.sleep(1)
    print(u"\u001b[0m JK AHAHAHAHHA Only joking lol")
    time.sleep(2)
    chap3()
  elif play.upper()=='N':
    print('YOU REALLY DONT WANT GO LOOKING FOR THE PERALS?!!')
    time.sleep(1)
    print('Sending you back to the start now >:(')
    chap2()
  else:
    print('Maybe if I start telling you that the brain is an app then you will start using it')
    time.sleep(1)
    print('Resetting game please wait...')
    time.sleep(5)
    chap1()
    
def chap3():
  global playerName
  
  print('')
  print('As I was saying')
  time.sleep(1)
  print('When...')
  time.sleep(2)
  print('A giant Kraken jumps out of nowhere')
  time.sleep(1)
  print('And says')
  time.sleep(2)
  print('Nice to meet you! Whats your name?')
  time.sleep(1)
  play = input('Do you tell him your name? (y/n): ')
  if play.upper()=='Y':
    print('')
    print('My name is '+ playerName)
    time.sleep(1)
    print('Nice to meet you '+ playerName +' I am the Kraken King')
    time.sleep(1)
    print('What where you going to do with the pearls when you get them?')
    time.sleep(1)
    chap4()
  elif play.upper()=='N':
    print('Oh I thought you would be more polite then that')
    time.sleep(1)
    print('"SO WHAT WERE YOU GOING TO DO WITH THE PEARLS?" asked the King')
    time.sleep(1)
    chap4()
  else:
    print('REEEEEEEEEEEEEEEEEEEEEEEE')
    time.sleep(1)
    print('Resetting game please wait...')
    time.sleep(10)
    chap1()
    
def chap4():
  global playerName
  
  print('')
  print('Lets go staight into a question shall we? ')
  time.sleep(1)
  play = input('Do you steal the pearls?(Y/N) ')
  if play.upper()=='S':
    print('')
    print("I wouldn't of done that if I were you")
    time.sleep(1)
    print('You did a bad thing')
    time.sleep(1)
    endGame()
  elif play.upper()=='N':
    print('')
    print('"Oh thats ok then" said the king')
    time.sleep(1)
    print("I'll show you around my kingdom")
    time.sleep(1)
    chap5()
  else:
    print('hahaha')
    time.sleep(1)
    print('Resetting game please wait...')
    time.sleep(10)
    chap1() 

def chap5():
  global playerName
  
  print('')
  print('The King is showing you around his land')
  time.sleep(1)
  print('And he bring you to his palace')
  time.sleep(1)
  print('You see somthing that looks a bit peculiar')
  time.sleep(1)
  print('He says"Do not worry about that, thats just umm...')
  time.sleep(1)
  print('a special rock')
  time.sleep(1)
  print('You finish the tour and you still wonder what was that special \x1B[3mRock\x1B[23m')
  play = input('What do you do, (L) you look at the \x1B[3mRock\x1B[23m, (S) you steal the \x1B[3mRock\x1B[23m or (O) you meet the other krakens')
  if play.upper()=='L':
    print('')
    print('When you get a closer view you see that it is more like a power source')
    time.sleep(1)
    print("Your eyes are transfixed, you can't stop looking at it")
    time.sleep(1)
    print('Then a spiral of rainbow dust circles you')
    time.sleep(1)
    print('slowly your arms start becoming very slimy and long')
    time.sleep(1)
    print('**The transformation is complete**')
    time.sleep(1)
    print('The king speaks "welcome to the cupboard, dragon..."')
    time.sleep(2)
    print('...or should I say kraken!!!')
    time.sleep(2)
    print('Did you not know that a group of krakens is called a cupboard? Everyone knows that!!')
    time.sleep(3)
    endGameP()
  elif play.upper()=='S':
    print('You start running at the rock, which turns out really to be a chest')
    time.sleep(1)
    print('Then you grab it, but you run into the other krakens')
    time.sleep(2)
    print('They start crowding around you and say')
    time.sleep(2)
    print('Where are you going with that chest- we need that!!!')
    time.sleep(1)
    print('They take it and...')
    tickle()
  elif play.upper()=='O':
    print('')
    print('The King is showing you to the family')
    time.sleep(3)
    print("They eye you warily")
    time.sleep(1)
    print('The King introduces you')
    time.sleep(1)
    riddle()
    
def riddle():
    
  play = ''
  while play.lower() != "krakens don't lay eggs":
    print("And here's another member of our cupboard...")
    time.sleep(2)
    print('A kraken was sitting in a cave at a 45 degree angle. A rock was below him at 36 degrees facing left and another rock at a 21 degrees facing right. ')
    play = input('If the kraken layed a egg pointing down to the middle of the branches at a 67 degree angle, which way will the egg fall, left or right? ')
    time.sleep(1)
    print('Think outside the box')
  time.sleep(2)
  print('At last... we are able to move on...')
  time.sleep(1)
  print('You walk out the village and the King is still bleating on')
  time.sleep(1)
  print('When suddenly you walk into a portal and you are back home with your mother wittering on...')
  time.sleep(1)
  print('Was it all a dream?')
  time.sleep(4)
  print('bye')
  print('')
  endGame()
  
    
def endGameP():
  global playerName
  print('')
  print('Oh dear you are now a stupid kraken living in a cupboard')
  time.sleep(1)
  print("At least you didn't choose the steal option, that would have been way worse")
  play = input('Would you like to play again ' + playerName +' y/n')
  if play.upper() == 'Y':
    time.sleep(0.5)
    chap1()
  else:
    print('Goodbye- hope you try again later')
    time.sleep(1)
    
def tickle():
  print('')
  print("...tickles you until you can't breathe")
  time.sleep(15)
  print("Are you still here, I thought you would have gone by now!!")
  endGame()
  
def endGame():
  global playerName
  print('')
  print('The reason you are in this chapter is because you have probably done somthing stupid or won')
  time.sleep(1)
  play = input('Do you want to play again? ' + playerName + ' y/n ')
  if play.upper()=='Y':
    time.sleep(1)
    print('Good choice')
    time.sleep(1)
    chap1()
  if play.upper()=='N':
    time.sleep(1)
    print('You are such a baby- you dont even want to try again!!!')
    time.sleep(1)
    print('I am disapointed in you')
    print(' :b')



chap1()
