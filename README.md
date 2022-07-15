# bubble_KodiTVDB
bubble_KodiTVDB


Configfile konfigurieren:


    #####2 SQL-Server (sql1,sql2)#####

        -----SQL-LITE-----
        "sql1":
        {
            "type":"sqllite",
            "filename":""
        },

        -----SQL-LITE-----
        "sql2":
        {   
            "active":true,
            "type":"mysql",
            "username":"",
            "password":"",
            "port":0
        },
    

    #####Programs#####

        -----Comparing Movies-----(sql1 & sql2)
        "program": ["movies","comp"]
            --Detail-level--
            "detail_level":1   (Only shows the name of the movie and on which side it doesn't exist)

        -----Comparing Series-----(sql1 & sql2)
        "program": ["tvseries","comp"]
            --Detail-level--
            "detail_level":1   (Only shows the name of the serie and on which side it doesn't exist)
            "detail_level":2   (Compares the amount of episodes and returns the difference if exists + level 1)
        -----Series-Double-Prevention-----(sql1)
         "program": ["tvseries","doubleprevent"]
            --Detail-level--
            "detail_level":1   (Only shows the name of the serie that exists 2 times)
        -----Series-Database-Print-----(sql1)
         "program": ["tvseries","dbprint"]
            --Detail-level--
            "detail_level":1   (Only shows the show, the amount of seasons and episodes)
	    "detail_level":2   (Prints the show with all the seasons and associated episodes f.e. Season:Episodes)
	    "detail_level":3   (Exports the whole DB as JSON)