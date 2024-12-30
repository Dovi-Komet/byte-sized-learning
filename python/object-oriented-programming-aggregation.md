---
layout: default
title: "Object-Oriented Programming: Aggregation"
order: 51
---

Aggregation is a type of composition where the contained objects can exist independently of the container object.

### Example of Aggregation

A `Team` class might aggregate `Player` objects.

Example:

```python
class Player:
    def __init__(self, name):
        self.name = name

class Team:
    def __init__(self, name):
        self.name = name
        self.players = []

    def add_player(self, player):
        self.players.append(player)

    def list_players(self):
        return ", ".join(player.name for player in self.players)

player1 = Player("Alice")
player2 = Player("Bob")
team = Team("Sharks")
team.add_player(player1)
team.add_player(player2)
print(team.list_players())
```

### Expected Output

```plaintext
Alice, Bob
```

Aggregation is useful for modeling relationships where components maintain their independence.