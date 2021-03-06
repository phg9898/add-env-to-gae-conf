# Add env to Google App Engine config file

## What is it?

- It's a script to add environment variables to Google App Engine config file (app.xml)
- It adds environment variables to `app.xml` at deploy time.

## Why are you made it?

- Google App Engine config file is exposed environment variables in plain.
- I just want to make more secure that.

## When can I use it?

- When you deploy your code to Google App Engine by CD(Continuous Delivery) tool (e.g. Github Actions, Bitbucket pipelines, Circle CI, Etc.)

## How to use?

- Add names of environment variable that you want to add to `app.xml` to `.env.array`
- Add key/value of environment variable in your CD tool settings.
- Add commands to run this script to your CD tool config file.

## Warning

- It's only run correctly, when `app.xml` doesn't have `env_variables` field.
- You have to migrate all environment variables from `app.xml` to CD tool settings.

## Example
- [Bitbucket pipelines](./bitbucket-pipelines.yml)