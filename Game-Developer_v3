#Imports
from termcolor import colored
import time
from random import randint
import math

#Game Variables
mode = ""
balance = 0
companyValue = 0
totalProfit = 0
username = ""
companyName = ""
fans = 0
gamesSold = 0
gameFinished = False
#Date
day = 4
month = 3
year = 2020
#Console Popularities
pcPop = randint(78,95)
consolePop = randint(65,95)
mobilePop = randint(40,75)
#Lists used to contain game stats
games = []
gamesYears = []
copiesSold = []
revenues = []
gameConsoles = []
gamePrices = []

def niceNumber(number): #Function to print numbers neat
   return '{:,}'.format(number)


#Algorithm to find amount of buyers
def buyerAlgorithm(prodBud, markBud, time, console, price):
    purchases = 0
    #Calculates the budget in
    budget = prodBud*markBud
    purchases = (math.pow(math.log(budget),7))/(30000) + ((markBud+prodBud)*1.5)
    #Calculates time in
    purchases = purchases * (time/12)
    #Calculates console in
    if console.lower() == "pc":
        purchases = purchases * pcPop/100
    elif console.lower() == "console":
        purchases = purchases * consolePop/100
    elif console.lower() == "mobile":
        purchases = purchases * mobilePop/100
    #Calculates the price in
    if price > 1000:
        purchases = purchases/(price*50)
    elif price > 500:
        purchases = purchases/(price*20)
    elif price > 100:
        purchases = purchases/(price*8)
    elif price > 50:
        purchases = purchases/(price*3)
    elif price > 20:
        purchases = purchases/(price*1.8)
    elif price > 10:
        purchases = purchases/(price*1.5)
    elif price > 5:
        purchases = purchases/(price*1.2)
    elif price > 0:
        purchases = purchases/(price*1)
    elif price == 0:
        purchases = purchases/(price/2)
    #Adds fans to the mix
    purchases += fans*(randint(30,90)/100)
    #Returns final result
    return purchases


def welcomePlayer(): #Function to Welcome Player
    #Welcomes Player
    for i in range(0,99):
        print("\n")
    print(colored("Welcome to Game Dev II, I hope you enjoy!\n","blue"))
    time.sleep(2)

def selectMode(): #Function to select gamemode
    global mode
    modePicked = False
    #Asks player for Game Mode
    while modePicked == False:
        print(colored("What game mode do you want to play in?","blue"))
        print(colored("       -Easy: Start with 100k","blue"))
        print(colored("       -Normal: Start with 20k","blue"))
        print(colored("       -Hard: Start with 5k","blue"))
        choice = input("")
        print("\n\n")
        validChoices = ["easy","normal","hard"]
        if choice.lower() in validChoices:
            modePicked = True
            mode = choice.lower()
            print(colored("   >>>Loading Game...\n","green"))
            time.sleep(1)
        else:
            print(colored("Please select a valid choice.","red"))
        
def intro(): #Function to give the player an intro
    #Gives player an Intro
    global balance
    if mode == "easy":
        print(colored("\n\nRecently, your rich uncle passed away from Ligma, and you inhereted a large chunck of Cash.\nAfter contemplating what to do with it, you figured you'd start a game company.\nAfter all the paperwork and taxes you are left with 100k to develop your first game.","yellow"))
        balance = 100000
    elif mode == "normal":
        print(colored("\n\nYou just finished college, and as a young chap full of ambition, you decided to start your own game company.\nAfter taking out some loans, and getting some help from your parents,\nyou are left with an unamed company, and 20k left to develop your first game.","yellow"))
        balance = 20000
    elif mode == "hard":
        print(colored("\n\nYou have had enough of life.\nYou're tired of people and have decided to follow your passion of creating games.\nAfter scraping together all the money you could find,\nyou filed all the paperwork and started your own company, and found yourself with 5k left to devolop your first game.","yellow"))
        balance = 5000
    time.sleep(1)

