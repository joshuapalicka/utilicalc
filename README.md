<h1 align="center">Utilicalc</h1>

<h4 align="center">A basic implementation of Jeremy Bentham's Felicific Calculus formula in Python</h4>

The purpose of this repository is to provide a set of methods for calculating the moral value of an action.
The moral value of an action is the sum of the moral value of the consequences of the action.
We calculate this by using Jeremy Bentham's formula, called "Felicific Calculus", "Hedonic Calculus", or
"Utilitarian Calculus", which is defined as such:

Variables:

    For pleasure:
    I = the intensity of pleasure
    D = the duration of pleasure
    C = certainty of pleasure
    N = propinquity or nearness in time of the pleasure
    F = fecundity or probability of 2nd order pleasure (the pleasure stemming from the pleasure)
    P = purity or probability of 2nd order pain (the pain stemming from the pleasure)
    E = how many people are affected by the pleasure

    For pain:
    I = the intensity of pain
    D = the duration of pain
    C = certainty of pain
    N = propinquity or nearness in time of the pain
    F = fecundity or probability of 2nd order pain (the pain stemming from the pain)
    P = purity or probability of 2nd order pleasure (the pleasure stemming from the pain)
    E = how many people are affected by the pain

Formula:

    For each actor affected by the action, the moral value of the action is calculated as follows:
        C * (I * D * N * E) must be calculated for each pleasure and pain that happens as a result of 
        the action, and for each 2nd order pleasure and pain. For 2nd order pleasure and pain, the same
        formula is used, but C is replaced with F or P, respectively. Pain is calculated as a negative 
        value, and pleasure is calculated as a positive value. The sum of all of these values is the 
        moral value of the action for this/these actor(s).

    The summation of all actor's calculated moral values for the action are summed together to get the
    total moral value of an action. One can use this formula to calculate the moral value for all decisions 
    they can make in a situation, and choose the decision with the most-positive moral value, or, in the case 
    of negative utilitarianism, the least-negative moral value.

Getting Started:
<br>
First, create an ActionSelector. This object holds multiple possible actions for which to choose from. Then, for each possible
act, create an Act object, and use the createActor function to create an actor for each actor that may be affected by the decision.
Once this is complete, call ActionSelector.getActWithHighestValue() to return the best (highest utility) action.
