BoxLang is a scripting language that runs on the JVM.

It is the spiritual successor to CFML.

# BoxLang Instructions

BoxLang files come in three different formats:
- `.bx` - A BoxLang class definition.
- `.bxs` - A script file that can be used as an entrypoint or included in other BoxLang files.
- `.bxm` - A template file that can be used to generate html.

BoxLang can also run CFML files
- `.cfc` - A component definition.
- `.cfs` - A script file that can be used as an entrypoint or included in other BoxLang files.
- `.cfm` - A template file that can be used to generate html.

<boxlang-code-example type="bxs">
x = 1

if x == 1 {
    printLn("x is one")
} else {
    printLn("x is not one")
}

// lambdas use the `->` operator
myLambda = (a, b) -> a + b
// closures use the `=>` operator
myClosure = ( a, b ) => a + b

// you can use the `new` operator to create new instances of classes
myObject = new lib.MyClass()
// you can use the `import` operator to import other BoxLang files
// imports use fully qualified names - they SHOULD NOT be quoted
import lib.MyOtherClass

// now MyOtherClass is available in the current scope
myOtherObject = new MyOtherClass()

// you can also use the `import` operator to import java classes
import java.util.ArrayList

myList = new ArrayList()
</boxlang-code-example>

<boxlang-code-example type="bx">
// classes in BoxLang are not named
// you will need to add accessors=true if you want to create generated getters and setters
// IMPORTANT: BoxLang classes are always defined with `class` only ColdFusion components (CFCs) are defined with `component`
class accessors=true {
    // properties are defined first
    // short property form
    property string FirstName;
    // long property form
    property name="LastName" type="string";

    // you can provide an optional constructor named `init`
    public function init(){

    }

    // functions can be defined without type information
    function doStuff(){
        printLn("Doing stuff")
    }

    // function can be defid with type information
    public string function greet( required string name) {
        return "Greetings, " & name & "!"
    }

}
</boxlang-code-example>

<boxlang-code-example type="bxm">
<!--- comments in template files are written like html comments but with 3 dashes --->
<bx:output>
    <!--- use a script tag to write boxlang scripts --->
    <bx:script>
        names = ["Alice", "Bob", "Charlie"]
    </bx:script>

    <!--- you can use bx:loop to iterate over arrays --->
    <bx:loop array="#names#" index="name">
        <p>Hello, #name#!</p>
    </bx:loop>

    <!--- you can use bx:if to conditionally render content --->
    <bx:if names.len() gt 3>
        <p>There are too many names!</p>
    <bx:else>
        <p>There are not enough names.</p>
    </bx:if>

    <!--- if you use hash marks (#) inside of a bx:output for anything other than variables, you need to escape them using double hash (##)--->
    <style>
        .greeting {
            color: ##f79c42;
        }
    </style>
</bx:output>
</boxlang-code-example>