# Use Ubuntu as the base image
FROM ubuntu

# Set the working directory in the container
WORKDIR /app
COPY requirements.txt .

# Install Python and pip
RUN apt-get update && \
    apt-get install -y python3 python3-pip python3-venv

# Setup virtual env
ENV VIRTUAL_ENV=/opt/venv
RUN python3 -m venv $VIRTUAL_ENV
ENV PATH="$VIRTUAL_ENV/bin:$PATH"


# Install Jupyter Notebook
RUN pip3 install notebook
RUN pip3 install -r requirements.txt


# Command to run Jupyter Notebook
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--no-browser", "--allow-root"]
