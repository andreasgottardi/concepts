# Improve code quality in Eclipse

Source code is volatile and when a team is working on the same code it can get let's say "messy". Especially when unused stuff is not removed and obsolete practices are applied. And to be honest, when the task of changing the logic is done I don't start cleaning up my code. Fortunately there is support to take care of that during the coding process. Because I am working mainly with Eclipse I will show a few features of this particular IDE that keep the code clean. I will only show the Java formatter here, but it will give you a basic idea about the functionality and the practices can be applied to other languages as well.

## Why is it useful to define a company wide code style?

### Easier to read code

When code has the same style it makes it easier for developers to read the code of others. A new developer does not have to worry to do something wrong because the whole code style and formatting is defined in the IDE during setup.

### Only the real changes are committed

Imagine changing one line of code, saving the file and because you are using a formatter and the other developer doesn't the whole file gets formatted. Thus all the formatting changes get committed.

![Commit changes](reasoning1.png)

### Reduced Warnings

Before ...

![Formatter configuration dialog](formatter1.png)

... and after saving:

![Formatter configuration dialog](formatter2.png)

Unused imports are removed automatically. This makes code easier to read, reduces code size and is in general good practice.

## Formatter

Formatters do exactly, what the name says: They format your code. The formatter gets started manually by pressing [Crtl]+[Shift]+[F] when a source file is opened. Then the indents, spaces and syntax gets cleaned up. Formatters are configured in the Eclipse preferences for several languages under the following path "<Language (i.e. Java)> - Code Style - Formatter":

![Formatter configuration dialog](formatter3.png)

Starting from this point some organizational tasks can be done:

* Create and edit formatters
* Import- and export formatter definitions (as xml files)
* Open the configuration dialog

I don't go too much into detail here, but the code formatter is the place to define code conventions, guidelines and style. This can be done very detailed. And multiple profiles can be defined, ex- and imported.

![Formatter main window](formatter4.png)

### Temporary switch off formatter

Let's assume you have a source code like the following:

```java
String xml = ""
	+ "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n"
	+ "<note>\n"
	+ "	<to>You</to>\n"
	+ "	<from>Me</from>\n"
	+ "	<heading>Reminder</heading>\n"
	+ "	<body>About the task.</body>\n"
	+ "</note>";
```

Now the formatter would format it to this:

```java
String xml = "" + "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n" + "<note>\n" + "	<to>You</to>\n"
	+ "	<from>Me</from>\n" + "	<heading>Reminder</heading>\n" + "	<body>About the task.</body>\n"
	+ "</note>";
```

But this is not readable anymore. To avoid this the formatter offers a special comment to temporary disable it:

```Java
//@formatter:off
String xml = ""
	+ "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n"
	+ "<note>\n"
	+ "	<to>You</to>\n"
	+ "	<from>Me</from>\n"
	+ "	<heading>Reminder</heading>\n"
	+ "	<body>About the task.</body>\n"
	+ "</note>";
//@formatter:on
```

Now, even when formatting is applied, the marked code parts are left as they are.
## Save actions

Formatters are great, but they have to be applied every time manually by selecting the appropriate menu item. Fortunately there are "Save actions". These actions can apply formatters automatically when saving a file.

![Save actions dialog](saveactions1.png)

## SonarLint

[Sonarlint](https://www.sonarlint.org) analyzes the source code during coding, shows categorized hints and provides improvements. The tool is available as [plugin for Eclipse](https://marketplace.eclipse.org/content/sonarlint).

SonarLint provides improvement dialogs when code is not best practice.

![Improvement hint dialog](sonarlint1.png)

When the description is opened text explaining the problem and offering improvements is shown.

![Improvement screen](sonarlint2.png)

## Conclusion

I am working for some time now with these improvements and they made my code better and taught me better programming. If ones goal is to get better in coding and write code that is more stable and secure these tools can provide good support.
