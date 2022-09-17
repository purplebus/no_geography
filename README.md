# Anastasia Dyakova T2a

> ## R1	Identification of the problem you are trying to solve by building this particular app.
> ## R2	Why is it a problem that needs solving?
> ## R3	Why have you chosen this database system. What are the drawbacks compared to others?

> ## R4	Identify and discuss the key functionalities and benefits of an ORM
> ## R5	Document all endpoints for your API
### Authoisational routes
- __@auth.route("/register", methods=["POST"])__
register new clients
- __@auth.route("/login", methods=["POST"])__
log in existing clients
- __@auth.route("/admin/login", methods=["POST"])__
admin login, jwt requred
### Tours routes
- __@tours.route("/", methods=["GET"])__
shows all tours
- __@tours.route("/<int:id>", methods=["GET"])__
shows information about a choosen by id tour
- __@tours.route("/add", methods=["POST"])__
adding new tour, by admin only, jwt required
- __@tours.route("/<int:id>", methods=["PUT"])__
update excisting tour, by admin only, jwt required
### Providers routes
- __@providers.route('/', methods=['GET'])__
shows all providers, by admin only
- __@providers.route("/<int:id>", methods=['GET'])__
shows 1 provider choosen by id, admin only
- __@providers.route("/add", methods=["POST"])__
adding new provider, admin only
### Bookings routes
- __@bookings.route('/', methods=["GET"])__

> ## R6	An ERD for your app
> ## R7	Detail any third party services that your app will use
- psycopg2 To create the connection in Flask we need Psycopg, which is the most popular PostgreSQL database adapter for Pytho
- SQLAlchemy SQLAlchemy is the ORM we will use to connect Flask and PostgreSQL, so let's install that as well:
- marshmallow. This means that the data we get from a database is not serialized, it is not considered a list. To do that we can get help of a package like marshmallow
- blueprintsBlueprints are basically a way of defining some of the properties of a Flask app in advance, so that you can pick when that definition takes effect, and even apply your defined behaviour to multiple apps if you want. 
- flask-bcrypt To keep the users password safe in our database we will use hashing. The technical definition of a hash function is the ability for the function to take a piece of data of any size and create a piece of data from the original in a fixed size.An example would be if we take a piece of text and hash it with a hasing function such as sha256. We are returned a piece of data with a fixed length of 256 bits. For our server we'll use a slow-hashing library like flask-bcrypt. I
from marshmallow import ValidationError
from marshmallow.validate import Length
- flask-jwt-extended

> ## R8	Describe your projects models in terms of the relationships they have with each other
> ## R9	Discuss the database relations to be implemented in your application
> ## R10	Describe the way tasks are allocated and tracked in your project