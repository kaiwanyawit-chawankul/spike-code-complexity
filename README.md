


## Steps

### install packge on core library

``` 
dotnet add package Microsoft.CodeAnalysis.Metrics --version 3.3.3
```

### Add .editorconfig

```
[*.cs]
dotnet_diagnostic.CA1501.severity = error
dotnet_diagnostic.CA1502.severity = error
dotnet_diagnostic.CA1505.severity = error
dotnet_diagnostic.CA1506.severity = error
```

Rules
```
CA1501: Avoid excessive inheritance	A type is more than four levels deep in its inheritance hierarchy. Deeply nested type hierarchies can be difficult to follow, understand, and maintain.
CA1502: Avoid excessive complexity	This rule measures the number of linearly independent paths through the method, which is determined by the number and complexity of conditional branches.
CA1505: Avoid unmaintainable code	A type or method has a low maintainability index value. A low maintainability index indicates that a type or method is probably difficult to maintain and would be a good candidate for redesign.
CA1506: Avoid excessive class coupling	This rule measures class coupling by counting the number of unique type references that a type or method contains.
CA1507: Use nameof in place of string	A string literal is used as an argument where a nameof expression could be used.
CA1508: Avoid dead conditional code	A method has conditional code that always evaluates to true or false at run time. This leads to dead code in the false branch of the condition.
CA1509: Invalid entry in code metrics configuration file	Code metrics rules, such as CA1501, CA1502, CA1505 and CA1506, supplied a configuration file named CodeMetricsConfig.txt that has an invalid entry.
```


### Run build

```
dotnet build
```

## References

https://docs.microsoft.com/en-us/visualstudio/code-quality/how-to-generate-code-metrics-data?view=vs-2019
https://docs.microsoft.com/en-us/visualstudio/code-quality/how-to-generate-code-metrics-data?view=vs-2019#net-code-quality-analyzers-code-metrics-rules
https://docs.microsoft.com/en-us/visualstudio/code-quality/use-roslyn-analyzers?view=vs-2019#set-rule-severity-in-an-editorconfig-file
https://docs.microsoft.com/en-us/visualstudio/code-quality/how-to-generate-code-metrics-data?view=vs-2019#microsoftcodeanalysismetrics-nuget-package
https://docs.microsoft.com/en-us/dotnet/fundamentals/code-analysis/quality-rules/ca1508
https://docs.microsoft.com/en-us/dotnet/fundamentals/code-analysis/quality-rules/ca1509
https://www.strathweb.com/2019/04/roslyn-analyzers-in-code-fixes-in-omnisharp-and-vs-code/

msbuild /t:Metrics