---
template: BlogPost
path: /covid-dashboard
mockup: /assets/covid/covid.png
thumbnail: "https://images.pexels.com/photos/3951355/pexels-photo-3951355.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
github: https://github.com/moonsmile-dev/covid19-dashboard
demo: https://ncov-dashboard.herokuapp.com/
date: 2020-12-01
name: COVID-19 Dashboard
title: A powerful yet intuitive COVID-19 analytics dashboard, attracting thousands of users.
category: Web app
description: "Powerful Django web application, tracking real-time coronavirus cases, with an intuitive & clean UI."
tags:
  - Python
  - Django
  - Plotly
  - Pandas
---

The goal of this project is not to build _just another dashboard_. But, to focus on collaborative plot ideas, and a mobile friendly UI/UX. Feel free to open an issue requesting a type of plot, table, or any feature for that matter. Join the repo's [Gitter chat](https://gitter.im/ncov-dashboard/community?utm_source=share-link&utm_medium=link&utm_campaign=share-link).

> Coronavirus disease (COVID-19) is an infectious disease caused by a newly discovered coronavirus.
> At this time, there are no specific vaccines or treatments for COVID-19. The best way to prevent and slow down transmission is be **well informed** about the COVID-19 virus. [who.int](https://www.who.int/health-topics/coronavirus#tab=tab_1)

![covid-2](/assets/covid/covid-2.png)

<figcaption>Mobile interactive plots</figcaption>

## Getting Started

Get the project installed and running locally in just a couple quicky and easy steps.
First, create a personal [Fork](https://github.com/login?return_to=%2FBrianRuizy%2Fcovid19-dashboard) of this repository. Then git **Clone** using your local terminal to a preferred location, and **cd** into the project.

1. Create & activate virtual environment

```bash
python -m venv env

source env/bin/activate  # Linux/Mac
env/Scripts/activate  # Windows
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Run local server, and **DONE**!

```bash
python manage.py runserver

May 06, 2020 - 11:22:23
Django version 3.0.6, using settings 'core.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```

## Deployment

Heroku app is already configured to this repository for _automatic deploys_ from any push to the **master** branch. Create a pull request containing your respective changes and wait for merge.

## Reading data locally

You can go through all the available datasets by going into the `/processdata` directory, launching a interactive python shell, importing `getdata` file, and calling any function.

```bash
cd covid19-dashboard/processdata
```

```bash
$ python

>>> import getdata
>>> getdata.realtime_growth()

         Confirmed  Deaths  Recovered
Date
1/22/20        555      17         28
1/23/20        654      18         30
...            ...     ...        ...
8/2/20    18079723  689362   10690555
8/3/20    18282208  693694   10913000

[195 rows x 3 columns]
```

## Built With

- [Django](https://www.djangoproject.com/) Django is a high-level Web framework that encourages rapid development and clean, pragmatic design.
- [Plotly](https://plotly.com/) The leading front-end for ML & data science models in Python, R, and Julia.
- [Appseed](https://appseed.us/)
- [Bootstrap](https://getbootstrap.com/)

## Data Sources

- Johns Hopkins University: [CSSE](https://systems.jhu.edu/) 2019-ncov data repository, found [here](https://github.com/CSSEGISandData/COVID-19).
- Our World in Data: [OWID](https://ourworldindata.org/) GitHub Data repository, found [here](https://github.com/owid/covid-19-data/tree/master/public/data).
- New York Times' COVID GitHub data repository, found [here](https://github.com/nytimes/covid-19-data)
