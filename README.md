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

* **URL Params**

`GET` **Required** `subject=[String]` ** OR ** `body=[String]`

* **Data Params**

`POST` **Header** `Content-Type='text/xml'` 

example of body

```
<?xml version="1.0" encoding="UTF-8"?><SiebelMessage
 MessageId="1-I085"
 IntObjectName="GMvn Email Bucketing"
 MessageType="Integration Object"
 IntObjectFormat="Siebel Hierarchical"
><ListOfGmvnEmailBucketing>
<Action>
<ActivityId>1-1F44EE</ActivityId>
<Comment>
Hello Support,

 

Please look into my billing issue?

 

Thanks,

Ashish

Nothing in this message is intended to constitute an electronic signature unless a specific statement to the contrary is included in this message.

Confidentiality Note: This message is intended only for the person or entity to which it is addressed. It may contain confidential and/or privileged material. Any review, transmission, dissemination or other use, or taking of any action in reliance upon this
 message by persons or entities other than the intended recipient is prohibited and may be unlawful. If you received this message in error, please contact the sender and delete it from your computer.</Comment>
<Objective></Objective>
<SubType></SubType>
</Action>
</ListOfGmvnEmailBucketing>
</SiebelMessage>
```

 **Success Response:**

  * **Code:** 200 <br />
    **Content:** `<?xml version="1.0" encoding="UTF-8"?>
<SiebelMessage MessageId="1-I085" IntObjectName="GMvn Email Bucketing" MessageType="Integration Object" IntObjectFormat="Siebel Hierarchical">
    <ListOfGmvnEmailBucketing>
        <Action>
            <ActivityId>1-1F44EE</ActivityId>
            <Comment>Hello Support, Please look into my billing issue? Thanks,AshishNothing in this message is intended to constitute an electronic signature unless a specific statement to the contrary is included in this message.Confidentiality Note: This message is intended only for the person or entity to which it is addressed. It may contain confidential and/or privileged material. Any review, transmission, dissemination or other use, or taking of any action in reliance upon this message by persons or entities other than the intended recipient is prohibited and may be unlawful. If you received this message in error, please contact the sender and delete it from your computer.</Comment>
            <Objective>Billing</Objective>
            <SubType></SubType>
        </Action>
    </ListOfGmvnEmailBucketing>
</SiebelMessage>`

* **Error Response:**

Ungoing work, didn't finish yet

## Contact

Jiaqi Ma jiaqi.ma@gm.com

