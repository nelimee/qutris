# Ideas for `qutris`

In this file we write down any idea that might be interesting.

## Tetriminos generation

### Random number generation and noise

The simplest idea consists in chosing the blocks (tetriminos) by generating random numbers in [0, 7] with the quantum computer and then picking the tetriminos with the associated identifiant.
Then, noise can be added by submitting (on the quantum chip or not) circuits that should end up in the |0> state but might, because of noise, output some |1> along the way.

### Limiting the number of possible tetriminos

This idea is a simplification of the original idea presented in the next section. Basically, instead of having the 7 tetriminos in superposition, we only superpose 2 or 3 random tetriminos. This allows to simplify the quantum circuit.

### Having all the tetriminos in superposition

The original idea. The 7 tetriminos are superposed in a quantum state, and then a quantum measurement will chose which tetriminos.

## In-game vision

Several quantum-related objects and properties can be scenarised in the game to make them more "abordable" to newcomers. Examples are listed in the following sections.

### Quantum chips / simulators can be seen as opponents the player will fight against

Viewing the quantum chips / simulators as opponents have several good implications.

First, the player has the sensation of playing against a quantum computer. For some users, their first experience with a real quantum chip might be to play against it, which is an appealing experience.

Secondly this vision paves the way for opponent cards. These cards will be accessible to anyone and will describe each "opponent" (quantum chip or simulator). Here is a possible description for a simulator:

> Quantum simulator
>
> Uses the power of classical computers to simulate the behaviour of a real quantum computer.
> No noise, no errors, only classical randomness.

One goal will be to make these descriptions
1. Short
2. Easy to read and understand
3. Informative enough

Based on the difficulties of the "opponents", different levels can be created. For example, level 1 can be a stage with classical computer and the hardest level can be a stage with real quantum machine with the highest noise level. By progressing through levels, users can then get a better objective in clearing the game and be more motivated to play with all different opponents with greater fun. 

### Adding noise into the game 

In order for players to grasp the idea of quantum noise, `qutris` might make possible for players to chose the type(s) of noise they want to include in their game. Types of noise include:
- Measurement noise
- Gate noise
- Decoherence noise
- Initialisation error

Ideally, when the player plays on a fake backend with simulated noise, he/she should be able to pick the different noise(s) wanted for the hardcore level.
For the real backend, different quantum circuits for the different sources of noise can be combined together to be sure that the non-chosen noises will only be negligible when compared to the picked ones.

### Adding error mitigation

Error-mitigation can be used to lower down the impact of noise on the tetriminos. 

It can be seen as a power-up, for example when one perform a tetris.

Possibility to have as powerups:
- Instead of changing the block shapes, add power-ups blocks when the noisy circuits output a |1>.
- Still change the block shape **but** mark the changed block as a power-up.
