# Google-Map
practice graph theory and data structures



### 准备工作

[CS 61B](https://sp18.datastructur.es/)

[项目文档](https://sp18.datastructur.es/materials/proj/proj3/proj3)

[项目视频](https://www.youtube.com/watch?v=KZIDT5zHAVE&list=PL8FaHk7qbOD6xsQBRCY5Su-vbkf0X4gq8)

[基础代码](https://github.com/orgs/Berkeley-CS61B/repositories)

[项目完成文档(北大作者版)](https://github.com/PKUFlyingPig/CS61B/tree/master/proj3)

[参考完成文档(Lance117版本)](https://github.com/Lance117/Bear-Maps)



### 前端实现

http://localhost:4567/





### 后端实现



| File                                                         | Deescription                                                 |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [Rasterer](https://github.com/LanceSanity/Berkeley-CS61B-Audit/blob/master/proj3/src/main/java/Rasterer.java) | Renders map images given a user's requested area and level of zoom |
| [GraphDB](https://github.com/LanceSanity/Berkeley-CS61B-Audit/blob/master/proj3/src/main/java/GraphDB.java) | Graph representation of the contents of [Berkeley OSM](https://github.com/Berkeley-CS61B/library-sp18/tree/proj3/data). Implemented an Autocomplete system using a Trie data structure, which allows matching a prefix to valid location names in $O(n)$ time, where $n$ is the number of words sharing the prefix. |
| [GraphBuildingHandler](https://github.com/LanceSanity/Berkeley-CS61B-Audit/blob/master/proj3/src/main/java/GraphBuildingHandler.java) | Handler used by SAX parser to parse Nodes and Ways from Berkeley OSM file |
| [Router](https://github.com/LanceSanity/Berkeley-CS61B-Audit/blob/master/proj3/src/main/java/Router.java) | Uses $A*$ search algorithm to find the shortest path between two points in Berkeley; uses shortest path to generate navigation directions. |



```
If you do want to use it through the command line here are some basic instructions: 
Windows users: Follow the instructions here, making sure to adjust them to your machine which should already have JDK8 installed. 
Use command prompt, not git bash. 
Mac users: brew install maven Ubuntu users: sudo apt-get install maven.

You can then use the mvn compile and mvn exec:java -Dexec.mainClass="MapServer" targets to run MapServer, 
after patching your pom.xml to include src/static as a sources root. 
Do so by renaming pom_alternate.xml to pom.xml. You can also run the tests with mvn test. 
```
