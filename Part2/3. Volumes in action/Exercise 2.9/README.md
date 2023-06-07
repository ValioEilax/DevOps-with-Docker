## Changes to Backend file
I added /api to ENV REACT_APP_BACKEND_URL=http://localhost to get the Path right.

## Changes to Docker Compose file
I needed to change nginx and postgres images to nginx:1.19-alpine and postgres:13.2-alpine for some reason. At least they work now...

