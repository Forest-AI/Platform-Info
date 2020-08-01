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

![portal](doc/assets/images/forest-ai-gif.gif)

## The architecture

![Forest AI architecture](/doc/asset/forest-ai-architecture.png)

1. The sensors deployed in forest monitor and pushes raw alert into DB when unsual audio detected
2. **Data server** passes this raw data to **ML-service** which classifies alerts as chainsaw or no chainsaw. Both of the services are hosted on IBM Cloud Foundry
3. If chainsaw detected then the alert is pushed into DB and Call/SMS alerts are generated using twillio API and sent to first responders
4. New alerts are also shown in **Forest Console** on a map, which is used to manage network of Forest sensor

## Project roadmap

![Roadmap](roadmap.jpg)

## Getting started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```bash
dnf install wget
wget http://www.example.com/install.sh
bash install.sh
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be, for example

```bash
export TOKEN="fffd0923aa667c617a62f5A_fake_token754a2ad06cc9903543f1e85"
export EMAIL="jane@example.com"
dnf install npm
node samplefile.js
Server running at http://127.0.0.1:3000/
```

And repeat

```bash
curl localhost:3000
Thanks for looking at Code-and-Response!
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why, if you were using something like `mocha` for instance

```bash
npm install mocha --save-dev
vi test/test.js
./node_modules/mocha/bin/mocha
```

### And coding style tests

Explain what these tests test and why, if you chose `eslint` for example

```bash
npm install eslint --save-dev
npx eslint --init
npx eslint sample-file.js
```

## Live demo

You can find a running system to test at [callforcode.mybluemix.net](http://callforcode.mybluemix.net/)

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
