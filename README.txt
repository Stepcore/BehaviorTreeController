The controller is called BehaviorTreePacMan
Import all the java files into the same package and then run in executor with
exec.runGame(new BehaviorTreePacMan(), your ghosts(), visual, delay);


This controller is using a simple behavior tree that checks if there are enemies nearby. If not, it eats the pills. If there are enemies nearby it goes through a few checks.

First it checks how many there are, if there is one enemy it just directly away.
Then it checks if there are more than one, if it's in a junction, if not, it goes to the nearest junction.
Then it checks if it's in a junction, which direction is the safest to go. This is done by checking when directions lead to ghosts and then choosing the one where it doesn't find a ghost.

It does not prioritise power pills. Just eating pills and getting away from ghosts.