```python
'''
Week 4: Project One. Task Manager
Question
You're working for an online marketplace. Users often search for products using keywords. Given a list of product names and their corresponding IDs, 
design a function that allows users to input a keyword and quickly find the product they are looking for. 
Implement a linear search algorithm to search for the keyword in the list of product names and return the corresponding product ID.

'''
#Though process
# create a list of dictionaries where we can have key, value pairs. This way we would be able to fix in the product name and its ID

location_dict = dict([("gas", 21), ("pot", 31), ("kettle", 38), ("spoon", 42), ("plates", 50), ("sink", 60)])

def find_product(product):
    location = location_dict.get(product)
    if location is not None:
        return location
    else:
        return "Product not found!"

def user_input():
    product_name = input("Enter the keyword of product you want to search for: ")
    local = find_product(product_name)
    print(f" The product ID is {local}.")
    
user_input()

```

    Enter the keyword of product you want to search for:  spoon
    

     The product ID is 42.
    


```python

```


```python
'''
Project 2: Movie recommender system 
Problem: Build a movie recommendation system that 
suggests movies to users based on their preferences. 
Create a class-based system where each user can rate 
movies. Use a dictionary to store movie ratings, and 
implement a recommendation algorithm that suggests 
movies similar to those the user has liked. The 
program should allow users to: i. Add new movies to the system. ii. Rate movies on a scale of 1 to 5. iii. Get recommendations based on the user's 
highest-rated movies using a 
recommendation decorator. 
Implement a function to find movies with the highest 
and lowest average ratings 

'''
```


```python
class User:
    def __init__(self, user_id, movies_rated, favorite_movies, favorite_genres, disliked_genres):
        self.user_id = user_id
        self.movies_rated = movies_rated
        self.favorite_movies = favorite_movies
        self.favorite_genres = favorite_genres
        self.disliked_genres = disliked_genres
        
        def __init__(self, user_id):
            self.user_id = user_id
        
        def rate_movie(self, movie):
            movie_rating = int(input("Rate this movie on a scale from 1-5, where 5 is best: "))
            self.movies_rated.append(movie)


class Movie(User):
    def __init__(self, movie_name, movie_id, rating, genre):
        super().__init__(movie_id)
        self.movie_name = movie_name
        self.rating = rating
        self.genre = genre
    
    def search_products(user_id, keyword):
        recommended_movies = []
        return recommended_movies

    for movie in user_id.movies_rated:
        if movie.genre == keyword:
            recommended_movies.append(movie)
return recommended_movies
    #return recommended_movies

# recommended_movies = []
# return recommended_movies

user_id = 1
user_movies_rated = ["American", "Korea", "Mexico", "Columbia", "Nigeria"]
movie = input("Enter the name of a movie to add to the user's list of movies: ")
user_movies_rated.append(movie)
keyword = input("Enter a keyword to search for movies: ")
recommended_movies = search_products(user_id, keyword)
print("The following movies match your keyword:")
for movie in recommended_movies:
    print(f"{movie}: Rating: {movie.rating}")
```