def playerChoices(): #Function to get player to choose his name, and his company name
    #Gets Player to choose his name
    global username
    print(colored("\nPlease choose a name for you: ","green"))
    username = input("   ")
    #Gets Player to choose his a company name
    global companyName
    print(colored("\nPlease choose a name for your Company: ","green"))
    companyName = input("   ")

    print(colored(f"\n >>>On the 4th of March, 2020, {username} founded the Company {companyName}!","blue"))
    time.sleep(1)

def elapseTime(months):
    global month
    global year
    global pcPop
    global consolePop
    global mobilePop
    for i in range(0,int(months)-1):
        month += 1
        pcPop = max(min(randint(pcPop-1,pcPop+1),100),0)
        consolePop = max(min(randint(consolePop-1,consolePop+1),100),0)
        mobilePop = max(min(randint(mobilePop-1,mobilePop+1),100),0)
    while month > 12:
        year += 1
        month -= 12

def createGame():
    global fans
    print(colored(f"\n\n\nUntitled Game by {companyName}.","green"))
    global balance
    sufficientCash = False
    #Asks User for Game Name
    namePicked = False
    while namePicked == False:
        name = input("    > Name of Game: ")
        if name in "                                                                                   ":
            print(colored("> Please input a proper name.","red"))
        else:
            games.append(name)
            namePicked = True
    #Gets game budget
    while sufficientCash == False:
        prodBudget = input("    > Production Budget: $")
        markBudget = input("    > Marketing Budget: $")
        try:
            prodBudget = int(prodBudget)
            markBudget = int(markBudget)
            if int(prodBudget) + int(markBudget) > balance:
                print(colored("> You went over budget, please don't spend money you don't have.","red"))
            else:
                sufficientCash = True
                balance -= int(prodBudget) + int(markBudget)
        except:
            print(colored("> Please input a number for both your budgets.","red"))
    #Development Time
    timeSpentChosen = False
    while timeSpentChosen == False:
        timeSpent = input("    > Months spent developing: ")
        try:
            if int(timeSpent) > 0:
                elapseTime(timeSpent)
                timeSpentChosen = True
                gamesYears.append(year)
            else:
                print(colored("> Please input a positive number.","red"))
        except:
            print(colored("> Please input a number.","red"))
    #Prints out the different Console Popularities and lets user pick on Console
    consolePicked = False
    print(colored(f"      |PC Popularity: {pcPop}%","green"))
    print(colored(f"      |Console Popularity: {consolePop}%","green"))
    print(colored(f"      |Mobile Popularity: {mobilePop}%","green"))
    while consolePicked == False:
        consoles = ["pc","mobile","console"]
        console = input("    > Console: ")
        if console.lower() in consoles:
            consolePicked = True
            gameConsoles.append(console)
        else:
            print(colored("> Please select a Console.","red"))
    #Pick Game Price
    pricePicked = False
    while pricePicked == False:
        price = input("    > Price: $")
        try:
            price = int(price)
            pricePicked = True
            gamePrices.append(price)
        except:
            print(colored("> Please input a number.","red"))
            

    #Does the calculations for amount of games sold
    purchases = round(buyerAlgorithm(int(prodBudget),int(markBudget),int(timeSpent),console,int(price)))
    totalCost = int(prodBudget) + int(markBudget)
    revenue = int(purchases)*int(price)
    profit = revenue - totalCost
    print(colored(f"\nAfter {timeSpent} months of working on {name}, it was finally released on {day}/{month}/{year}.","green"))
    print(colored(f"The total cost of the game came to ${niceNumber(round(totalCost))}.","green"))
    print(colored(f"{niceNumber(round(purchases))} people bought {name}.","green"))
    print(colored(f"{companyName} made ${niceNumber(revenue)} in revenue, and ${niceNumber(profit)} in profit.","green"))
    print(colored(f"","green"))
    #Pays you the revenue
    balance += purchases*price
    copiesSold.append(niceNumber(round(purchases)))
    revenues.append(niceNumber(round(profit)))
    fans += round(purchases/10)
    global gamesSold
    gamesSold += round(purchases)
    global totalProfit
    totalProfit += profit/2
    wait = input("")

