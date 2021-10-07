# Move Server

{% api-method method="post" host="https://api.cakes.com" path="/v1/customer/user/otpSend" %}
{% api-method-summary %}
OTP Send
{% endapi-method-summary %}

{% api-method-description %}
OTP Send
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="mobile" type="string" required=true %}
customer Mobile Number
{% endapi-method-parameter %}

{% api-method-parameter name="transType" type="number" required=true %}
Unique type of the transaction
{% endapi-method-parameter %}

{% api-method-parameter name="UUID" type="string" required=true %}
Unique Id
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully send the OTP
{% endapi-method-response-example-description %}

{% tabs %}
{% tab title="Plain Text" %}
```
{
  "responseCode" : "00",
  "responseMessage" : "OTP Sent successfully",
  "transType" : "02",
  "UUID" : "982072e2-6991-434e-9040-d49e71a09fb2",
  "userId" : "1"
}
```
{% endtab %}
{% endtabs %}
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



