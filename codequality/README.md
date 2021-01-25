# Improve code quality in Eclipse

Source code is very volatile and when a team is working on the same code it can get, let's say "messy". Espcecially when unused stuff is not removed and obsolete practices are applied. And to be honest, when the task is done I don't start cleaning up my code. Fortunately there is support to take care of that during the coding process. Because I am working mainly with Eclipse I will show a few features of this particulare IDE that keep the code clean. I will only show the Java formatter here, but it will give you a basic idea about the functionality and the practices can be applied to other languages as well.

## Formatter

Formatters do exactly, what the name says: They format your code. The formatter gets started manually by pressing [Crtl]+[Shift]+[F] when a source file is opened. Then the indents, spaces and syntax gets cleaned up. Formatters are configured in the Eclipse preferences basically under the following path "<Language (i.e. Java)> - Code Style - Formatter":

![Formatter configuration dialog](formatter1.png)

Starting from this point some organizational tasks can be done:

* Create and edit formatters
* Import- and export formatter definitions (as xml files)
* Open the configuration dialog

## But why is it useful to define a company wide code style?

### Easier to read code

When code has the same style it makes it easier for developers to read the code of others.

### Only the real changes are commited

Imagine changing one line of code, saving the file and because you are using a formatter the whole file gets formatted.

### Reduced Warnings

Before and after saving:

![Formatter configuration dialog](formatter2.png) ![Formatter configuration dialog](formatter3.png)

Warnings are removed automatically. This makes code easiser to read and reduces code size.

## Save actions

## SonarLint