[![angularfire-lite-illustration](https://cdn.rawgit.com/hamedbaatour/ffd1020004cd8adc14535cebc53fc442/raw/35f9112d318137595cbbcb5651d50e7e0fd3094a/ANGULAR%2520FIRE%2520ILLUSTARTION%25201.svg)](#)

<p align="center">
  <h1 align="center">AngularFire Lite</h1>
    <p align="center">lightweight wrapper to use Firebase API with Angular.</p>
</p>

[![Travis](https://img.shields.io/travis/hamedbaatour/angularfire-lite.svg)](https://travis-ci.org/hamedbaatour/angularfire-lite)
[![CircleCI](https://circleci.com/gh/hamedbaatour/angularfire-lite.svg?style=shield)](https://circleci.com/gh/hamedbaatour/angularfire-lite)
[![npm version](https://badge.fury.io/js/angularfire-lite.svg)](https://www.npmjs.com/package/angularfire-lite)
[![dependencies Status](https://david-dm.org/hamedbaatour/angularfire-lite/status.svg)](https://david-dm.org/hamedbaatour/angularfire-lite)
[![Greenkeeper](https://badges.greenkeeper.io/hamedbaatour/angularfire-lite.svg)](#)
[![GitHub issues](https://img.shields.io/github/issues/hamedbaatour/angularfire-lite.svg)](https://github.com/hamedbaatour/angularfire-lite/issues)
 [![Join the chat at https://gitter.im/angularfire-lite/Lobby](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/angularfire-lite/Lobby)


| Features              | AngularFire Light         | AngularFire2  |
| -------------         |:-------------:|         :-------------------:  |
| Authentication        | :heavy_check_mark:    | :heavy_check_mark:     |
| Firestore             | :heavy_check_mark:    |   :heavy_check_mark:   |
| Storage               | :heavy_check_mark:    |  :x:                   |
| Realtime Database     | :heavy_check_mark:    |  :heavy_check_mark:    |
| Server Side Rendering | :heavy_check_mark:    |  :x:                   |
| Size                  | :N/A:                 |  :N/A:                 |

<p></p>
<p align="center">
  <h2 align="center">Getting Started</h2>
</p>

[![angularfire-lite-step-1](https://cdn.rawgit.com/hamedbaatour/a500be30a8520653d7759dfd248b535f/raw/7d0facd6691beadad8f74d22d44e68e4edc373fb/step1%2520-%2520angularfire-lite.svg)](#)

<br>

**Reminder**: don't forget to install [nodejs](https://nodejs.org/en/) first.

```bash
 
npm install --save angularfire-lite firebase
 
```
<br>

[![angularfire-lite-step-2](https://cdn.rawgit.com/hamedbaatour/9b22511bf9c59cfe1aab595bfd528c5d/raw/9e08922b4aee17d61f32bdb5500fa11a335e93e0/step%25202.svg)](#)

<br>

**How?**: 
- Create a firebase account and login to your dashboard

- Click on 'Add Firebase to your web app' icon and copy the config object

- Add it to `environment.ts` & `environment.prod.ts` located under `/src/environments/`

```ts
export const environment = {
  production: false, // production: true => in `enviroment.prod.ts`
  config: {
    apiKey: '<your-key>',
    authDomain: '<your-project-authdomain>',
    databaseURL: '<your-database-URL>',
    projectId: '<your-project-id>',
    storageBucket: '<your-storage-bucket>',
    messagingSenderId: '<your-messaging-sender-id>'
  }
};
```
<br>

[![angularfire-lite-step-3](https://cdn.rawgit.com/hamedbaatour/3855327ef6c4f7d22133a693231d6186/raw/956f99f36d834e15898e7712064f4316787f4185/step%25203.svg)](#)


**How?**: 
- Import the config object we created from `enviroment.ts`

- Imoprt `AngularFireLite` and pass it the config object

```ts
import { AngularFireLite } from 'angularfire-lite';
import {environment} from '../environments/environment';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    AngularFireLite.forRoot(environment.config)
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }

```

<br>

[![angularfire-lite-api](https://cdn.rawgit.com/hamedbaatour/f8c9581ab250d47e841d49ae7690ef82/raw/2cc67b7b2d1c29adbcdf3b7ea32a2de44439056a/api.svg)](#)

- **Observable based**: Every function returns an Observable that you should subscribe to it to get back the data.

- **Learn One API**: AngularFire Lite has the same syntax of the native Firebase API plus some useful addtions.
