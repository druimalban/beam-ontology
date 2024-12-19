# Demonstration ontology of the Erlang VM

The BEAM is Erlang's virtual machine. This is a lightweight, 
demonstration ontology with fairly simple semantics, i.e. no dependency 
on OWL DL. It models what the BEAM is doing at a high level, and some 
of OTP.

The aim is to use it to demonstrate versioning an ontology with respect
to what RDF(S) alone gives us.

This is pretty rough. If we were going to model the BEAM well, we'd have
to put a bit more thought into it. A lot is left out, e.g. compound types
like maps (except for bitstring), behaviours, supervision trees. Indeed, 
while the BEAM's processes, their activities and the data which they
ingest/produce can be modelled pretty closely by PROV, this is 
purposefully omitted for now.

