# week-5-pyhton

ASSINGMENT 1
# Base class representing a football game
class FootballGame:
    def __init__(self, name, developer, release_year, genre="Sports"):
        self.name = name
        self.developer = developer
        self.release_year = release_year
        self.genre = genre
    
    def display_game_info(self):
        return f"{self.name} ({self.release_year}) - Developed by {self.developer}. Genre: {self.genre}"

    def start_game(self):
        return f"Starting {self.name}... Enjoy the match!"

# Subclass representing eFootball 2024 (specific football game)
class eFootball2024(FootballGame):
    def __init__(self, name, developer, release_year, teams, game_modes):
        # Initialize base class with common attributes
        super().__init__(name, developer, release_year)
        self.teams = teams  # List of teams available in the game
        self.game_modes = game_modes  # List of game modes (e.g., Career Mode, Multiplayer)
    
    # Method to display the teams available in the game
    def display_teams(self):
        return f"Available teams in {self.name}: {', '.join(self.teams)}"
    
    # Method to simulate selecting a game mode
    def select_game_mode(self, mode):
        if mode in self.game_modes:
            return f"Selected game mode: {mode}"
        else:
            return f"Error: {mode} is not available in this game."

# Create an instance of eFootball2024
game1 = eFootball2024(
    name="eFootball 2024", 
    developer="Konami", 
    release_year=2024, 
    teams=["FC Barcelona", "Real Madrid", "Manchester United", "Bayern Munich"], 
    game_modes=["Career Mode", "Multiplayer", "Ultimate Team"]
)

# Displaying game information
print(game1.display_game_info())

# Display available teams
print(game1.display_teams())

# Start the game
print(game1.start_game())

# Selecting a game mode
print(game1.select_game_mode("Career Mode"))
print(game1.select_game_mode("Story Mode"))  # Invalid mode to demonstrate error handling

ASSIGNMENT 2
# Base class representing an Animal
class Animal:
    def move(self):
        raise NotImplementedError("Subclass must implement abstract method")

# Subclass representing Dog
class Dog(Animal):
    def move(self):
        return "Running 🐕"

# Subclass representing Fish
class Fish(Animal):
    def move(self):
        return "Swimming 🐟"

# Base class representing a Vehicle
class Vehicle:
    def move(self):
        raise NotImplementedError("Subclass must implement abstract method")

# Subclass representing Car
class Car(Vehicle):
    def move(self):
        return "Driving 🚗"

# Subclass representing Plane
class Plane(Vehicle):
    def move(self):
        return "Flying ✈️"

# Function to demonstrate polymorphism
def demonstrate_movement(entity):
    print(entity.move())

# Create instances of animals and vehicles
dog = Dog()
fish = Fish()
car = Car()
plane = Plane()

















