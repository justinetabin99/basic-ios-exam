# Task

Write a single-page app that displays a list of GitHub users.

# Minimum Specification

The app must perform the following tasks:

1. Display a list of users
> This can be retrieved from publicly available GitHub user account as initial screen.
2. Display and cache avatar image urls.
3. Use this [GET /users](https://api.github.com/users) endpoint.
4. Display the error message informing "Rate limit exceeded". 
> The API can be accessed without auth however, it requires error handling of rate limit.
```
$ curl -I https://api.github.com/users
> HTTP/1.1 200 OK
> Date: Mon, 01 Jul 2013 17:27:06 GMT
> Status: 200 OK
> X-RateLimit-Limit: 60
> X-RateLimit-Remaining: 56
> X-RateLimit-Reset: 1372700873
```
> If you exceed the rate limit, an error response returns:
```
> HTTP/1.1 403 Forbidden
> Date: Tue, 20 Aug 2013 14:50:41 GMT
> Status: 403 Forbidden
> X-RateLimit-Limit: 60
> X-RateLimit-Remaining: 0
> X-RateLimit-Reset: 1377013266

> {
>    "message": "API rate limit exceeded for xxx.xxx.xxx.xxx. (But here's the good news: Authenticated requests get a higher rate limit. Check out the documentation for more details.)",
>    "documentation_url": "https://docs.github.com/rest/overview/resources-in-the-rest-api#rate-limiting"
> }
```
5. Support for both portrait and landscape.

# Minimum Screen Specification
![](resources/example-screenshot.png)

# Additional Optional Specification
You may consider incorporating extra features or improved design. (e.g pull to refresh, avatar placeholders, persistence, unit tests, [pagination](https://docs.github.com/en/rest/reference/users#list-users), etc)

# Guidance for Code Quality 
### Modern Architecture
* Demonstrate your preferred architectural design patterns. (e.g MVC, MVVM, modular, testable, etc)

### Knowledge of Cocoa Touch
* Demonstrate high knowledge of UIKit. (e.g Storyboards, AutoLayout, ConstraintLayout, programmatically UIs, etc)

### Coding Standard
* Write high quality Swift code using standard best practice coding conventions. This includes naming methods and classes, using structs and classes as needed. (e.g. Raywenderlich Swift Style, Gitflow)

# Evaluation Criteria
Implementation of [Minimum Specification](#Minimum-Specification), clearly communicating decisions and best engineering practices (e.g complexity, refactorability and scalability). 

Examinee will also be hearing back the assessment of code's strengths, weaknesses.

# Requirements
* Latest Xcode
* Latest Swift / Storyboard UI
* Cocoapods or iOS / Cocoa Touch frameworks

# Submission
* Please configure the project/workspace to be able to run simply `CMD + R` or `Product > Run`
* Commit the directory containing the app and your README.md in master branch
* Send it back to your recruitment officer as an attachment in `tar` format
