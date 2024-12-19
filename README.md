# Demonstration ontology of the Erlang VM

The BEAM is Erlang's virtual machine. This is a lightweight, 
demonstration ontology with fairly simple semantics, i.e. no dependency 
on OWL DL. It models what the BEAM is doing at a high level, and some 
of OTP (many of the bits which make Erlang Erlang).

# Motivation

The aim is to use it to demonstrate versioning an ontology with respect
to what RDF(S) alone gives us.

This conception of the Erlang/OTP system is based partly on a different
project I worked on, data processing infrastructure for fish farms. 
PROV was used to model the computational system (which was an Elixir 
program using `gen_stage`) and how data flowed through it. The ontology
was about model validation, hence why information about Erlang went in 
it, rather than the fish proper.

# Erlang internals and the ontology

This is pretty rough. If we were going to model the BEAM well, we'd have
to put a bit more thought into it. 

In the ontology:

  - Most BEAM data-types but no compound data-types like maps. (`BitString` is mapped to `XSD:String`, however.)
  - BEAM nodes: instances of the BEAM, running on the host computer system.
  - OTP applications: a package which provides some sort of functionality. (An example of this included with the Erlang/OTP distribution is the `mnesia` DBMS.)
  - OTP processes: like operating system processes, but better.
  - Activities which occur in the Erlang/OTP system, like OTP application invocation, process invocation.
  - Outputs produced by activities

The ontology doesn't introduce supervision trees or behaviours (e.g. 
`gen_server`), at least not at the start, since these will be used to
demonstrate extending the ontology by changing the semantics. While the
BEAM's processes, their activities and the data which they ingest/produce
can be modelled pretty closely by PROV, this is purposefully omitted for
now.
