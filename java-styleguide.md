## Rules

- Don't ignore exceptions. Alternatives to ignoring exceptions:
 - Throw the exception up to the caller of your method
 - Throw a new exception that's appropriate to your level of abstraction
 - Handle the error gracefully and substitute an appropriate value in the catch {} block
 - Catch the Exception and throw a new RuntimeException
 - If you are confident that actually ignoring the exception is appropriate then you may ignore it, but you must also comment why with a good reason.
- Don't catch generic exceptions
- Don't use finalizers
- Fully qualify imports
- Use Javadoc standard comments
- Write short methods
- Define fields in standard places
- Limit variable scope
- Local variables should be declared at the point they are first used.
- Nearly every local variable declaration should contain an initializer. If you don't yet have enough information to initialize a variable sensibly, you should postpone the declaration until you do.
- Loop variables should be declared in the for statement itself unless there is a compelling reason to do otherwise.
- Order import statements.
- Use 4 spaces for indentation.
- Follow field naming conventions.
 - Non-public, non-static field names start with m.
 - Static field names start with s.
 - Other fields start with a lower case letter.
 - Public static final fields (constants) are ALL_CAPS_WITH_UNDERSCORES.
- Use standard brace style.
- Always use braces around the statements for a conditional.
- Limit line length to 100 characters.
- Use standard java annotations.
- Treat acronyms and abbrevations as words in naming variables, methods and classes.
- Use TODO: comments
- one declaration per line
- single spce between type and identifier
- initialize local variables where they are declared
- put declaration at the beginning of block (method block or conditional block)

## References

- [Android](http://source.android.com/source/code-style.html)
- [Sun](http://www.oracle.com/technetwork/java/javase/documentation/codeconvtoc-136057.html)

## Thoughts

- Declaring java method arguments as final

    Final on method parameters ensures that those parameters are not accidentally overwritten by the method. So, final on method parameters is a handy way to protect against insidious bugs that erroneously change the value of your parameter. Note that final parameter are not considered part of the method signature, and are ignored by the complier when resolving calls. Parameters can be declared final or not with no influence on how the method is overridden.
