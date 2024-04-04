[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/TLLTF7bJ)

# **Artwork Infromation**
A web api to retrieve an infromation about an artwork.
## **Get Artwork Information**

**Request** 
Retrieve a list of artworks: GET request to /artwork

curl --location 'localhost:5000/artworks'

To retrieve artwork by ID: GET request to /artworks?id=123, where 123 is the ID of the artwork.

curl --location 'localhost:5000/artwork?id=1'

To retrieve artwork by title: GET request to /artworks?title=DesiredTitle replace DesiredTitle desired title

curl --location 'localhost:5000/artwork?title=Starry%2BNight'

**Post** 
To add new artwork: POST /artworks/art_id replace art_id to a desired art_id

curl --location 'localhost:5000/artwork/2' \
--header 'Content-Type: application/json' \
--data '{
    "title": "Bloody Night",
    "color": "red",
    "medium": "Watercolor on paper"
}'

**Put**
To update artwork: PUT /artwork/art_id replace art_id with existing art_id

curl --location --request PUT 'localhost:5000/artwork/2' \
--header 'Content-Type: application/json' \
--data '{
    "title": "Christmas Night",
    "color": "green",
    "medium": "Watercolor on paper"

}'

**Delete** 
To delete artwork: DELETE /artwork/art_id replace art_id with existing art_id

curl --location --request DELETE 'localhost:5000/artwork/2'