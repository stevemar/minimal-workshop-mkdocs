# mkdocs examples

This page includes a few samples.

## Code

```python
print("hello world!")
```

## Code with line numbers

```python linenums="1"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

## Code with highlights

```python hl_lines="2 3"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```


## Code with tabs

=== "C"

    ```c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "C++"

    ```c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```

## Add a button

[Launch the lab](https://developer.ibm.com){: .md-button .md-button--primary }

## Sidebar call out

!!! note inline end
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

!!! tip
    You can use `note`, `abstract`, `info`, `tip`, `success`, `question`
    `warning`, `failure`, `danger`, `bug`, `quote` or `example`.
    See [Admonitions](https://squidfunk.github.io/mkdocs-material-insiders/reference/admonitions/)
    for more examples.

!!! note
    A note.

!!! abstract
    An abstract.

!!! info
    Some info.

!!! success
    A success.

!!! question
    A question.

!!! warning
    A warning.

!!! danger
    A danger.

!!! example
    A example.

!!! bug
    A bug.

## Call outs with code

!!! note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

    ```python
    def bubble_sort(items):
        for i in range(len(items)):
            for j in range(len(items) - 1 - i):
                if items[j] > items[j + 1]:
                    items[j], items[j + 1] = items[j + 1], items[j]
    ```

    Nunc eu odio eleifend, blandit leo a, volutpat sapien. Phasellus posuere in
    sem ut cursus. Nullam sit amet tincidunt ipsum, sit amet elementum turpis.
    Etiam ipsum quam, mattis in purus vitae, lacinia fermentum enim.

## Images

![image](../assets/bee.png)
