+++
title = "resume"
template = "cv.html"
+++

---

# ME

## profile

* [Github](https://github.com/zachvalenta)
* [LinkedIn](https://www.linkedin.com/in/zachvalenta/)
* [Stack Overflow](https://stackoverflow.com/users/6813490/zach-valenta?tab=profile)
* [personal site](http://www.zachvalenta.com/)

## skills

---

INFRA
* _AWS_: Lambda, CloudWatch, EC2, IAM
* _PaaS_: Cloud Foundry, Platform.sh
* _IaC_: [Terraform](https://github.com/zachvalenta/terraform-ec2), Ansible
* _operating systems_: [Linux](https://stackoverflow.com/a/47824267/6813490)
* _servers_: ([Nginx, Gunicorn](https://github.com/zachvalenta/nginx-wsgi))
* [Algolia](https://github.com/zachvalenta/mdn-scrape)

LANGUAGES
* _Python_: Django/DRF, Flask, FastAPI + libraries ([bpython, Black, bandit, coverage, loguru, pdoc, pytest, python-dotenv](https://github.com/zachvalenta/create-python-app)) scraping ([Scrapy, Beautiful Soup](https://github.com/zachvalenta/mdn-scrape))
* _JS_: Angular, [Vue](https://github.com/zachvalenta/vue-firebase), htmx, Selenium
* various: Java (Spring), PHP

DATA
* SQL, Mongo aggregation framework
* _dbms_: Postgres, Mongo, Oracle, MySQL/MariaDB, DuckDB
* _messaging_: RabbitMQ, Qpid, Kafka, ARQ
* _tooling_: visidata, litecli https://github.com/dbcli/litecli/pull/217
* _dataframes_: Polars, Pandas

## open source

---

* __technical writer__: Stack Overflow ([threads vs. processes](https://stackoverflow.com/a/47824267), [debugging](https://stackoverflow.com/a/61151333), [Docker Compose inheritance](https://stackoverflow.com/a/63585954)), [technical article](https://github.com/zachvalenta/nginx-wsgi) covered by [Python Bytes podcast](https://pythonbytes.fm/episodes/show/120/aws-mongodb-and-the-economic-realities-of-open-source-and-more)
* __code contributor__: [The Hitchhiker's Guide to Python](https://www.amazon.com/Hitchhikers-Guide-Python-Practices-Development/dp/1491933178/ref=as_li_ss_il?ie=UTF8&linkCode=li2&tag=bookforkind-20&linkId=804806ebdacaf3b56567347f3afbdbca) (PRs on [loguru](https://github.com/realpython/python-guide/pull/993), [Clint](https://github.com/realpython/python-guide/pull/970)), various ([Portray](https://github.com/timothycrosley/portray/blob/master/docs/contributing/4.-acknowledgements.md), [CPython](https://github.com/python/cpython/pull/14538), [ptpython](https://github.com/prompt-toolkit/ptpython/issues/304), [bandit](https://github.com/PyCQA/bandit/issues/471), [fff](https://github.com/dylanaraps/fff/pull/116))

# EXPERIENCE

## 🏀 Kero Sports

🗓️ 2025.10-present

---

* Sentry
* Mongo, Postgres
* Kafka

## 🟥 Capp

🗓️ 2024.08-2025.04

* __project__: ERP
* __role__: data eng
* __contribution__: set up EDI connection for suppliers, wrote product category tooling, modernized price updates (Polars, sqlite-utils, visidata)

## 💿 United Masters

🗓️ 2022.01-2023.12

* __project__: payments
* __role__: backend (Flask, Postgres, Mongo, Kafka)
* __contribution__: projects include hardening data ingregrity for Split Pay system, integrating Chargebee for subscriptions, moving from 3rd party royalty system to in-house replacement

## 🏦 Eliassen (BNY, Capital One)

🗓️ 2022.01-2023.12

* __project__: infrastructure automation
* __role__: backend (Flask, Django)
* __contribution__: CLI client and Flask server to run distributed go-to-production testing suites on bare metal and VMWare servers
* __project__: risk rating for sector-specific (real estate, energy) commercial lending
* __role__: backend (Flask, SQL, Docker)
* __contribution__: write microservices, establish SDLC patterns (repo standardization, code review)

## 🟦 JP Morgan

🗓️ 2016.12-2019.02

* __project__: feature-flagging system for high traffic clients (Chase.com)
* __role__: backend (Django, DRF, SQL) ops (Cloud Foundry, database migrations, load balancers)
* __contribution__: search, user/group perms, ER models
* __project__: CRM for HNW clients
* __role__: backend (PHP, SugarCRM, SQL) frontend (Angular1, Selenium)
* __contribution__: API integrations, Selenium integration test suite, Angular admin dashboard
