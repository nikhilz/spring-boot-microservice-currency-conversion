# spring-boot-microservice-currency-conversion
 Currency Conversion Microservice
 
 Forex-service : https://github.com/nikhilz/spring-boot-microservice-forex-service
 
 Overview:
 
* Currency Conversion Service (CCS) can convert a bucket of currencies into another currency. It uses the Forex Service to get current currency exchange values. CCS is the Service Consumer. (Use of Feign Load Balancer) 
* We are using Ribbon to distribute load between the two instances of Forex Service.

<img src= "https://github.com/nikhilz/spring-boot-microservice-currency-conversion/blob/master/src/main/resources/static/Spring-Boot-Microservice-1-CCS-FS.png" >


 
 GET to http://localhost:8100/currency-converter/from/EUR/to/INR/quantity/10000
````
{
  id: 10002,
  from: "EUR",
  to: "INR",
  conversionMultiple: 75,
  quantity: 10000,
  totalCalculatedAmount: 750000,
  port: 8000,
}
 ````
 
 [Ref](https://www.springboottutorial.com/creating-microservices-with-spring-boot-part-3-currency-conversion-microservice)
