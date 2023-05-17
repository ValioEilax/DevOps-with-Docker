# Start from the Ubuntu:20.04 image and add instructions to install curl into that image.
FROM ubuntu:20.04
RUN apt-get update && apt-get install -y curl

# Use /usr/src/app as our workdir. The following instructions will be executed in this location.
WORKDIR /usr/src/app

# Copy the scipto.sh file from this location to /usr/src/app/ creating /usr/src/app/script.sh
COPY script.sh .

# Alternatively, if we skipped chmod earlier, we can add execution permissions during the build.
RUN chmod +x script.sh

# When running Docker run the command will be ./script.sh
CMD ./script.sh
