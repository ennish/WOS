# HMMS_WO_WS
This project provided the web service for WOS.  
[Online](https://github.com/ennish/WOS)
## To build the project

``` 
cd HMMS_WOS_WS 
mvn clean package
```
The HMMS_WOS_WS.war should be found under target if the command runs successfully.

## To replaced the masked sql with real one
Replace the files under `src/main/resources/mapper` with `src/main/resources/mapper.bak`
and package again.

## To fix sql of web service
1. **Find the mapper**
     
    ![Controller layer](https://github.com/ennish/WOS/blob/main/controller.png?raw=true)
     
    ![Service layer](https://github.com/ennish/WOS/blob/main/service.png?raw=true)
    
    ![DAO layer](https://github.com/ennish/WOS/blob/main/mapper.png?raw=true)
     
2. **Replace sql statement**  
    Please not to change alias of existing columns, cause it's used by `ResultMap`.  
    If new column need to add, new attributes need to add in `com.hmms.wos.model.XXX`
    and add a new line of  `result` in the `ResultMap`.
    
    
