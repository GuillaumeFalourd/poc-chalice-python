# poc-chalice-python

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

```bash
chalice deploy
```

## Testing

To start the server locally, run:

```bash
chalice local --host 0.0.0.0
```

Then you can:

- Access `http://0.0.0.0:8000` on your navegator to get the `Hello World` JSON implemented on the `app.py` file.

- Access `http://0.0.0.0:8000/time` on your navegator to get the current time.

- POST a message on `http://0.0.0.0:8000/echo` to see the same message returned.

- Access `http://0.0.0.0:8000/country/{country_name}` to get the covid-19 datas in JSON format from the informed country.

- Access `http://0.0.0.0:8000/price/{symbol}` to get cryptocurrencies price values ([the full list of symbol can be obtained from here](https://coinmarketcap.com/api/documentation/v1/#section/Standards-and-Conventions)).
