# Exercises. Part 3

-   The following command will invoke a program called Git to download some Python files.
```
$ git clone https://github.com/darinpeetz/rankine
```     
    Execute this line and then go into the directory `rankine` and list its contents.
    These scripts are designed to input and output their data through streams.
    For instance, execute `python grab_stations.py `.

    -   What is the output?
    -   How can we capture this output as a file?
    -   The programs are designed to work in series:<br>
        `grab_stations.py` feeds data into `grab_forecast.py` <br>
        `grab_forecast.py` feeds data into `plot_forecast.py`.<br>
        Write a single line command to effect this entire process.

<!--
```
python grab-stations.py > stations.txt
python grab-forecast.py < stations.txt > forecast.txt
python plot-forecast.py < forecast.txt
```
-->

#### Make sure you have properly generated the output from grab_forecast.py and stored it in the `forecast.txt` file for the following exercises.

-   If we run sort on the file `forecast.txt`, what is the output?  If we run
    `sort -k2` on the same input, what do we get instead? Why does `-k2`
    have this effect.

-   What is the difference between
    `$ wc -l < forecast.txt`
    and
    `$ wc -l forecast.txt`

-   The command `uniq` removes adjacent duplicated lines from its input.
    Try running the following commands:

```
$ cat forecast.txt > duplicate.txt
$ cat forecast.txt >> duplicate.txt
$ uniq duplicate.txt | wc -l
```

- Why do you think `uniq` only removes adjacent duplicated lines<sup>*</sup>?<br>
&nbsp;<sub> ***Hint**: think about very large data sets.</sub><br><br>
- Which other command could you combine with it in a pipe to remove all duplicated lines?

-   Examine the file called `forecast.txt` using less.  What text passes through
    each of the pipes and the final redirect in the pipeline below?

```
$ cat forecast.txt | head -5 | tail -3 | sort -r > final.txt
```

-   The command:

```    
$ cut -d, -f 1 duplicate.txt
```
prints out the first column of `duplicate.txt` (the station names). What other command(s) could be added to this in a pipeline to find out the original list of station names, sorted by latitude (the first coordinate in the file)?