def createSequel():
    global fans
    if len(games) != 0:
        print(colored(f"\n\n\nUntitled Sequel by {companyName}.","green"))
        global balance
        #Asks user what game this will be a sequel to
        gameSelected = False
        print(colored("\nWhat game will this be a sequel to: ","blue"))
        gameID = 0
        for game in games:
            print(colored(f"     {gamesYears[gameID]} | {game} ({gameConsoles[gameID]}) (${gamePrices[gameID]}) | {copiesSold[gameID]} copies Sold | ${revenues[gameID]} Profit","green"))
            gameID += 1
        print("")
        while gameSelected == False:
            gameChoice = input("      >>>")
            for game in games:
                if gameChoice.lower() == game.lower():
                    gameSelected = True
            if gameSelected == False:
                print(colored("> Please select a game.","red"))
        #Asks User for Game Name
        namePicked = False
        while namePicked == False:
            name = input("\n    > Name of Sequel: ")
            if name in "                                                                                   ":
                print(colored("> Please input a proper name.","red"))
            else:
                games.append(name)
                namePicked = True
        #Gets game budget
        sufficientCash = False
        while sufficientCash == False:
            prodBudget = input("    > Production Budget: $")
            markBudget = input("    > Marketing Budget: $")
            try:
                prodBudget = int(prodBudget)
                markBudget = int(markBudget)
                if int(prodBudget) + int(markBudget) > balance:
                    print(colored("> You went over budget, please don't spend money you don't have.","red"))
                else:
                    sufficientCash = True
                    balance -= int(prodBudget) + int(markBudget)
            except:
                print(colored("> Please input a number for both your budgets.","red"))
        #Development Time
        timeSpentChosen = False
        while timeSpentChosen == False:
            timeSpent = input("    > Months spent developing: ")
            try:
                if int(timeSpent) > 0:
                    elapseTime(timeSpent)
                    timeSpentChosen = True
                    gamesYears.append(year)
                else:
                    print(colored("> Please input a positive number.","red"))
            except:
                print(colored("> Please input a number.","red"))
        #Prints out the different Console Popularities and lets user pick on Console
        consolePicked = False
        print(colored(f"      |PC Popularity: {pcPop}%","green"))
        print(colored(f"      |Console Popularity: {consolePop}%","green"))
        print(colored(f"      |Mobile Popularity: {mobilePop}%","green"))
        while consolePicked == False:
            consoles = ["pc","mobile","console"]
            console = input("    > Console: ")
            if console.lower() in consoles:
                consolePicked = True
                gameConsoles.append(console)
            else:
                print(colored("> Please select a Console.","red"))
        #Pick Game Price
        pricePicked = False
        while pricePicked == False:
            price = input("    > Price: $")
            try:
                price = int(price)
                pricePicked = True
                gamePrices.append(price)
            except:
                print(colored("> Please input a number.","red"))
                
        #Does the calculations for amount of games sold
        purchases = buyerAlgorithm(int(prodBudget),int(markBudget),int(timeSpent),console,int(price))  + (fans/10)
        totalCost = int(prodBudget) + int(markBudget)
        revenue = int(purchases)*int(price)
        profit = revenue - totalCost
        print(colored(f"\nAfter {timeSpent} months of working on the Sequel to {gameChoice}, {name}, it was finally released on {day}/{month}/{year}.","green"))
        print(colored(f"The total cost of the game came to ${niceNumber(round(totalCost))}.","green"))
        print(colored(f"{niceNumber(round(purchases))} people bought {name}.","green"))
        print(colored(f"{companyName} made ${niceNumber(revenue)} in revenue, and ${niceNumber(profit)} in profit.","green"))
        print(colored(f"","green"))
        #Pays you the revenue
        balance += purchases*price
        copiesSold.append(niceNumber(round(purchases)))
        revenues.append(niceNumber(round(profit)))
        fans -= round(fans/20)
        fans += round(purchases/10)
        global gamesSold
        gamesSold += round(purchases)
        global totalProfit
        totalProfit += profit/2
        wait = input("")
    else:
        print(colored(f"\nYou have no games to make a sequel of.","red"))
        wait = input("")

