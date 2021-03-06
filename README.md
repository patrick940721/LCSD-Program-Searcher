# LCSD Program Searcher

## Introduction
I started this project for 2 reasons: 1. I want to learn front-end development while make something useful. 2. The official search page on LCSD's site is not so user friendly, and has very limited function (eg. I can't search multiple district in 1 go). So I decided to make one my own with the function that i need.  
These are some of the function I coded in the project that is not provided by the official website:
- Select multiple district, venue, activity type, days of week, time range
- Bookmark activities locally
- Generate calendar (.ics file) for download
- Mobile friendly responsive interface
- Map link that at least really direct you to a map
- Add to home screen (as progressive web app)

## Data Source
Fortunately the list of classes is available in JSON format, so I don't have to make this project another tedious web scraping project that breaks after even a very small UI change. The detail of the JSON file is available at [DATA.GOV.HK - Community Recreation and Sports Programmes](https://data.gov.hk/en-data/dataset/hk-lcsd-event-event-leisure).  
There is still one thing to complain, the json link returns the data without properly setting CORS flags for 3-party app access, so I need to use [cors-anywhere](https://cors-anywhere.herokuapp.com/) as a proxy. I didn't setup my own proxy server because I want to host this application using nothing more than gitlab page, but if you take this project and host it for more formal use, you better setup this proxy server your own, there should be a great performance gain in loading the data on startup. 

## To-Do
- improve performance
- share button
- precise location marker
  - Actually the location data (with latitude, longitude) available on DATA.GOV.HK, but they are scattered in different files.
- Generate .ics file of one event with recurrent rule instead of many events. 
- Doing all the above while maintaining performance.

---

## Project setup (generated by vue-cli)
```bash
npm install
```

### Compiles and hot-reloads for development
```bash
npm run serve
```

### Compiles and minifies for production
```bash
npm run build
```

### Lints and fixes files
```bash
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
