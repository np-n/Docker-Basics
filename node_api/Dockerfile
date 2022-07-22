# Create base image
# Use the node image as the parent image and use the alpine linux distribution with node 18 installed

FROM node:18-alpine

# Set the /app as the working directory
WORKDIR /app

# To copy all the source code to the image
# Copy all the files from the source directory to the folder app inside the image
COPY . .


# To install the dependencies into the image
RUN npm install

# The EXPOSE instruction informs Docker that 
# the container listens on the specified network ports at runtime. 
# The EXPOSE instruction exposes the specified port and makes it available only for inter-container communication
EXPOSE 4000

# Run the node application
# We only want to run the node application when the container of the image has been created.
# But we doesn't want to run the NODE application at the build time
# So we are not used RUN command here
# Instead of RUN, if we will use CMD command, which will run when we run the Container
# So, when container is run it will run the command node app.js which will ultimately run the node app
CMD ["node","app.js"]