def rereleaseGame():
    global fans
    if len(games) != 0:
        print(colored(f"\n\n\nUntitled Rerelease by {companyName}.","green"))
        global balance
        #Asks user what game this will be a sequel to
        gameSelected = False
        print(colored("\nWhat game will you be rereleasing: ","blue"))
        gameID = 0
        for game in games:
            print(colored(f"     {gamesYears[gameID]} | {game} ({gameConsoles[gameID]}) (${gamePrices[gameID]}) | {copiesSold[gameID]} copies Sold | ${revenues[gameID]} Profit","green"))
            gameID += 1
        print("")
        while gameSelected == False:
            gameChoice = input("      >>>")
            for game in games:
                if gameChoice.lower() == game.lower():
                    gameSelected = True
            if gameSelected == False:
                print(colored("> Please select a game.","red"))
        #Asks User for Game Name
        namePicked = False
        while namePicked == False:
            name = input("\n    > Title of Rerelease: ")
            if name in "                                                                                   ":
                print(colored("> Please input a proper name.","red"))
            else:
                games.append(name)
                namePicked = True
        #Gets game budget
        sufficientCash = False
        while sufficientCash == False:
            prodBudget = input("    > Production Budget: $")
            markBudget = input("    > Marketing Budget: $")
            try:
                prodBudget = int(prodBudget)
                markBudget = int(markBudget)
                if int(prodBudget) + int(markBudget) > balance:
                    print(colored("> You went over budget, please don't spend money you don't have.","red"))
                else:
                    sufficientCash = True
                    balance -= int(prodBudget) + int(markBudget)
            except:
                print(colored("> Please input a number for both your budgets.","red"))
        #Development Time
        timeSpentChosen = False
        while timeSpentChosen == False:
            timeSpent = input("    > Months spent developing: ")
            try:
                if int(timeSpent) > 0:
                    elapseTime(timeSpent)
                    timeSpentChosen = True
                    gamesYears.append(year)
                else:
                    print(colored("> Please input a positive number.","red"))
            except:
                print(colored("> Please input a number.","red"))
        #Prints out the different Console Popularities and lets user pick on Console
        consolePicked = False
        print(colored(f"      |PC Popularity: {pcPop}%","green"))
        print(colored(f"      |Console Popularity: {consolePop}%","green"))
        print(colored(f"      |Mobile Popularity: {mobilePop}%","green"))
        while consolePicked == False:
            consoles = ["pc","mobile","console"]
            console = input("    > Console: ")
            if console.lower() in consoles:
                consolePicked = True
                gameConsoles.append(console)
            else:
                print(colored("> Please select a Console.","red"))
        #Pick Game Price
        pricePicked = False
        while pricePicked == False:
            price = input("    > Price: $")
            try:
                price = int(price)
                pricePicked = True
                gamePrices.append(price)
            except:
                print(colored("> Please input a number.","red"))
                
        #Does the calculations for amount of games sold
        purchases = buyerAlgorithm(int(prodBudget),int(markBudget),int(timeSpent),console,int(price)) + (fans/10)
        totalCost = int(prodBudget) + int(markBudget)
        revenue = int(purchases)*int(price)
        profit = revenue - totalCost
        print(colored(f"\nAfter {timeSpent} months of working on the rerelease of {gameChoice}, {name}, it was finally rereleased on {day}/{month}/{year}.","green"))
        print(colored(f"The total cost of the game came to ${niceNumber(round(totalCost))}.","green"))
        print(colored(f"{niceNumber(round(purchases))} people bought {name}.","green"))
        print(colored(f"{companyName} made ${niceNumber(revenue)} in revenue, and ${niceNumber(profit)} in profit.","green"))
        print(colored(f"","green"))
        #Pays you the revenue
        balance += purchases*price
        copiesSold.append(niceNumber(round(purchases)))
        revenues.append(niceNumber(round(profit)))
        fans -= round(fans/20)
        fans += round(purchases/10)
        global gamesSold
        gamesSold += round(purchases)
        global totalProfit
        totalProfit += profit/2
        wait = input("")
    else:
        print(colored(f"\nYou have no games to rerelease.","red"))
        wait = input("")


