# Cli

- hot reloading 
- cli tool instead of template repo
- name?

## Commands

```
<tool> help
    build [root=./src] - builds ./dist from ./src
    dev - rebuild files on change and makes all files accessible (incl. components)
    init [dir] - inits dir containing (docker stuff, nginx stuff, src dir)
```


# Syntax

## instantiation

```html
<include src="./abc">
{
    "arg1": "value1",
    "arg2": "value2"
}
</include>

<!-- Syntax IMPROVEMENT -->

<!-- comps are found via backtracking from ./ to the src root directory until ./<comp>.comp.html is found or error otherwise -->
<comp />

<!-- access attrs via `{{ attr1 }}` -->
<comp attr1='val1'/>

<!-- access inner via `{{ inner }}` -->
<comp>
    <p>Inner</p>
    <p>Inner</p>
</comp>
```

# Conventions 

## Naming 

```
.html -> plain file
.page.html -> can use components
.comp.html -> defines a component using other components
```

