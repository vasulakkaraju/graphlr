graphlr
=======

Index the antlr3 AST through a Neo4j graph.

ASTs generated by antlr(X) are cool and helpful, but
a bit unhandy and boring to traverse. The most
natural way to traverse a tree like that is a
directed graph.

So, welcome graphlr. It's basically an extended
Java6 antlr grammar, which in parallel to the AST
builds an inpersistent Neo4j graph and links its
nodes to the relevant AST entries.

That way, one can easily jump into the AST without
having to recursively traverse it. Just use Cypher to
find the relevant nodes and to procede from there.

GraphlrTest.java contains some examples. This is
a very pre-alpha bloody state. I still need to create
more nodes, relationship. And right now, I'm bad
in building a stack while parsing, so I exactly know
where a method has been implemented, where the fields
or variable declarations belong to etc. And I need to
have a mode how to index an existing AST, so I can use
this in my Sonar fork. And, of course, this
documentation sucks.

But anyway, it's a start. Feel free to comment and
to contribute.
