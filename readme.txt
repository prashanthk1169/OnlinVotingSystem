This application cosist several layes like
  Service Layer
     1.created class VoteService
  Cotroller Layer
    1. created class VoteController
 Entity or Model Layer
    1.created class Candidate


guidlines to access RestApi's 

Entering a Candidate:
A user makes a GET request to /entercandidate with the candidate name.
The VoteController forwards the request to the VoteService, which adds the
candidate to the in-memory data store.
url:https:/localhost:8080/entercandidate?name=Ajay

Casting a Vote:
A user makes a GET request to /castvote with the candidate name.
The VoteController forwards the request to the VoteService, which increments
the vote count for the specified candidate.
url:https:/localhost:8080/castvote?name=Ajay

Counting Votes:
A user makes a GET request to /countvote with the candidat  name.
The VoteController forwards the request to the VoteService, which retrieves and
returns the vote count for the specified candidate.
url:https:/localhost:8080//countvote?name=Ajay

Listing Votes:
A user makes a GET request to /listvote.
The VoteController forwards the request to the VoteService, which retrieves all
candidate names and vote counts and returns them in JSON format.
url:https:/localhost:8080/listvote

Getting the Winner:
A user makes a GET request to /getwinner.
The VoteController forwards the request to the VoteService, which determines
and returns the candidate with the highest vote count.
url:https:/localhost:8080/getwinner

Future Considerations:
Persistence Layer:
For a more robust and scalable solution, consider integrating a database for data
persistence.
