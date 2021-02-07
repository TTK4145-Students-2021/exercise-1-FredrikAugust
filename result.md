# Results

The results vary wildly between `{-1_000_000, 1_000_000}` due to the lack of synchronisation between the threads.

I would believe this is because the threads compete for control over the `i` variable, and who get's the say for a given iteration is essentially random due to no thread synchronisation.
