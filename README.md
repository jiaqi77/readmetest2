# Email classification 

The program is to classify the email to the folloing 4 categories

1. Account Status
2. Reservation
3. Billing
4. General 

It contains batch processing (from db) & API 
## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development purposes. 

### Prerequisites

It requires Python 3 installed. Also install the certain python packages using pip

nltk
```
pip install nltk
```
You might have issue with proxy, try the next step
```
pip install nltk --proxy http://10.81.68.10:8080
```
test installation: ```Start>Python36```,then type ```import nltk```

more instructions find http://www.nltk.org/ 

Install flask

```
pip install flask
```
For batch process, it connects to oracle database (optional)

```
pip install cx_Oracle
```
install Oracle Instant Client
instructions can find http://cx-oracle.readthedocs.io/en/latest/installation.html

Note: Python version, cx_Oracle and oracle instant Client should be in  the same windows redistributables (all 32 or 64)

## Run the code

In Python Spyder IDE, run ```mainapi.py```

you will get ```* Restarting with stat```

The program is running in localhost:5000

* **URL**

/emailclassification/1.0

* **Method:**

`GET` | `POST` 

## Contact

Jiaqi Ma jiaqi.ma@gm.com

