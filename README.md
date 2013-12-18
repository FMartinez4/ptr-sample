#Running concurrent protractor tests.

- Generated angular app using yeoman.

- Installed protractor & grunt-protractor-runner packages.

- Added protractor config & tests in test/scenario.

  1. Common config file: test/scenario/config/ptrConf.js
  2. Feature1 config file: test/scenario/conf/featureList1.js. Extends common config and adds list of specs to run.
  3. Tests are in test/scenario/feature1,feature2.

- Configured grunt to run protractor tests.

  1. protractor:feature1 runs specs from test/scenario/conf/featureList1.js
  2. protractor:feature2 runs specs from test/scenario/conf/featureList2.js
  3. concurrent:protractor runs protractor:feature1 & protractor:feature2 concurrently.

- Updated default build to start connect server & run concurrent:protractor   