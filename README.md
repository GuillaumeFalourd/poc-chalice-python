# poc-chalice-python

![title](/docs/chalice-python.png)

Repository inspired from [this video tutorial](https://www.youtube.com/watch?v=r60-90Stb2o&ab_channel=DevOpsJourney)

## What is Chalice?

**AWS Chalice** allows you to quickly create and deploy applications that use Amazon API Gateway and AWS Lambda. It provides: A command line tool for creating, deploying, and managing your app. A familiar and easy to use API for declaring views in python code. Automatic IAM policy generation.

## Installing Chalice

```bash
python3 -m pip install chalice
```

## Chalice Quickstart

[https://aws.github.io/chalice/quickstart.html](https://aws.github.io/chalice/quickstart.html)

## AWS Config Setup

[https://boto3.amazonaws.com/v1/documentation/api/latest/guide/configuration.html](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/configuration.html)

## New Projects

```bash
chalice new-project <project_name>
```

## Deploying

Before you can deploy an application, be sure you have credentials configured. If you have previously configured your machine to run boto3 (the AWS SDK for Python) or the AWS CLI then you can skip this section.

If this is your first time configuring credentials for AWS you can follow these steps to quickly get started:

```bash
$ mkdir ~/.aws
$ cat >> ~/.aws/config
[default]
aws_access_key_id=YOUR_ACCESS_KEY_HERE
aws_secret_access_key=YOUR_SECRET_ACCESS_KEY
region=YOUR_REGION (such as us-west-2, us-west-1, etc)
```

Then run:

```bash
chalice deploy
```

## Testing

To start the server locally, run:

```bash
chalice local --host 0.0.0.0
```

Then you can access on your navigator:

- `http://0.0.0.0:8000` to get the `Hello World` JSON implemented on the `app.py` file.

- `http://0.0.0.0:8000/time` to get the current time.

- POST a message on `http://0.0.0.0:8000/echo` to see the same message returned.

- `http://0.0.0.0:8000/country/{country_name}` to get the covid-19 datas in JSON format from the informed country.

- `http://0.0.0.0:8000/price/{symbol}` to get cryptocurrencies price values 
  - [The full list of symbol can be obtained from here](https://coinmarketcap.com/api/documentation/v1/#section/Standards-and-Conventions).
  - This endpoint needs a valid [API KEY from coinmarketcap.com](https://coinmarketcap.com/api/documentation/v1/#section/Introduction) set on the [chalicelib file](https://github.com/GuillaumeFalourd/poc-chalice-python/blob/main/chalicelib/__init__.py) to work.
