# HMMS_WO_WS
This project provided the web service for WOS.
[url](https://drive.google.com/file/d/1jj5ElhjIJ6LJ-tkcUv3nSjLIj8OHoB2G/view?usp=sharing)
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
     
    ![Controller layer](https://drive.google.com/file/d/1QFrhxPViSp6pPh8gNXsQRQ2EegrTmXvU/view?usp=sharing)
     
    ![Service layer](https://drive.google.com/file/d/12-_elS5lGC8sBGO-Ccy_G50LT28CHv2p/view?usp=sharing)
    
    ![DAO layer](https://drive.google.com/file/d/1nEZuBzaUCmVSsZ1E_1oiQZ3wx9mzMw4Z/view?usp=sharing)
     
2. **Replace sql statement**  
    Please not to change alias of existing columns, cause it's used by `ResultMap`.  
    If new column need to add, new attributes need to add in `com.hmms.wos.model.XXX`
    and add a new line of  `result` in the `ResultMap`.
    
    
