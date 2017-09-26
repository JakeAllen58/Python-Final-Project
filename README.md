### Synopsis

This is a maze game designed to bring enjoyment to the player. You start off as an adventurer who enters a labyrinth, the program will function from the user's input to turn the adventurer left or right. If you make a wrong turn, the game will end! There is no description notifying the user where they are, and it is very easy to get lost inside of the labyrinth.

## Code Example

def _gamePlay(self):		#causing endless loop on main call
		global workingRoom
		gameEnd = roomMap[workingRoom].getDead()								#game loop
		print(workingRoom)
		if workingRoom == 4 or workingRoom == 36 or workingRoom == 24:
			workingRoom = random.randint(1, 43)
			self._label['text'] = ("You've been teleported! Now..." + roomMap[workingRoom].getDesc())
			self._startButton["image"] = roomMap[workingRoom].getImage()
		else:
			self._label['text'] = roomMap[workingRoom].getDesc()
			self._startButton["image"] = roomMap[workingRoom].getImage()	
		if gameEnd is True:
			self._leftButton["state"] = DISABLED
			self._rightButton["state"] = DISABLED
			return True

This is the code that focuses on the game loop and the user's input, it will take account of the user input and control their navigation. 

## Motivation

My whole life I have been a gamer, and I have always loved playing games. They have taught me many life lessons and helped my problem solving skills and knowledge in many ways. I thought it would be challenging and satisfying to me to create a game based on the lessons I have learned from Python.

## Installation

	roomMap[1]  = spot(53, 59, "You enter into the labryinth and approach a wall, do you turn left or right?", 1, wall, False)	#room1

This is code that is located in the main function, there are roughly 50 lines of these making descriptions to file into a class.

## API Reference

I am referencing a tkinter library for the program.

## Tests

Testing the program was a continuation of running the gui.

## Contributors

My instructors who helped me with the code and a fellow student who helped me brainstorm the idea.
