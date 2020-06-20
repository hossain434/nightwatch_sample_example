# Steps to create Nightwatch project:
1.	Create workspace folder mkdir nightwatchproject, cd nightwatchproject
2.	Create package.json: npm init -y
3.	Include below dependencies in package.json
  "devDependencies": {
    "nightwatch": "^1.3.6",
    "chromedriver": "^83.0.0"
  }
4.	In package.json, update script as
“scripts”: {
  “test”: “nightwatch”
}

5.	Please note that if we run npm test  now it will spit out an error since Nightwatch requires nightwatch.json or nightwatch.conf.json.
6.	Here we have test folder directory ( i.e tests, the name can be anything ), webdriver properties ( like path, port etc.), and desired capabilities with a default value.
{
  "src_folders": ["tests"],
  "webdriver": {
    "start_process": true,
    "server_path": "./node_modules/chromedriver/lib/chromedriver/chromedriver.exe",
    "port": 9515,
    "cli_args": ["--port=9515"]
  },
  "test_settings": {
    "default": {
      "desiredCapabilities": {
        "browserName": "chrome"
      }
    }
  }
}
7.	Let’s create tests folder inside the project since Nightwatch will look for that folder. And we need to add a basic test inside this folder. I will name it basicTests.js If everything went smooth running npm test will open a chrome browser and close it down since our test does not do anything yet.
8.	Reference: https://www.swtestacademy.com/introduction-to-nighwatch-js/

