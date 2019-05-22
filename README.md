# Promregator

[![Build Status](https://travis-ci.com/zuhlke/ah-poc-promregator.svg?branch=master)](https://travis-ci.com/zuhlke/ah-poc-promregator)

PCF service discovery for prometheus metrics.

## Deployment to PCF

Promregator requires PCF credentials and configuration in order to do its job. This means that it needs environment variables passed through to 
its execution environment when it deploys. The easiest way to do this is to pass them through the PCF manifest.

We do not want to store the PCF credentials and configuration directly in this repo, so we inject them into the pipeline using travis.

These variables, injected by travis, are then used to dynamically create a PCF deployment manifest, `manifest.yml`, as part of the travis build. 
This manifest is used to deploy the app and run it in PCF, with all the required variables passed through.


