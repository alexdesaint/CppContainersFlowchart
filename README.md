# C++ memo

## Choose the right c++ container

### Containers with no keys (search is slow) :
|  Container   | Continious data | Persitent position   | Iterator type | Insertion     | Notes |
|--------------|-----------------|----------------------|---------------|---------------|-------|
| `array`      | yes             | yes                  | Random access | Not possible  | Size must be tamplate |
| `vector`     | yes             | No (lost on reserve) | Random access | End (slow)    | Need copy construcor on reserve |
| `deque`      | no              | No (lost on resize)  | Random access | Start and end | Need copy construcor on resize |
| `list`       | no              | yes                  | Bidirectional | Everywere     | No random access |

### Container with keys (no continus data, persitent position and iterator) :
| Container            | Ordered | Allow dublicate | Separate key/value | Iterator type | Notes |
|----------------------|---------|-----------------|--------------------|---------------|--|
| `map`                | yes     | no              | yes                | Bidirectional |  |
| `set`                | yes     | no              | no                 | Bidirectional |  |
| `multimap`           | yes     | yes             | yes                | Bidirectional |  |
| `multiset`           | yes     | yes             | no                 | Bidirectional |  |
| `unordered_map`      | no      | no              | yes                | Forward       | Really fast search |
| `unordered_set`      | no      | no              | no                 | Forward       | Really fast search |
| `unordered_multimap` | no      | yes             | yes                | Forward       | Really fast search |
| `unordered_multiset` | no      | yes             | no                 | Forward       | Really fast search |

### Flowchart

![CppContainersFlowchart](flowchart.svg)

### TODO
- `std::vector` needs a copy constructor
- add cpp version for each container
- add constructor guide (copy, move, deleted, default)
- add template guide
- add cout format guide
- add data type + range guide
