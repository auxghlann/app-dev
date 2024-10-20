# APP DEV Reviewer

## 1. Modal and Non-Modal Forms

### `MODAL` Forms
- A modal form is a type of form that **restricts** any action to the main window 
- but keeps it visible.
- can be called using the `Form.ShowDialog()` method.

### `Non-MODAL` Forms
- A non-modal form is a type of form that **allows interaction** from the parent form where it came
from.
- can be called using the `Form.Show()` method.


## 2. Closing and Disposing of Form

### Disposing
- Disposing a form **releases all unmanaged resources** that the form is currently holding.


### `Form.Dispose()`
- Shuts down and *manually* disposes the current form.

### `Form.Close()`
- Shuts down and *automatically* disposes the
current form.


## When to use?

```
Form.Show() => Form.Close()

Form.ShowDialog() => Form.Dispose()
```


## 3. Passing Values from Form to another Form

### Two (2) possible methods:

#### 1. Passing it as arguments for parameters.

``` c#
// MainFrm.cs

some_control_function() {
    AnotherFrm frm = new AnotherFrm(value)
}

// AnotherFrm.cs

public AnotherFrm(dataType variable) {
    this.variable = variable;
}

// - or

dataType _variable;

public AnotherFrm(dataType variable) {
    _variable = variable;
}

```

#### 2. Changing control modifiers.



## Bonus
- You can setup a form owner by passing the parent form as the WindowOwner for the form that you want toopen.

Ex.
```
Form.Show(this);
```