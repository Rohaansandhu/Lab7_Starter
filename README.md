## 1.

Automated tests should be put into a Github action so that it can be on a standardized and consistently testable environment. By having the tests run in a Github action, we can ensure that no code is merged before having passing tests. You should also manually run them before pushing code, but you definitely need the Github action tests for consistency with environments and between developers.

## 2.

No, for an individual function you would only need a unit test to ensure that when given correct inputs it gives the correct output (or given bad inputs it fails appropriately). End to end tests should involve multiple functions working in tandem.

## 3.

Navigation mode loads the page from scratch and measures how fast it loads, things like paint times and time to interactive. Snapshot mode just looks at the page as it currently is, so it's better for catching accessibility issues but can't tell you anything about load performance.

## 4.

First, the html element is missing a lang attribute, which the accessibility audit flagged. Screen readers use that to know what language to read the page in, so it's an easy fix that directly helps users. Second, there's no meta description, which is why the SEO score docked points. Adding one helps search engines summarize the page in results. Third, the CSS stylesheet is flagged as render-blocking, meaning it delays the first paint. Inlining critical styles or deferring the stylesheet would help shave off some load time. Also, most important than anything i've said so far, the images don't load (didn't really need lighthouse to show me this).


