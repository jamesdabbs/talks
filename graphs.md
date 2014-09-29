# [fit] Atlanta
# [fit] Intermediate
# [fit] Ruby

---

# What's All This Then?

* Next Meetup - TBD, late October (tentatively on the 22nd)
* [Propose and vote for topics](http://air-topics.herokuapp.com) that you'd like to hear
* Pull requests welcome - [jamesdabbs/air-tracker](https://github.com/jamesdabbs/air-tracker)

---

# [fit] GRAPHS
# [fit] A Drunkard's Walk
# _**James Dabbs**_

![](http://d1.stern.de/bilder/stern_5/wissen/2013/KW16/Leonhard_Euler2_maxsize_2048_1536.jpg)

---

# A Graph

* is a collection of _nodes_ (or _vertices_)
* joined by _edges_ (or _links_)
* which may have _attributes_ and a _direction_

---

# Nodes and Edges

![inline, fill, fit](http://tjm.org/wp-content/uploads/2013/01/KONIGSBERG-MULTIGRAPHS.jpg)

~ Euler, 1735

---

# Paths

* A series of successive adjacent edges is a _path_ (or _walk_).
* Graphs can be studied by looking at the paths in them: Konigsberg's bridges have no _Eulerian_ path, but do have a _Hamiltonian_ path

---

^ 1d / 2d lattices
^ Ant on a chessboard
^ Monopoly
^ The Internet

# Random Walks

![](http://i.ytimg.com/vi/UkLq3es11Jc/hqdefault.jpg)

---

# Neo4j

* Graph database - stores nodes and links
* Allows queries in terms of attributes, relationships and paths
* Written in Java

---

# Neo4j

* Quick start: `brew install neo4j && neo4j start`
* [REST API](http://docs.neo4j.org/chunked/stable/rest-api.html) available via [neography](https://github.com/maxdemarzi/neography) and [active_node](https://github.com/klobuczek/active_node)
* Embedded access on JRuby via [neo4j.rb](https://github.com/neo4jrb/neo4j)

---

^ Non-goals, but interesting
^ * Understand performance / efficiency of graph queries
^ * Implement anything on JRuby

# Goals

* Explore Neo4j capabilities and syntax
* Compare with a traditional SQL implementation
* Examine tools for integrating with a Rails app

---

^ These are all in the linked air-graphs project
^ * Movie database exploration
^ * Social network SQL-vs-Neo4j comparison
^ * Ruby Gems dependency exploration

# Examples

![](http://www.my80splaylist.com/wp-content/uploads/2014/03/kevin-bacon-in-footloose.jpg)

---

# [fit] FIN
# [fit] **_Questions?_**

---

# Resources

* AIR Homepage - [air-tracker.herokuapp.com](http://air-tracker.herokuapp.com)
* Slides - [jamesdabbs/air-talks](https://github.com/jamesdabbs/air-talks)
* Rails Project - [jamesdabbs/air-graphs](https://github.com/jamesdabbs/air-graphs)
* Twitter - [@jamesdabbs](https://twitter.com/jamesdabbs)
