# ![Forest AI](/doc/asset/forest-ai-name-logo.png?raw=true)

[![License](https://img.shields.io/badge/License-Apache2-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0) [![Slack](https://img.shields.io/badge/Join-Slack-blue)](https://join.slack.com/t/forest-ai-workspace/shared_invite/zt-ga90t9yr-xI3Dc9sYd2T5l1Hdd8TeJQ) [![Website](https://img.shields.io/badge/View-Website-blue)](https://forestai.tech/)

## Contents

1. [Short description](#short-description)
1. [Demo video](#demo-video)
1. [The architecture](#the-architecture)
1. [Long description](#long-description)
1. [Project roadmap](#project-roadmap)
1. [Getting started](#getting-started)
1. [Running the tests](#running-the-tests)
1. [Live demo](#live-demo)
1. [Built with](#built-with)
1. [Contributing](#contributing)
1. [Versioning](#versioning)
1. [Authors](#authors)
1. [License](#license)
1. [Acknowledgments](#acknowledgments)

## Short description

### What's the problem?

Forest are essential for life on earth, they regulate our climate, filter the water, purify the air. But they are being destroyed at an alarming rate. Every two second forest area size of a football field is destroyed due to illegal logging.

Deforestation accounts for more greenhouse gases than trains, planes and cars of the whole planet combined. It contributes 17% to climate change while vehicles contribute 13% only. According to the interpole 90% logging is illegal which means, preventing it can be the easiest and the cheapest way to fight the climate change. Local law enforcement try their best to protect it but illegal logging is hard to detect due to dense and wide forest.

### How can technology help?

If we can design a system that can monitor whole forest area 24/7 and detect the enviromental acostics autonomously, first responders can show up stop any illegal activity happening.

### The idea

Welcome to Forest AI ! A vigilant system that detects and alerts illegal deforestation in realtime. A smart solar powered device is deployed under tree canopies listening for all sorts of sounds. As soon as sound of chainsaw is detected in forest, device picks it up and sends an alert through a standard cellphone network to the nearest forest-ranger & first responders so that they can intervene immediately and stop it.

## Demo video

[![Watch the video](/doc/asset/forest-ai-screenshot.png)](https://www.youtube.com/watch?v=bcqdxG92-RM)

## How it Works

![portal](doc/asset/images/forest-ai-gif.gif)

## The architecture

![Forest AI architecture](/doc/asset/forest-ai-architecture.png)

1. The sensors deployed in forest monitor and pushes raw alert into DB when unsual audio detected
2. **Data server** passes this raw data to **ML-service** which classifies alerts as chainsaw or no chainsaw. Both of the services are hosted on IBM Cloud Foundry
3. If chainsaw detected then the alert is pushed into DB and Call/SMS alerts are generated using twillio API and sent to first responders
4. New alerts are also shown in **Forest Console** on a map, which is used to manage network of Forest sensor

## Project roadmap

![Roadmap](doc/asset/forest-ai-roadmap)

## Getting started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

## Live demo

You can find a running system to test at
[console.forestai.tech](http://console.forestai.tech/home)
[data-service.eu-gb.cf.appdomain.cloud](https://data-service.eu-gb.cf.appdomain.cloud)
[ml-server.eu-gb.cf.appdomain.cloud](https://ml-server.eu-gb.cf.appdomain.cloud)

## Built with

- [IBM Cloudant](https://cloud.ibm.com/catalog?search=cloudant#search_results) - The NoSQL database used
- [IBM Cloud Functions](https://cloud.ibm.com/catalog?search=cloud%20functions#search_results) - The compute platform for handing logic
- [IBM API Connect](https://cloud.ibm.com/catalog?search=api%20connect#search_results) - The web framework used
- [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
- [Maven](https://maven.apache.org/) - Dependency management
- [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

## Authors

- **Billie Thompson** - _Initial work_ - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/Code-and-Response/Project-Sample/graphs/contributors) who participated in this project.

## License

This project is licensed under the Apache 2 License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

- Based on [Billie Thompson's README template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2).
