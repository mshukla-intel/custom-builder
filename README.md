# custom-builder

Below are the steps we need to follow to generate custom builder \n
================ PYTHON ===============
oc project mangalxshukla-intel
cd C:\Users\mshuklax\GitHub\CustomBuilderImage\python-custom
\> openshift\oc new-build --strategy docker --binary --name python-custom4
\> oc start-build python-custom4 --from-dir="." --follow

And then use that for another build in Dockerfile as a base image in FROM element(already done in python-applied). Then generate image using below commands - 
cd C:\Users\mshuklax\GitHub\CustomBuilderImage\python-applied
\> oc new-build --strategy docker --binary --name python-applied13
\> oc start-build python-applied13 --from-dir="." --follow
