# Account Operations

Use the account operations to perform account related actions

## Retrieve account balance info

```java
AirtimeAPI airtimeAPI = AirtimeAPI.builder()
        .clientId(clientId)
        .clientSecret(clientSecret)
        .environment(Environment.SANDBOX)
        .build();

Request<AccountBalanceInfo> request;
try {
    request = airtimeAPI.accounts().getBalance();
} catch (ReloadlyException e) {
    // api error retrieving access_token
}

AccountBalanceInfo accountBalanceInfo = null;
try {
    accountBalanceInfo = request.execute();
} catch (APIException e) {
    // api error
} catch (ReloadlyException e) {
    // request error
} catch (Exception e) {
    // all others
}  
```