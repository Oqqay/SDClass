import random
import os

PlayerOneScore = 0
PlayerTwoScore = 0
ComputerScore = 0
AgainstCPU = bool(False)
AgainstPlayer = bool(False)

def choiceToNumber(choice):
   return {"rock": 0, "paper": 1, "scissors": 2}[choice]

def TryAgain():
  global PlayerOneScore
  global PlayerTwoScore
  global ComputerScore
  global AgainstCPU
  global AgainstPlayer

  print("Try Again?")
  Choice = input("type 'yes' or 'no': ")
  if Choice == 'yes' and AgainstCPU:
    VsComputer()
  
  if Choice == 'yes' and AgainstPlayer:
    os.system('clear')
    VsLocal()


  elif Choice == 'no':
    AgainstCPU = False
    AgainstPlayer = False
    PlayerOneScore = 0
    PlayerTwoScore = 0
    ComputerScore = 0
    TitleScreen()

  else:
    print("oops, incorrect response")
    TryAgain()
#------------------------------------------------------#
def VsLocal():
  global PlayerOneScore
  global PlayerTwoScore
  global AgainstPlayer
  AgainstPlayer = True
  print("Now, Player 1, what will you choose? (make sure to look away Player 2): ")
  print("type 'rock'; type 'paper'; or type 'scissors'")
  PlayerOneChoice = input("")

  if PlayerOneChoice == "rock" or PlayerOneChoice == "paper" or PlayerOneChoice == "scissors":
    PlayerOneNumber = choiceToNumber(PlayerOneChoice)
    os.system('clear')
    print('Now, Player 2, what will you choose?')
    print("type 'rock'; type 'paper'; or type 'scissors'")

    PlayerTwoChoice = input("")
    if PlayerTwoChoice == "rock" or PlayerTwoChoice == "paper" or PlayerTwoChoice == "scissors":
      PlayerTwoNumber = choiceToNumber(PlayerTwoChoice)
      if (PlayerOneNumber - PlayerTwoNumber) % 3 == 1:
        PlayerOneScore = PlayerOneScore + 1
        print("Player 2 chose: " + PlayerTwoChoice + ". Player 1 chose: " + PlayerOneChoice)
        print("PLAYER 1 WINS!")
        print ("Player 2 score = " + str(PlayerTwoScore))
        print ("Player 1 score = " + str(PlayerOneScore))
        TryAgain()

      elif PlayerOneNumber == PlayerTwoNumber:
        print("Player 2 chose: " + PlayerTwoChoice + ". Player 1 chose: " + PlayerOneChoice)
        print("IT'S A TIE")
        print ("Player 2 score = " + str(PlayerTwoScore))
        print ("Player 1 score = " + str(PlayerOneScore))
        TryAgain()

      else:
        PlayerTwoScore = PlayerTwoScore + 1
        print("Player 2 chose: " + PlayerTwoChoice + ". Player 1 chose: " + PlayerOneChoice)
        print("PLAYER 2 WINS!")
        print ("Player 2 score = " + str(PlayerTwoScore))
        print ("Player 1 score = " + str(PlayerOneScore))
        TryAgain()
    else:
      os.system('clear')
      print('oops, incorrect response. Start over')
      VsLocal()     
  else:
    os.system('clear')
    print('oops, incorrect response. Start over')
    VsLocal()  

#---------------------------------------------------#
def VsComputer():
  global PlayerOneScore
  global ComputerScore
  global AgainstCPU
  AgainstCPU = True
  os.system('clear')
  print("Now, what will you choose: ")
  print("type 'rock'; type 'paper'; or type 'scissors'")
  ComputerChoice = random.choice(["rock", "paper", "scissors"])
  ComputerNumber = choiceToNumber(ComputerChoice)
 
  HumanChoice = input("")
  if HumanChoice == "rock" or HumanChoice == "paper" or HumanChoice == "scissors":
    HumanNumber = choiceToNumber(HumanChoice)
    if (HumanNumber - ComputerNumber) % 3 == 1:
      PlayerOneScore = PlayerOneScore + 1
      print("Computer chose: " + ComputerChoice + ". You chose: " + HumanChoice)
      print("YOU WIN!")
      print ("Computer score = " + str(ComputerScore))
      print ("Your score = " + str(PlayerOneScore))
      TryAgain()

    elif HumanNumber == ComputerNumber:
      print("Computer chose: " + ComputerChoice + ". You chose: " + HumanChoice)
      print("IT'S A TIE")
      print ("Computer score = " + str(ComputerScore))
      print ("Your score = " + str(PlayerOneScore))
      TryAgain()

    else:
      ComputerScore = ComputerScore + 1
      print("Computer chose: " + ComputerChoice + ". You chose: " + HumanChoice)
      print("COMPUTER WINS!")
      print ("Computer score = " + str(ComputerScore))
      print ("Your score = " + str(PlayerOneScore))
      TryAgain()

  else:
    print("oops, incorrect response")
    VsComputer()
  

def TitleScreen():
  os.system('clear')
  print("Welcome to my little Rock, Paper, Scissors (or is it Paper, Rock Scissors? Who knows) game.")
  print("Here are the choices: ")
  print("type 'computer' to go against a cpu;")
  TitleScreenChoice = input("type 'local' to play against a friend on the same computer: ")

  if TitleScreenChoice == 'computer':
    VsComputer()
  elif TitleScreenChoice == 'local':
    os.system('clear')
    VsLocal()
  else:
    TitleScreen()


#---------------------------------------------------------#


TitleScreen()

