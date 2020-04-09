# fizzbuzz
Ah, the classic challenge!

Why do it?  I feel I am have enough experience to say I'm a good developer.  I have even done a few interviews in my career, though I've never asked this one.

It is fun little challenge and it is small enough to make changes to see if you can get some performance out of it.

My end solution is around 102 nanoseconds.

Other solutions:

```
for i := 1; i <= 100; i++ {
    w := fmt.Sprintf("%d", i)
	if i%3 == 0 {
        w = "Fizz"
        if i%5 == 0 {
    	    w = "FizzBuzz"
        }
	} else if i%5 == 0 {
		w = "Buzz"
	}
    fmt.Println(w)
```

Even though there is less branching, the multiple assignments I believe make this one a bit slower: ~120 nanoseconds

```
for i := 1; i <= 100; i++ {
    if i%15 == 0 {
        fmt.Println("FizzBuzz")
    } else if i%3 == 0 {
        fmt.Println("Fizz")
    } else if i%5 == 0 {
        fmt.Println("Buzz")
    } else {
        fmt.Println(i)
    }
}

```
About the same as the my original solution in time execution.  Though not following the rules of stating it is either multiple of 3 or 5.

Anyway a fun little exercise.

Happy coding!