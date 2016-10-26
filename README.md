# Simple Salesforce SOAP Server

I often find myself wanting to test Saleforce's Web Service function but have problems finding a good sample SOAP service to test with. Frequently the WSDL2Apex parser complains and is not able to create the Apex classes for the endpoint. Therefore I built my own that you can modify to suit your needs.

Warning: this is a very simple server and most of the functionality is mocked.

I am currently unable to get Java to generate the WSDL file automatically with the endpoint address so I [added it my self](https://github.com/jeffdonthemic/simple-salesforce-soap-server/blob/master/public/calculator.xml#L174) and made it publicly available.

## Setup

Do a search and replace for `simple-salesforce-soap-server` with the name of your app (e.g., frisky-fox-5673).

The individual endpoints are defined in `conf/applicationContext.xml`. You can generate the WSDL for each service by appending `?wsdl` to the endpoint. For instance, to view the wsdl for HelloWorld service, go to `http://frisky-fox-5673.herokuapp.com/service/hello?wsdl`.

## Running Locally

Make sure you have [Play with Activator](https://www.playframework.com/download) installed.

``` activator play ```

```run```
