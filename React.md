# React

### Tertiary Operator

```
render () {
  return (
    <div className="row">
      { //Check if message failed
        (this.state.message === 'failed')
          ? <div> Something went wrong </div> 
          : <div> Everything in the world is fine </div> 
      }
    </div>
  );
}
```

**Tertiary Operator Template**

`(expression or statement) ? (return this) : (return other)`

How this is read: If the {expression or statement} is true, {return this}. Otherwise, {return other}.

### If Statement

```
<If condition={condition}>
  statement
</If>
```
Condition can be an expression or a statement
- Expression `condition={error}` (meaning, "if error is true or present")
- Statement `condition={currentYear != year}` (meaning, "if it is not the current year"

### If Else Statement

```
<If condition={error}>
  statement
  <Else />
  else statement
</If>
```


## Common errors
- Forgetting to import modules
