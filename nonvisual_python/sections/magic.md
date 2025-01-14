[<<< Previous](motivation.md) | [Next >>>](resources.md)

# Saving Our Code with IPython Magic

We're at the end of our workshop, and you may want to keep a record of the commands you entered into IPython during your session. Since we're using IPython, we can do that using a magic command.

Magic commands are useful utilities built into IPython and Jupyter Notebooks. If you use Python from other programs, you won't have access to magic commands—they're specific to IPython and Jupyter.

## Saving Your Session

To save our session to a text file, we can run:

```python
%save nonvisual.py 1-40
```

That's a percent sign, the word `save`, a space, a filename, a space, the number 1, a hyphen, and the number 40. The last number should be the number of your last output line.

If you would like to resume your session in the future, you can use the `%load` magic:

```python
%load nonvisual.py
```
## Other Useful Magic Commands and IPython Tricks

IPython has a [variety of magic commands](https://ipython.readthedocs.io/en/stable/interactive/magics.html). A few other useful commands:

- `%run` If you have an external Python file, you can run it and load all of its functions and variables into the current REPL with this command. This is, by far, my most used magic command.
- `%notebook`: This is a great command if you're working with sighted collaborators. It takes your REPL session and creates a Jupyter Notebook out of it. You can share the notebook with sighted collaborators. If you need to edit the notebook, currently Google Colab is more accessible with NVDA than Jupyter Notebook.
- `%edit`: Opens a text editor. You can then write Python, save and close the file, and the code will be run in the REPL. By default, this command opens Notepad on Windows, but you can set another editor to be the default.
- `%who`: Print out all the variables you've defined and that are available in your session.
- `%whos`: Like who, but you get more information on each variable
- `%xmode`: This mode determines how much information will be printed out during a traceback error. `%xmode minimal` can be good for screen reader users who don't want verbose output.

### The Underscore Trick

IPython stores the output of the last successfully run command as the variable `_` (the underscore symbol).

If you ran a command and would like to assign its output to a variable, you can use the underscore as follows:

```Python
2 + 5
```

Then run:

```Python
x = _
```

That's the letter x, a space, the equal sign, a space, and an underscore.

Now the output of `2 + 5` should be assigned to `x`:

```Python
x
```

You should receive the number 7 as output.

In fact, you can do this for the output of any cell in your session. To assign `y` to the output of the ninth cell in your code, run the following:

```Python
y = _9
```

That's the letter y, a space, an equal sign, a space, an underscore, and the number 9.

Just replace the number 9 with the number of the cell whose output you want to reference.

[<<< Previous](motivation.md) | [Next >>>](resources.md)
