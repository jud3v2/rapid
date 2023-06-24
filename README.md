# Rapid Rust project

This project is open source.

### The issue:
make data more accessible and more fast around the world


This project written in rust allow users to use an orm that implements redis cache multi instances around the world’s for cdn with by example cloudflare headers location or vercel edge headers location to get users more closer to the database cache instance, when data is written in the cache they will be sent automatically or after the specified developer config to the Database

this is the schema:

Redis cluster exmple region | SQL Instance
FR                          | FR
US
EN

when u make a request trough’s cdn by exemple you are in France country and you make a request to the England country, rapid will parse the request

rapid parse the headers sent by client cdn in england country using cloudflare worker
we parse location headers and see the french location
we will make a request to french location if cache exist if not we will make the request to the england
after that we will revalidate cache of used data
