This proposes to add some election related objects to OCD. It attempts to stay close to the VIP election specification. http://vip-specification.readthedocs.io/en/vip5/xml/index.html#elements

Implementation
==============

Election
--------

id
    ocd identifier

identifiers
    upstream identifer

name
    name of the Election, I.e. 2016 General Election

date
    date of the election 

type
    general, special, runoff, primary

administrator
    reference to the ``Organization`` that administers the election

created_at
    Time that this object was created at in the system, not to be confused with the start_date.

updated_at
    Time that this object was last updated in the system.

sources
    List of sources used in assembling this object.  Has the following properties:

    url
        URL of the resource.
    note
        **optional**
        Description of what this source was used for.

extras
    Common to all Open Civic Data types, the value is a key-value store suitable for storing arbitrary information not covered elsewhere.



CandidateContest
----------------

id
    ocd identifier

election_id
    reference to the ``Election`` this contest is part of

posts
    References to the ``Post`` that this contest is for

created_at
    Time that this object was created at in the system, not to be confused with the start_date.

updated_at
    Time that this object was last updated in the system.

sources
    List of sources used in assembling this object.  Has the following properties:

    url
        URL of the resource.
    note
        **optional**
        Description of what this source was used for.

extras
    Common to all Open Civic Data types, the value is a key-value store suitable for storing arbitrary information not covered elsewhere.
   

Candidacy
---------

id
    ocd identifier

candidate_contest_id
    reference to a ``CandidateContest``

person_id
    reference to a ``Person``
