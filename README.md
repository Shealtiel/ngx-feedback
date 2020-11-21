# ngx-feedback

> An angular directive for sending feedback featuring [Angular 11](https://angular.io/), [Html2canvas](https://html2canvas.hertzen.com/), [Angular Material](https://material.angular.io/), [Rxjs](https://rxjs-dev.firebaseapp.com/), inspired by Google send feedback, based on [angular-cli](https://cli.angular.io/).

## Prerequisites

- angular@11
- angular/material@11

### How to use it in your project

Install:

```bash
npm install https://github.com/shealtiel/ngx-feedback --save
```

Import:

```ts
import { FeedbackModule } from "ng-feedback";
```

Use:

```html
<button feedback>feedback</button>
```

### Properties

| Name             | Default Value                                                         |
| ---------------- | --------------------------------------------------------------------- |
| `title`          | Send feedback                                                         |
| `placeholder`    | Describe your issue or share your ideas                               |
| `editTip`        | Click to highlight or hide info                                       |
| `checkboxLabel`  | Include screenshot                                                    |
| `cancelLabel`    | CANCEL                                                                |
| `sendLabel`      | SEND                                                                  |
| `moveToolbarTip` | Move toolbar                                                          |
| `drawRectTip`    | Draw using yellow to highlight issues or black to hide sensitive info |
| `highlightTip`   | Highlight issues                                                      |
| `hideTip`        | Hide sensitive info                                                   |
| `editDoneLabel`  | DONE                                                                  |

Method `send(feedback)` is an output of the directive, the usage is:

```html
<button feedback (send)="onSend($event)">Feedback button</button>
```

Then you can custom the `onSend` method in your component.
The param `feedback` is an object contains two properties: `description` and `screenshot`.

- description is string to describe issues or ideas
- screenshot comes from `HTMLCanvasElement.toDataURL('image/png')`, can be used as src of an img tag

### Getting started with this repo

Clone/Download the repo then edit feedback library inside [`/src/app/feedback`](/src/app/feedback)

```bash
# clone repo
git clone https://github.com/Shealtiel/ngx-feedback.git

# change directory to our repo
cd ngx-feedback

# install the repo with npm
yarn

# start the server
yarn start

```

go to <http://localhost:4200> in your browser
