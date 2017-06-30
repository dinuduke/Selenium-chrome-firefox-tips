# Selenium-Chrome-Firefox-Tips-Python
Selenium Chrome and Firefox automated browser tips for blocking images, geotagging, etc...

## Automated Browser testing --python

 In #dissablemodelsinselenium.py you can find a cheat code to minimize the time complexity while using selenium Chrome or selenium Firefox

#### Firefox Cheats: (Selenium) --python
     firefox_profile = webdriver.FirefoxProfile()
     firefox_profile.set_preference('permissions.default.stylesheet', 2)
     firefox_profile.set_preference('permissions.default.image', 2)
     firefox_profile.set_preference('dom.ipc.plugins.enabled.libflashplayer.so', 'false')

     driver = webdriver.Firefox(firefox_profile=firefox_profile)

 #### Chrome/Chromium Cheats:(Selenium)--python
     chromeOptions = webdriver.ChromeOptions()
     prefs = {"profile.managed_default_content_settings.images":2,
             "profile.default_content_setting_values.notifications":2,
             "profile.managed_default_content_settings.stylesheets":2,
             "profile.managed_default_content_settings.cookies":2,
             "profile.managed_default_content_settings.javascript":1,
             "profile.managed_default_content_settings.plugins":1,
             "profile.managed_default_content_settings.popups":2,
             "profile.managed_default_content_settings.geolocation":2,
             "profile.managed_default_content_settings.media_stream":2,
    
    
             }
     chromeOptions.add_experimental_option("prefs",prefs)
     driver = webdriver.Chrome(chrome_options=chromeOptions)
     
 #### Executing Automated browser using selenium: --python
 
     driver.get('https://www.hubspot.com/')
     driver.close()
 
 **if any comments leave below**
