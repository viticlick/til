# Print uniq lines with AWK
If you want to print uniq lines of a file, and the file is very big, maybe this approach is better than ```sort + uniq``` approach
```bash
awk '!seen[$0]++'
```

First with ```seen[$0]``` we look at the value of ```seen[$0]``` (array a with whole input line (```$0```) as key).
If it does not exist ( ```!``` is negation in test will eval to true) ```!seen[$0]```. We print the input line ```$0``` (default action).

Also, we add one ( ```++``` ) to ```seen[$0]```, so next time ```!seen[$0]``` will evaluate to false.