def turnChoices(): #Function called every turn to get turn choices
    global fans
    global balance
    balance = round(balance)
    #Updates Company Value
    companyValue = balance + totalProfit
    date = f"Date: {day}/{month}/{year}"
    print(colored(f"\n------{companyName}------","blue"))
    balanceString = f"Balance: ${niceNumber(balance)}"
    print(colored(date,"blue")) #Prints the date
    print(colored(balanceString,"blue")) #Prints balance
    print(colored(f"Fans: {niceNumber(fans)}","blue")) #Prints amount of fans
    print(colored(f"Copies Sold: {niceNumber(gamesSold)}","blue")) #Prints amount of fans
    print(colored(" 1) Create a Game.","blue"))
    print(colored(" 2) Create a Sequel.","blue"))
    print(colored(" 3) Rerelease a Game.","blue"))
    print(colored(" 4) View your Games.","blue"))
    print(colored(" 5) Console Popularity.","blue"))
    print(colored(" 6) Wait.","blue"))
    print(colored(" 7) Company Value.","blue"))
    print(colored(" 8) Sell Company.","blue"))
    print("")
    
    choiceChosen = False
    while choiceChosen == False:
        choice = input("    >>>")
        if choice in "12345678" and choice != "":
            if choice == "1": #Create a game
                createGame()
            elif choice == "2": #Create a Sequel
                createSequel()
            elif choice == "3": #Rerelease a Game
                rereleaseGame()
            elif choice == "4": #View Games
                print(colored(f"\n >>>{companyName}'s Games:\n","green"))
                if (len(games) == 0):
                    print(colored(f"\n           -No Games Yet-","green"))
                else:
                    gameID = 0
                    for game in games:
                        print(colored(f"     {gamesYears[gameID]} | {game} ({gameConsoles[gameID]}) (${gamePrices[gameID]}) | {copiesSold[gameID]} copies Sold | ${revenues[gameID]} Profit","green"))
                        gameID += 1
                wait = input("")
            elif choice == "5": #Console Popularity
                print(colored(f"\n      |PC Popularity: {pcPop}%","green"))
                print(colored(f"      |Console Popularity: {consolePop}%","green"))
                print(colored(f"      |Mobile Popularity: {mobilePop}%\n","green"))
                wait = input("")
            elif choice == "6": #Wait
                timeSpentChosen = False
                print("")
                while timeSpentChosen == False:
                    timeToWait = input(" > How many months do you wish to wait: ")
                    try:
                        if int(timeToWait) >= 0:
                            elapseTime(timeToWait)
                            timeSpentChosen = True
                            wait = input(colored(f"> You waited for {timeToWait} months. The date now is {day}/{month}/{year}.\n","green"))
                        else:
                            print(colored("> Please input a positive number.","red"))
                    except:
                        print(colored("> Please input a number.","red"))
            elif choice == "7": #View Company Value
                print(colored(f"\n\n      >>> {companyName} is currently worth ${niceNumber(round(companyValue))}.","green"))
                wait = input("")
            elif choice == "8": #Sell Company
                offer = companyValue * (randint(50,100)/100)
                print(colored("\n\n-Negotiating Table-","green"))
                print(colored(f"     | Company Value: ${niceNumber(round(companyValue))}","green"))
                print(colored(f"     | Counter Offer: ${niceNumber(round(offer))}","green"))
                offerChosen = False
                while offerChosen == False:
                    offerChoice = input (" >>Accept Offer(y/n): ")
                    if offerChoice.lower() == "y" or offerChoice.lower() == "n":
                        offerChosen = True
                        if offerChoice.lower() == "y":
                            print(colored(f"\n   ---{companyName} has been sold at ${niceNumber(round(offer))}!---","green"))
                            wait = input("")
                            global gameFinished
                            gameFinished = True
                        elif offerChoice.lower() == "n":
                            print(colored(f"\n   You rejected their offer and walked away.","red"))
                            wait = input("")
                    else:
                        print(colored(f"> Please enter a valid option.","red"))
            choiceChosen = True
        else:
            print(colored("Please enter a valid choice.","red"))

welcomePlayer()
selectMode()
intro()
playerChoices()

while gameFinished == False:
    turnChoices()

