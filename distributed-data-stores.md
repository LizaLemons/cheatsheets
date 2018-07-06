
# Distributed Systems - Distributed Data Stores

---


### Examples of other distributed systems
- Distributed data stores
- Distributed computing
- Distributed file systems
- Distributed messaging
- Distributed applications


---


### What is a distributed system & distributed data stores?

Usually when we build a web app, we use a single database on a single machine.

What happens if our app becomes an overnight sensation & suddenly we have millions of users?

We have two options:
- We can **scale vertically** by increasing the hardware of our current machine
- Or we can **scale horizontally** by *distributing* our database across several machines


---


### Pros of a distributed system

- Reduce the chance of downtime (if one machine catches fire, we have 9 others to back it up)
- Scaling horizontally means you can scale infinitely (if we scale vertically, we can only add so much hardware)
- Low latency (if machines are dispersed geographically, traffic can hit the closest server)
- Incredible performance & scalability at the cost of consistency or availability


---


### Cons

- Can be challenging to deploy & maintain a distributed data store. For this reason, if a system is distributed, it has been done out of necessity.
- Propagation of new information across all databases does not happen instantaneously. Usually, there is a "master" DB that you write to, & "slave" DBs that you use to read data. This improves availability, but if you write to the master, the slave may not immediately be able to read the new data.


---


### Partitioning

**Partitioning**: split your server into multiple smaller servers. These smaller servers, called *shards*, all hold different database records, for example, perhaps one shard holds all DB records for users with the last names A-M and the second N-Z.

Pros:
- We only access the shard we need based on the user's last name

Con:
- What happens if more users have the last names A-M & this shard becomes overworked?


---


### ACID

Usually, DBs follow the ACID theory.

Atomicity • Consistency • Isolation • Durability


---


**Atomicity:** Incomplete transactions will be reverted; meaning the DB tracks the transactions start to finish

**Consistency:** If one part of a transaction didn’t work, none of it works, which ensures that your DB goes from one valid state to another, no failures

**Isolation:** If two transactions happen simultaneously, or need to happen in conjunction, the DB should be able to isolate those activities and execute them both

**Durability:** After a transaction is successful, your data should persist continuously so you can always access it.


---


### BASE

But distributed systems follow the BASE theory.

Basically Available • Soft state • Eventual consistency


---


**Basically Available:** The system always returns a response

**Soft state:** The system could change over time

**Eventual consistency:** data will spread to every node sooner or later - thus becoming consistent  









---
