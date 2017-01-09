
# Rules availables in eslint and tslint

|SONAR|TSLINT|ESLINT|
|---|---|---|
|FunctionComplexity|cyclomatic-complexity|complexity|
|DebuggerStatement|no-debugger|no-debugger|
|EqEqEq|triple-equals|eqeqeq|
|Eval|no-eval|no-eval|
|OneStatementPerLine|one-variable-per-declaration|one-var|
|Semicolon|semicolon|semi|
|CurlyBraces|curly|curly|
|BitwiseOperators|no-bitwise|no-bitwise|
|PrimitiveWrappers|no-construct|no-new-wrappers|
|ForIn|forin|guard-for-in|
|FunctionDeclarationsWithinBlocks|no-inner-declarations|no-inner-declarations|
|TrailingComma|trailing-comma|comma-dangle|
|AssignmentWithinCondition|no-conditional-assignment|no-cond-assign|
|LabelPlacement|label-position|no-labels|
|SwitchWithoutDefault|switch-default|default-case|
|NonEmptyCaseWithoutBreak|no-switch-case-fall-through|no-fallthrough|
|EmptyBlock|no-empty|no-empty|
|TabCharacter|indent|indent|
|BoundOrAssignedEvalOrArguments|no-eval|no-eval|
|VariableDeclarationAfterUsage|no-use-before-declare|no-use-before-define|
|S1125|no-extra-boolean-cast|no-extra-boolean-cast|
|RedeclaredVariable|no-duplicate-variable|no-redeclare|
|TrailingWhitespace|no-trailing-whitespace|no-trailing-spaces|
|S1442|ban|no-alert|
|S104|max-file-line-count|max-lines|

# Rules availables in eslint but currently unavailables in tslint

|SONAR|ESLINT|
|---|---|
|WithStatement|no-with|
|MultilineStringLiterals|no-multi-str|
|ArrayAndObjectConstructors|no-new-object && no-array-constructor|
|ExcessiveParameterList|max-params|
|FunctionDefinitionInsideLoop|no-loop-func|
|S1135|no-warning-comments|
|TrailingComment|no-inline-comments|
|S1134|no-warning-comments|
|S878|no-sequences|
|NestedIfDepth|max-depth|


# Rules availables in eslint but not applicable to Typescript.

|SONAR|ESLINT|
|---|---|
|UnreachableCode|no-unreachable|
|DuplicateFunctionArgument|no-dupe-args|
|DuplicatePropertyName|no-dupe-keys|
|OctalNumber|no-octal|
|StrictMode|strict|
|UnusedVariable|no-unused-vars [Deprecated]|

# Rules not available neither in tslint nor eslint

|SONAR|Descripción|
|---|---|
|HtmlComments|HTML-style comments should not be used|
|CollapsibleIfStatements|Collapsible "if" statements should be merged|
|ConstructorFunctionsForSideEffects|Objects should not be created to be dropped immediately without being used|
|FutureReservedWords|"future reserved words" should not be used as identifiers|
|ConditionalComment|Internet Explorer's conditional comments should not be used|
|S1145|Useless "if(true) {...}" and "if(false){...}" blocks should be removed|
|S138|Functions should not have too many lines|
|RedeclaredFunction|This rule checks that functions declared in same scope don't have identical names.|
|SameNameForFunctionAndVariable|Declaring both a variable and a function with an identical name in same scope should be avoided.|
|NamedFunctionExpression|Named function expressions should not be used|
|TooManyBreakOrContinueInLoop|Loops should not contain more than a single "break" or "continue" statement|
|UnusedFunctionArgument|Unused function parameters should be removed|
|S100|Function names should comply with a naming convention|
|S1301|"switch" statements should have at least 3 "case" clauses|
|S1126|Return of boolean expressions should not be wrapped into an "if-then-else" statement|
|S1264|A "while" loop should be used instead of a "for" loop|
|S1472|Function call arguments should not start on new lines|
|S1219|"switch" statements should not contain non-case labels|
|S1067|Expressions should not be too complex|

## Links

Sources:
- [Sonar Rules](http://grepcode.com/file/repo1.maven.org/maven2/org.codehaus.sonar-plugins.javascript/javascript-checks/1.2/org/sonar/l10n/javascript/rules/javascript/WithStatement.html?av=f)
- [Sonar Rules Repository](https://github.com/SonarSource/sonar-javascript/tree/master/javascript-checks/src/main/resources/org/sonar/l10n/javascript/rules/javascript)
- [TSLint rules](https://palantir.github.io/tslint/rules/)
- [ESLint rules](http://eslint.org/docs/rules/)

tslint-eslint-rules:
- [ESLint rules for TSLints - GitHub](https://github.com/buzinas/tslint-eslint-rules)
- [ESLint rules for TSLint - npm](https://www.npmjs.com/package/tslint-eslint-rules)
