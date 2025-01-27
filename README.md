# New_york-trips-data-engineering-zoomcamp
Running Postgres with Docker using new-york dataset

Docker and SQL
## Running postgres with Docker
Run the below code on cmd if using windows. Ensure docker is inatlled on local machine.

docker run -it
-e POSTGRES_USER="root" 
-e POSTGRES_PASSWORD="root" 
-e POSTGRES_DB="ny_taxi" 
-v "./ny-taxi-volume:/var/lib/postgresql/data" 
-p 5432:5432 --name pgdatabase --net pg postgres:13

# Test
Install pgcli: Run code on cmd.
pip install pgcli

# NY Trip dataset
Dataset 
https://www.google.com/url?q=https://s3.amazonaws.com/nyc-tlc/trip%2Bdata/yellow_tripdata_2021-01.csv&sa=D&source=editors&ust=1737098258057413&usg=AOvVaw1O25h1PHKMant0Kr5Nyt_B
>>>>>>> 11f799b4d16a87ac8bed5e14b10744b241f5a57c


### Create a docker image

Ensure you have dockerfile. If not use the cmd command to create the Dockerfile
New-Item -Path . -Name "Dockerfile" -ItemType "file"


Build the image
docker build -t taxi_ingest:v001 .


