
# Share API Polyfill

This is a (6kb) polyfill for the Web Share API that can be used in desktop too, so your users can share in their twitter, facebook, messenger, linkedin, sms, e-mail, print, telegram or whatsapp.

## Install

Just import it like in a head:

```html
  <head>
    ...
    <script src="https://unpkg.com/share-api-polyfill/dist/share-min.js"></script>
  </head>
```
or install

```bash
npm install share-api-polyfill
```

## Usage

Implement this function

```javascript
function share() {
        navigator
          .share(
            {
              title: 'Set title',
              text: 'Set body text',
              url: location.href,
              // Use this website for get Facebook id - https://findmyfbid.in/
              fbId: '1577700000000000',
              hashtags: 'hashtag1, hashtag2, hashtag3',
            },
            {
              // change this configurations to hide specific unnecessary icons
              copy: true,
              email: true,
              print: true,
              sms: true,
              messenger: true,
              facebook: true,
              whatsapp: true,
              twitter: true,
              linkedin: true,
              telegram: true,
              skype: true,
              language: 'pt', // specify the default language
            }
          )
          .then(_ => console.log('Yay, you shared it :)'))
          .catch(error =>
            console.log("Oh noh! You couldn't share it! :'(\n", error)
          )
      }
```
## Credit

[on2-dev](https://github.com/on2-dev/share-api-polyfill)

  