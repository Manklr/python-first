Hope this works for the assignment as I got it on github but had alot of trouble with github pages giving me 404 error.

def display_results(weathers,city):

    print("{}'s temperature: {}°C ".format(city,weathers['main']['temp']))
   
    print("Wind speed: {} m/s".format(weathers['wind']['speed']))
   
    print("Description: {}".format(weathers['weather'][0]['description']))
   
    print("Weather: {}".format(weathers['weather'][0]['main']))


def main():
   
    city=input('Enter the city:')
   
    print()
   
   try:
      query='q='+city;
      
      w_data=weather_data(query);
      
      display_results(w_data, city)
      
      print()
      
   except:
   
      print('City name not found')

if __name__=='__main__':

   main()first
