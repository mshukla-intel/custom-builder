FROM image-registry.openshift-image-registry.svc:5000/mangalxshukla-intel/python-custom4@sha256:35a57ce77359e999ed833d3ad328c5e19e42d1f06765953d81b457de08fa7b5e
#FROM registry.access.redhat.com/ubi8/python-38
# Add application sources to a directory that the assemble script expects them
# and set permissions so that the container runs without root access
USER 0
ADD . .
RUN chown -R 1001:0 ./
USER 1001

# Install the dependencies
RUN pip install -U "pip>=19.3.1" && \
    pip install -r requirements.txt
    # python app.py collectstatic --noinput && \
    # python app.py migrate

# Run the application
CMD python app.py
        # runserver 0.0.0.0:8080