# custom-builder

Below are the steps we need to follow to generate custom builder <br>
================ PYTHON =============== <br>
oc project mangalxshukla-intel <br>
cd C:\Users\mshuklax\GitHub\CustomBuilderImage\python-custom <br>
\> openshift\oc new-build --strategy docker --binary --name python-custom4 <br>
\> oc start-build python-custom4 --from-dir="." --follow <br>

And then use that for another build in Dockerfile as a base image in FROM element(already done in python-applied). Then generate image using below commands - <br>
cd C:\Users\mshuklax\GitHub\CustomBuilderImage\python-applied <br>
\> oc new-build --strategy docker --binary --name python-applied13 <br>
\> oc start-build python-applied13 --from-dir="." --follow <br>
