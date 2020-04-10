# Bticino X8000 Rest Api
Chronothermostat Bticino X8000 Rest Api

**BY NOW READ ONLY**

[![stable](http://badges.github.io/stability-badges/dist/stable.svg)](http://github.com/badges/stability-badges)

## 1. First step

### 1.1. Register a Developer account
Sign up for a new Developer account on Works with Legrand website (https://developer.legrand.com/login).

### 1.2. Subscribe to Legrand APIs
Sign in, go to menu "API > Subscriptions" and make sure you have "Starter Kit for Legrand APIs" subscription activated; if not, activate it.

![Alt text](/../test/screenshots/subscription.PNG?raw=true "App Register")

### 1.3. Register a new application
Go to menu "User > My Applications" and click on "Create new" to register a new application:
- Insert a **valid public URL** in "First Reply Url". 
- Make sure to tick the checkbox near scopes `comfort.read` and `comfort.write`

Submit your request and wait for a response via email from Legrand (it usually takes 1-2 days max).
If your app has been approved, you should find in the email your "Client ID" and "Client Secret" attributes.

```
Public Url = https://myWebServerIP:myWebServerPort/rest
```
```
First Reply Url = https://myWebServerIP:myWebServerPort/callback
```
![Alt text](/../test/screenshots/app1.png?raw=true "App Register")
![Alt text](/../test/screenshots/app2.png?raw=true "App Register")

## 2. API CONFIGURATION

### 2.1. Install Requirements
- python3 pip3

- To install **Api Requirements** run:
  ```
  pip3 install -r requirements.txt
  ```

### 2.2. Update your config.yml
client_id: "Recived via mail"<br>
client_secret: "Recived via mail"<br>
subscription_key: "Your Subscription Key"<br>
redirect_url: "Your VALID Redirect Url"<br>

### 2.3. Nat API port:5588 on your router/firewall (Only for the first Oauth)

## 3. API START
### 3.1. Run app
```
python3 bticino.py
```
### 3.2. 1st RUN
- Navigate to http://my_api_ip:5588/get_code and click ***get your code***

![Alt text](/../test/screenshots/api1.png?raw=true "Api Allow")

- **Login with your developer account**


![Alt text](/../test/screenshots/api2.png?raw=true "Api Allow")

- **Allow your app permissions**


![Alt text](/../test/screenshots/api3.png?raw=true "Api Allow")

- **If you see your Plant Info enjoy!!**


![Alt text](/../test/screenshots/api4.png?raw=true "Api Allow")

### 3.3. Request Thermostat status

- **Navigate to http://my_api_ip:5588/rest**

**ll return a json with the status of your thermostat!**


![Alt text](/../test/screenshots/api5.png?raw=true "Api Allow")


## 4. HOME ASSISTANT INTEGRATION

**Add my custom repository** https://github.com/andrea-mattioli/mattiols_hassio_repository








