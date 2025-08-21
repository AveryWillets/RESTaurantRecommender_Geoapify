# RESTaurantRecommender_Geoapify
This project, made in C++ 17, provides the user with restaurant suggestions through connecting with the GeoApify API.

The user inputs a ZIP code and food preference keyword, then the program makes two api requests to Geoapify: 1: Converts ZIP to lat/lon (region-locked to US, to modify just change the filter on the CURL request string) 2: Retrieves restaurant from around the given coordinates that match the keyword (keyword is currently buggy)
The program then parses the response using nlohman::json, a publicly available json parsing tool. Finally, the program outputs the restaurants that meet the criteria for the user, providing them with suggestions on where to go for food.
Hungry and don't know where to go? This RESTaurant Recommender will let you know!
This project requires a variety of dependencies. I recommend using MVSC's libcurl library if possible. Make sure to copy any necessary DLLs from the downloaded bin folder to the project folder before building.
