# Game Eng. Tutorial

Game Name: **Parkour Warrior**<br>
Core game loop: A short parkour course that's sure to have some *interesting* surprises.

Controls:<br>
`WASD` - Move<br>

`Space` - Jump<br>
`Y` - Spawn Yellow Cube<br>
`G` - Spawn Green Cube<br>

## Implemented Patterns

#### Factory Design Pattern
Creates a green cube if `G` is pressed and a yellow one is `Y` is pressed. Uses SpawnActor to spawn the instances.

<img width="1428" height="607" alt="image" src="https://github.com/user-attachments/assets/19142cec-0401-410c-a5d3-eb9c34bdd923" />

**Diagram**<br>
<img width="608" height="498" alt="image" src="https://github.com/user-attachments/assets/371e9e83-6c4c-4a01-a352-cf1c7b416cc6" />

**Q: What element of your game adopts the chosen pattern?**<br>
A: The pattern is implemented in my game as part of the core control scheme, allowing the player to use this Factory to arbitrarily spawn cubes (green/yellow) to platform with.

**Q: Why is this pattern a good choice for the associated functionality?**<br>
A: The main reason the Factory is a good choice for a Cube Spawner is because the type of cube doesn't need to be known inside the function that's creating it, and the object is essentially disowned after SpawnActor regardless, which makes it a perfect candidate for Factory.

#### Singleton Design Pattern
A simple LogManager that logs an event when the game first starts, as a sanity check.

<img width="726" height="345" alt="image" src="https://github.com/user-attachments/assets/e32d47b7-711f-4802-be0d-cb1df0b66310" />

#### Observer Design Pattern
Just a Win Observer that prints text when the player enters the region considered "winning".

<img width="1005" height="409" alt="image" src="https://github.com/user-attachments/assets/c9a4d84d-82a5-4ec1-be97-bd3053e528cc" />
