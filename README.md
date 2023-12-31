# Unhandled-exception-charmap-codec
MySQL Workbench Error Unhandled exception: 'charmap' codec byte Ox81 in position 4053: character ma &lt; undefined>

![image](https://github.com/MEIVIKAS/Unhandled-exception-charmap-codec/assets/105585314/56e56350-a6ab-44f2-abbf-8fca567baf0d)


This error occurred when I tried to import a CSV file that I had downloaded from the following Kaggle dataset: [Top 250 Football Transfers from 2000 to 2018](https://www.kaggle.com/datasets/vardan95ghazaryan/top-250-football-transfers-from-2000-to-2018).
![image](https://github.com/MEIVIKAS/Unhandled-exception-charmap-codec/assets/105585314/5892cb7d-d0a9-458b-abd2-5da5903baf31)


Despite trying various solutions, none of them seemed to work for me. Therefore, I found a workaround by converting the problematic CSV file to a JSON file. I used the website [csvjson.com](https://csvjson.com/csv2json) to perform the conversion, but you can use any other tool or method you prefer.
![image](https://github.com/MEIVIKAS/Unhandled-exception-charmap-codec/assets/105585314/aad4a0c9-3828-4fea-9a09-f84abc9c0942)


The error was caused by the presence of player names in the dataset written in Latin script, which MySQL Workbench didn't handle well. Examples of affected names include "LuÃ­s Figo" and "HernÃ¡n Crespo." However, during the import process, MySQL replaced these Latin script characters with some other characters.
![image](https://github.com/MEIVIKAS/Unhandled-exception-charmap-codec/assets/105585314/0ce082bb-8dcc-4f1c-a663-d5c36747a78c)

As a data scientist, I documented this solution in my GitHub account to help others who might encounter a similar issue.

