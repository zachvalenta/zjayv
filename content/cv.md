+++
title = "resume"
template = "cv.html"
+++

---

https://gaultier.github.io/blog/body_of_work.html

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

https://github.com/lusingander/serie/issues/53
* __technical writer__: Stack Overflow ([threads vs. processes](https://stackoverflow.com/a/47824267), [debugging](https://stackoverflow.com/a/61151333), [Docker Compose inheritance](https://stackoverflow.com/a/63585954)), [technical article](https://github.com/zachvalenta/nginx-wsgi) covered by [Python Bytes podcast](https://pythonbytes.fm/episodes/show/120/aws-mongodb-and-the-economic-realities-of-open-source-and-more)
* __code contributor__: [The Hitchhiker's Guide to Python](https://www.amazon.com/Hitchhikers-Guide-Python-Practices-Development/dp/1491933178/ref=as_li_ss_il?ie=UTF8&linkCode=li2&tag=bookforkind-20&linkId=804806ebdacaf3b56567347f3afbdbca) (PRs on [loguru](https://github.com/realpython/python-guide/pull/993), [Clint](https://github.com/realpython/python-guide/pull/970)), various ([Portray](https://github.com/timothycrosley/portray/blob/master/docs/contributing/4.-acknowledgements.md), [CPython](https://github.com/python/cpython/pull/14538), [ptpython](https://github.com/prompt-toolkit/ptpython/issues/304), [bandit](https://github.com/PyCQA/bandit/issues/471), [fff](https://github.com/dylanaraps/fff/pull/116))

# EXPERIENCE

## 🏀 Kero Sports

🗓️ 2025.10-present

---

### pregame resolution

https://bitbucket.org/kerogaming/rush_ml_v2/pull-requests/4844
* lookup error happens (per Sentry) on market_info.get("form_actionNumber")
* nothing has changed in the code around this LOC for 2+ years
* which makes me think this is a data issue, not a code issue
* all the issues seem to be with pre-game markets
* pregame markets don't have PBP data
* pregame markets can (will occasionally? always? never?) have null actionNumber
* when the game starts, we attempt to resolve all markets, incl. pregame
* if pregame markets lack actionNumber, they can't resolve
* so why is this only happening for *select* pregame markets (e.g. P_4_23_5, P_4_29_4)?
* we seemingly handle pregame market state mgmt via get_pregame_publish_market, which *should* be picking up P_4_23_5, P_4_29_4, and so forth
* these markets have ownership of their own unpublish logic (unlike other pregame markets?? "There should be one - and preferably only one - obvious way to do it.")
```python
class P_4_23_5(v.TeamNextOffensivePossessionResult):
    ...
    @classmethod
    def resolve_market(cls, event_info, market, last_row, con: BasketballRmgWorkDB):
        ...
        if last_row.get(
            "@matchstatus"
        ) != BetRadarMatchStatus.NOT_STARTED and not market.get("unpublished"):
            res = ResolveOption.UNPUBLISH
```
* so the issue could be that when we try to resolve them via BasketballRmgResolving.run(), we're trying to lookup form_actionNumber before their own internal unpublish mechanism resolve_market gets called, which means we'll hit this lookup error, which means we'll never resolve them.
* Ok, so here's a *potential* fix for this https://bitbucket.org/kerogaming/rush_ml_v2/branch/fix/basketball/pregame-unpublish-temp-fix?dest=feat_common_service
* The fix looks idiotically simple, I know, but think it will handle these deviant markets for now. Mid/long-term we should align them with their fellow pregame markets and move ownership of their resolution outside of themselves.

### stack

* FastAPI
* Sentry
* Mongo, Postgres
* Kafka, ARQ

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
