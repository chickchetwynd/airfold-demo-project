# Airfold CLI Project

This project is a simple demonstration of using Airfold to model basic product conversion metrics using event data.
It shows how to use Airfold Pipes to process clickstream events and expose a published API to serve conversion insights.

✅ What This Project Does
It calculates conversion rates per product based on:

Page View to Cart

Cart to Purchase

Page View to Purchase

Using a small ~6000 row sample dataset, it walks through:

Building multi-step SQL Pipes

Publishing results as an API endpoint

## Setup

Create a virtual environment and install dependencies:

```bash
`python3 -m venv venv && source venv/bin/activate`
`pip install -r requirements.txt`
```

Create an Airfold workspace

Go to https://app.airfold.co and create a new Workspace.

Run

```bash
af config init
```

When prompted, enter your key found on the Airfold UI.

Then run:

```bash
af push
af source append events.csv
```


This will upload the demo dataset, the schema, as well as a transformation pipeline (Called a pipe in Airfold)