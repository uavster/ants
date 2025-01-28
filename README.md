# Ants

<img src="media/ants-example.gif" width="600" />

## Disclaimer

This is an experimental notebook. Please, do not take it as an example of what production code should look like.

## What is this?

This is a simulation of an ant colony. Ants collaborate to take food to the anthill.

Ants don’t have an internal representation of the food or anthill locations. They just follow a simple set of local rules, consisting in dropping and following chemical signals (pheromones) that they smell in their immediate vicinity. The colony's behavior emerges from these rules. 

Utimately, the dropped pheromones form a roadmap in the environment that tells individual ants how to get to the food or home. It is a world representation on the world itself.

The food is modeled as a circular mass, accelerated by the force vector of all ants collectively pushing it (yellow lines), and decelerated by the static and dynamic friction with the ground. It takes more ants to move heavier food.

The rules in each ant that make the colony find food:
* Sense food around? Drop some pheromones and head there.
* Sense pheromones around? Drop pheromones, but less than what you sense, and move to the highest concentration.

What makes the colony take food home:
* Each ant starts dropping a new type of “home” pheromones after leaving the anthill, in an amount that progressively decreases.
* When the ant finds food, it pushes the food in the direction of maximum home pheromone.

## How to run

1. Install jupyter notebook with conda or pip:
```
conda install jupyter
```
or
```
pip install notebook
```
2. Run a notebook
```
jupyter notebook
```
3. Locate and open `ants.ipynb`
4. Run all cells
5. Play the animation generated at the last cell (you can adjust the playback speed with the control under it)
   
## Attribution

If you use this code or get inspired by it, I'd appreciate a mention in any form:

Nacho Mellado

https://bsky.app/profile/uavster.bsky.social

https://x.com/uavster
