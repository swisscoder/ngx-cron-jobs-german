[![Build Status](https://travis-ci.org/rvalenciano/ngx-cron-jobs.svg?branch=master)](https://travis-ci.org/rvalenciano/ngx-cron-jobs) [![Maintainability](https://api.codeclimate.com/v1/badges/dc6b973320992074a560/maintainability)](https://codeclimate.com/github/rvalenciano/ngx-cron-jobs/maintainability) [![Test Coverage](https://api.codeclimate.com/v1/badges/dc6b973320992074a560/test_coverage)](https://codeclimate.com/github/rvalenciano/ngx-cron-jobs/test_coverage)

# ngx-cron-jobs

Angular > 2 version of angular-cron-jobs (http://angular-cron-jobs.github.io/angular-cron-jobs)

## Installation

To install this library, run:

```bash
$ npm install ngx-cron-jobs --save
```

```bash
$ yarn add ngx-cron-jobs
```

## Consuming your library


and then from your Angular `AppModule`:

```typescript
import { CronJobsModule } from 'ngx-cron-jobs';

@NgModule({
  imports: [
    ...,
    CronJobsModule,
    ...
  ]
})
export class AppModule { }
```

Once your library is imported, you can use its components, directives and pipes in your Angular application:

```xml
<!-- To insert to in your component minimal config with ngModel -->
<cron-jobs [(ngModel)]="hero.frequency"></cron-jobs>

<!-- To insert to in your component minimal config with reactive forms -->
<cron-jobs [formControl]="freqControl"></cron-jobs>

<!-- To insert to in your component minimal config with reactive forms -->
<!-- additional parameters -->
<cron-jobs [formControl]="freqControl" [config]="cronConfig"  [validate]="cronValidate"></cron-jobs>
```

## Configuration:

The component takes an input of `[config]` and `[validate]`

### Options
Plugin maybe configured by config object to which should be pass in `[config]` input.

List of options:

Option | Type | Description
-------|------|------------
quartz | boolean (false)| Use quartz syntax rather then cron syntax in control output
multiple | boolean (false)| Enable multi select in plugin selects
bootstrap | boolean (true) | Use bootstrap 4 html and css classes to build plugin forms 
option | object | Additional options
option.minute | boolean (true) | remove (false) or add minute to plugin select to control user ability to set cron expression.
option.hour | boolean (true) | remove (false) or add hour to plugin select to control user ability to set cron expression.
option.day | boolean (true) | remove (false) or add day to plugin select to control user ability to set cron expression.
option.week | boolean (true) | remove (false) or add week to plugin select to control user ability to set cron expression.
option.month | boolean (true) | remove (false) or add month to plugin select to control user ability to set cron expression.
option.year | boolean (true) | remove (false) or add year to plugin select to control user ability to set cron expression.

Additional to this plugin supports validation config (`[validate]` input):

Option | Type | Description
-------|------|------------
validate | boolean (false)| Add validation classes if controls are invalid.

## License

MIT © [Daniel 'yp2' Derezinski](https://github.com/yp2)

## Contributors

From angular 1 project

[@wowo](https://github.com/wowo)

[@immertreu](https://github.com/immertreu)

[@TSteele27](https://github.com/TSteele27)

[@DmitryEfimenki](https://github.com/DmitryEfimenko)

From angular2-cron-jobs project

[@rvalenciano](https://github.com/rvalenciano)

From ngx-cron-jobs project

[Daniel 'yp2' Derezinski](https://github.com/yp2)
