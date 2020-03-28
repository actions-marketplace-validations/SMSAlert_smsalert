# SMS Alert GitHub Action

Send an SMS from GitHub Actions.

## Prerequisites

- A SMSAlert Account. [Sign up for free](https://www.smsalert.co.in)

## Usage

1. Set up your credentials as secrets in your repository settings using `senderid`, `SMSALERT_USERNAME`, `SMSALERT_PASSWORD`

2. Add the following to your workflow

```yml
- name: 'Sending SMS Notification'
      uses: brijkishor7828/smsalert@master
      env:
        SMSALERT_USERNAME: ${{ secrets.SMSALERT_USERNAME }}
        SMSALERT_PASSWORD: ${{ secrets.SMSALERT_PASSWORD }}
      with:
        senderid: ${{ secrets.senderid }}
        toPhoneNumber: ${{ secrets.MY_PHONE_NUMBER }}
        message: "New push on ${{ github.repository }} from ${{ github.actor }}"
    ```

## Inputs

### `senderid`

**Required** senderid in your SMSAlert account to send the SMS from

### `toPhoneNumber`

**Required** Phone number to send the SMS to

### `message`

**Required** The message you want to send

### `SMSALERT_USERNAME`

A SMSAlert Username. Can alternatively be stored in environment

### `SMSALERT_PASSWORD`

A SMSAlert Password. Can alternatively be stored in environment

## Outputs

## Contributing

## Third Party Licenses

This GitHub Action uses a couple of Node.js modules to work.

License and other copyright information for each module are included in the release branch of each action version under `node_modules/{module}`.

More information for each package can be found at `https://www.npmjs.com/package/{package}`
