## Setup
* Clone the repo
* Install dependencies `mvn install`
* Update *.conf.json files inside the `src/test/resources/conf` directory with your [BrowserStack Username and Access Key](https://www.browserstack.com/accounts/settings). 

## Running your tests
* Upload your Native App (.ipa file) to BrowserStack servers using upload API:

  ```
  curl -u "username:accesskey" -X POST "https://api.browserstack.com/app-automate/upload" -F "file=@/path/to/app/file/Application-debug.ipa"
  ```

* If you do not have an .ipa file and looking to simply try App Automate, [you can download our sample app and upload](https://www.browserstack.com/app-automate/sample-apps/ios/BStackSampleApp.ipa)
to the BrowserStack servers using the above API.
* Update the desired capability "app" with the App URL returned from the above API call
* To run a single test, run `mvn test -P single`
* To run parallel tests, run `mvn test -P parallel`
* To run local tests, run `mvn test -P local`

## Notes
* You can view your test results on the [BrowserStack Automate dashboard](https://www.browserstack.com/automate)
* Refer [Get Started](https://www.browserstack.com/app-automate/get-started#getting-started-ios) document to configure the capabilities
* You can export the environment variables for the Username and Access Key of your BrowserStack account. 

  ```
  export BROWSERSTACK_USERNAME=<browserstack-username> &&
  export BROWSERSTACK_ACCESS_KEY=<browserstack-access-key>
  ```

## Addtional Resources
* [Getting Started with App Automate](https://www.browserstack.com/app-automate/get-started-ios)
