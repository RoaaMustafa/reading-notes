# Read: 12 - Docs for the HTML <canvas> Element & Chart.js
  #### Creating a Chart
  It's easy to get started with Chart.js. All that's required is the script included in your page along with a single `<canvas>` node to render the chart.
  ####  after cloning the Chart.js repo to a local directory, and navigating to that directory in the command line, 
  we can run the following: `> npm install` This will install the local development dependencies for Chart.js.
  
 ```
 > npm run build             // build dist files in ./dist
> npm run autobuild         // build and watch for source changes
> npm run dev               // run tests and watch for source and test changes
> npm run lint              // perform code linting (ESLint, tsc)
> npm test                  // perform code linting and run unit tests with coverage
```
  
  
#### You can create a new image-based test by following the steps below:

1. Create a JS file or JSON file that defines chart config and generation options.
2. Add this file in `test/fixtures/{spec.name}/{feature-name}.json.`
3. Add a describe line to the beginning of `test/specs/{spec.name}.tests.js` if it doesn't exist yet.
4. Run npm run dev.
5. Click the `"Debug"` button `(top/right)`: a test should fail with the associated canvas visible.
6. Right click on the chart and "Save image as...`" test/fixtures/{spec.name}/{feature-name}.png` making sure not to activate the tooltip or any hover functionality
7. Refresh the browser page `(CTRL+R)`: test should now pass
8. Verify test relevancy by changing the feature values slightly in the JSON file.




