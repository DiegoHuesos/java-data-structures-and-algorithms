# Java Data Structures and Algorithms

Coursework from ITAM’s *Estructuras de Datos Avanzadas* course (August–December 2019). The repository includes Java implementations of data structures and algorithms, programming labs, and Python notebooks.

## Explore the repository

| Area | What it contains |
| --- | --- |
| [Linked lists](1.-CLASE_ESPONDA/EDA-WORKSPACE/src/DataEstructures/List/) | Node and list implementations with a console demo that exercises list reversal. |
| [Binary trees](1.-CLASE_ESPONDA/EDA-WORKSPACE/src/BinaryTree/) | A binary tree interface and a linked implementation with tree nodes. |
| [Sorting](1.-CLASE_ESPONDA/EDA-WORKSPACE/src/AlgoritmosDeOrdenamiento/) | Sorting exercises and experiments with merge sort. |
| [Recursion](1.-CLASE_ESPONDA/EDA-WORKSPACE/src/RecursiveExercises/) | Standalone exercises for practicing recursive methods. |
| [Friday Java project](1.-CLASE_ESPONDA/EDA_Viernes/) and [introductory lab](2.-LAB_GAMBOA/) | Console, command-line argument, and file I/O exercises. |
| [Graph notebook](Grafos.ipynb) | Notes and examples on adjacency matrices, shortest paths, and maximum flow. |
| [Python fundamentals](python-fundamentals.ipynb) | Notes and examples on Python objects and mutability. |

## Build and run the Java examples

Use a JDK with `javac` and `java` on your PATH. The three Java source groups were compiled separately with JDK 8. From the repository root, run this PowerShell example to compile the main workspace and run its linked-list demo.

```powershell
$source = '1.-CLASE_ESPONDA/EDA-WORKSPACE/src'
$output = 'build/workspace'
New-Item -ItemType Directory -Force $output | Out-Null
$files = (Get-ChildItem -LiteralPath $source -Recurse -Filter '*.java' -File).FullName
javac -encoding UTF-8 -d $output $files
if ($LASTEXITCODE -ne 0) { throw 'Java compilation failed' }
java -cp $output DataEstructures.List.TestList
```

For the Friday project, use `1.-CLASE_ESPONDA/EDA_Viernes/src` as the source folder. For the introductory lab, use `2.-LAB_GAMBOA`. Give each group its own output directory. The two NetBeans projects can also be opened directly in NetBeans.

## Course references

- [Course organization](https://github.com/Clase-EDA)
