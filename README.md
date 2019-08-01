This project creates a Docker Image with "sloppy cli".

Sloppy is a docker hosting platform, you can get more details here (https://sloppy.io/en/).

If you use GitLab CI as continuous integration and if you deploy your application to sloppy platform to run your application then 
you can use this docker image to execute sloppy cli from GitLab.

For example:
In the gitlab-ci.yml you can use the following lines to deploy your application

<pre>
deploy-app-in-sloppy:
  image: mhock/sloppy-cli:latest
  stage: [stage-name]
  script:
    - sloppy change -img [image-name] [app-name]
</pre>

<pre>
where as:
  image-name: name of the docker image, which has been build by the gitlab build pipeline
  app-name: is the name of your application in the sloppy platform
</pre>

For more details about the sloppy cli please follow the following link: https://kb.sloppy.io/en/collections/156128-features#cli-command-reference

Under the following link (https://kb.sloppy.io/en/articles/915327-step-1-install-the-cli) you will find overview of sloppy commands.

To learn more about gitlab ci please follow the following link https://docs.gitlab.com/ee/ci/examples/README.html
