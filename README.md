# sample
from selenium import webdriver
path=("C:\\Users\\Dell\\PycharmProjects\\Selenium\\LaunchBrowsers\\chromedriver.exe")
driver=webdriver.Chrome(executable_path=path)
driver.implicitly_wait(30)
driver.maximize_window()
# navigate to the application home page
driver.get("http://google.com")
# get the search textbox
search_field = driver.find_element_by_name("q")
search_field.clear()
# enter search keyword and submit
search_field.send_keys("iphone")
search_field.submit()
# get all the anchor elements which have product names displayed
# currently on result page using find_elements_by_xpath method

product=driver.find_elements_by_xpath("//*[@id='vn1s0p1c0']/h3")
driver.quit()
