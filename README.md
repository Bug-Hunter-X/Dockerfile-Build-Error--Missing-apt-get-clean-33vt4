# Dockerfile Bug: Missing apt-get clean
This repository demonstrates a common error in Dockerfiles: forgetting to run `apt-get clean` after installing packages. This can result in significantly larger image sizes and potential dependency conflicts.

## Bug
The original `Dockerfile` installs Python and its dependencies, but neglects to remove downloaded packages. This leads to a bloated image.

## Solution
The fixed `Dockerfile_fixed` includes `apt-get clean` to resolve this issue. This removes unnecessary downloaded packages and creates a smaller image.