Tyler Hoang
# Answers

1. I would put my automated tests within a GitHub action that runs whenever the code is pushed. Although we SHOULD run the tests prior to pushing, to make it easier to solve issues prior to pushing and waiting for Github actions to set up its environment and run, it is more important that we have publicly viewable and automatically running tests on any pull requests, etc., that way we can see if the code is up to quality standards in a convenient place prior to merging.

2. No, it is better to use a unit test for this case. Unit tests are better for testing small, modular parts of code, such as an individual function, as we can simply call this function, give its inputs, and verify the outputs, rather than going through the hassle of setting up a whole Puppeteer/other E2E setup for handling a function test.

3. Navigation mode will analyze a page after it loads, and provide performance metrics based on that. We use it to figure out how long pages take to load, and navigation performance. However, snapshot mode will provide analytics pertaining to a page at a particular moment of time, useful for assessing accessibility.

4. Based on the Lighthouse results on navigation mode on page load, we can properly size images (size them down) in order to decrease load times, serve images as WebP or AVIF files which offer better compression, further decreasing load times, and we can add a `<meta name = "viewport">` tag to optimize the app for mobile screen sizes & decrease input delays.