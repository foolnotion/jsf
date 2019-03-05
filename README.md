# jsf - Jenkins Small Fast Random Generator
Implementation of Bob Jenkins' small fast prng https://burtleburtle.net/bob/rand/smallprng.html

The name JSF (Jenkins Small Fast) was coined by Doty-Humphrey when he included it in PractRand.

A more detailed analysis at http://www.pcg-random.org/posts/bob-jenkins-small-prng-passes-practrand.html

# example usage
```cpp
#include <random>
#include <iostream>

Random::JsfRand<64> jsf;

std::uniform_real_distribution<double> dist(1.0, 10.0);

for (int i = 0; i < 10; ++i) 
{
    std::cout << dist(jsf) << "\n";
}
```
