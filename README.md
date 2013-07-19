Requestr
========
--------

Requestr is a simple API to make simple HTTP(currentily only GET method) requests. It uses libsoup behind the scenes.

## Dependencies
- valac-0.18
- libsoup-2.4

## Usage
Drop `Requestr.vala` file into your project `utils` directory and add the following compilation flag to your compile command.
```sh
--pkg lisoup-2.4 --thread
```
Create new instance of Requestr as following
```vala
var request = new Requestr("GET", "http://github.com");
```
and then send the request.
```vala
uint response_code = request.send ();
```
Access the response throught the `body` property, as shown bellow
```vala
stdout.write (request.body);
```
Have fun! :)

## Author
Diego Toral - <diegotoral@gmail.com>
