# C++ memo

## Choose the right STL container

### Flowchart

![CppContainersFlowchart](flowchart.svg)

### Sequence Containers :
- Search is slow

|  Container   | Continious data | Persitent position   | Iterator type | Insertion     | Notes |
|--------------|-----------------|----------------------|---------------|---------------|-------|
| `array`      | yes             | yes                  | Random access | Not possible  | Size must be tamplate compatible |
| `vector`     | yes             | No (lost on reserve) | Random access | End (slow)    | Need copy construcor on reserve |
| `deque`      | no              | No (lost on resize)  | Random access | Start and end | Need copy construcor on resize |
| `list`       | no              | yes                  | Bidirectional | Everywere     | No random access |

### Associative Containers :
- Ordered
- Fast search
- Persitent reference and iterator
- Not continus in memory

| Container             | Allow dublicate | Separate key/value | Iterator type |
|-----------------------|-----------------|--------------------|---------------|
| `map`                 | no              | yes                | Bidirectional |
| `set`                 | no              | no                 | Bidirectional |
| `multimap`            | yes             | yes                | Bidirectional |
| `multiset`            | yes             | no                 | Bidirectional |

### Unordered Associative Containers :
- Really fast search
- Persitent reference and iterator until rehashing
- Not continus in memory


| Container             | Allow dublicate | Separate key/value | Iterator type |
|-----------------------|-----------------|--------------------|---------------|
| `unordered_map`       | no              | yes                | Forward       |
| `unordered_set`       | no              | no                 | Forward       |
| `unordered_multimap`  | yes             | yes                | Forward       |
| `unordered_multiset`  | yes             | no                 | Forward       |

### TODO
- add cpp version for each container
- add constructor guide (copy, move, deleted, default)
- add template guide
- add cout format guide
- add data type + range guide

### Inspired by 
- https://www.hackerearth.com/practice/notes/c-stls-when-to-use-which-stl/
- https://stackoverflow.com/questions/471432/in-which-scenario-do-i-use-a-particular-stl-container
