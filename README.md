# Integrating Redis Cache with SpringBoot Application 

# Introduction

Welcome to the Integrating Redis Cache with Spring Boot Application repository! In this project, we will explore the concept of caching, the reasons behind using Redis as a caching solution, and how to seamlessly integrate Redis with a Spring Boot application.

# What is Cache and Why Use Redis?

Caching is a technique used to store frequently accessed data in a temporary storage layer, allowing faster access and reducing the load on the primary data source. By caching data, we can avoid repetitive and resource-intensive computations or database queries, resulting in improved application performance and responsiveness.

Redis is an open-source, in-memory data structure store that serves as an excellent distributed caching solution. It provides lightning-fast read and write operations, making it an ideal choice for caching frequently used data. Redis also offers various data structures, enabling versatility in handling different types of cached information.

![image](https://github.com/vignesh6645/Cache/assets/86340986/7b1d5cf7-24be-4748-93e3-aa5cb80cef74)

# Project Overview

In this repository, you will find a Spring Boot application that demonstrates how to integrate Redis as a caching mechanism. The codebase is structured to help you understand the key components and configurations required for successful Redis cache implementation.

# Prerequisites

  Kindly learn the documentation about Redis Caching.

 # Installation

  Kindly ensure that redis installed in your local machine.
  if not installed using docker desktop pull latest redis image or using below link you can download and install it in your local machine.
   
       https://www.bing.com/searchpglt=41&q=redis+download+for+windows+11+git&cvid=8bd6b2c491694a64ab7ebd8cda097788&aqs=edge..69i57j0l8.12094j0j1&FORM=ANAB01&PC=HCTS 

 # Configuration

   1. Go to the Spring Initializer webPage
   2. Add the spring-boot-starter-data-redis and neccessory depedencies
   3. In application.yml file add below config
    
           spring:
              cache:
                type: redis
                redis:
                  cache-null-values: true
                  time-to-live: 100s

   4. Add ` @Cacheable("value") ` annotation to the API that needs caching.
   5. Using ` @CacheEvict Or @CachePut ` you can delete or modify the stored cache in redis.
      
      Note: Caches store data in a key-value model, enabling faster access and retrieval of frequently used information. we passed key in  
            @Cacheable("user") annotation so the caches are stored like user: [values]. If you want to check the caches go cmd and follow the below 
            instructions.

        ` type redis-cli in cmd `
        ` it shows your local Ip address: type ping `
        ` replies PONG and your Ip address `
        ` type keys *  after that you will get all of your stored catches`
        ` if you want to delete all the caches enter FLUSHDB `

        
        ` redis-cli `

  For Ref:          
  
        https://github.com/vignesh6645/IntegratingRedis-Cache-withSpringBoot

  # Conclusion
   I would like to extend my heartfelt gratitude to everyone reading this README file. Your interest and time are greatly appreciated. If you have any 
   suggestions, feedback, or improvements to contribute, please feel free to raise a pull request (PR) on this repository. Together, we can make this 
   project even better and help others learn about integrating Redis cache with Spring Boot applications. Thank you once again for your support! Happy 
   coding!
