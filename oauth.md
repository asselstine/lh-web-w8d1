# Open Authorization (OAuth)

## Introduction

The Open Authentication, or OAuth, protocol allows web services to share user authentication and information.

By sharing the user authentication procedure websites can simply re-use accounts from another service to identify the users, making their life easier because they don't have to remember two accounts.

As part of the sign in process the user can optionally allow the site access to personal information from the OAuth provider.  This means less time spent filling in their background information or choosing their profile picture.

## History

### Open Authentication 1.0

[Wikipedia](https://en.wikipedia.org/wiki/OAuth)

### Open Authentication 2.0

OAuth 2.0 was developed to address some of the shortcomings of the original protocol.  It was designed to allow for non-web based authentication, more security features, among other things.

There is some interesting history behind the development of OAuth 2 and the resignation one of its creators, Eran Hammer.  To know more check out:

[His blog post regarding his resignation](http://hueniverse.com/2012/07/26/oauth-2-0-and-the-road-to-hell/)

[His video explanation](https://vimeo.com/52882780)

## The Open Authentication protocol (v2)

An excellent introduction is available [here](https://aaronparecki.com/articles/2012/07/29/1/oauth2-simplified)

The following is an overview of the different steps in the OAuth process.  There are three roles in this scenario:

1. A provider.  A web server that implements the OAuth 2 server protocol.
1. A user.  Whoever is trying to access the service.
2. A third-party application.  A web application or app that implements the OAuth 2 client protocol and wants to use the provider API on behalf of the user.

It shows how an application can:

- authenticate a user
- access that user's information

#### The Protocol

1. The application is registered as an OAuth client with the provider.  The application provides information such as a title, logo, description, and includes the OAuth callback URLs.  The provider generates an id and secret key for the application.

2. The user requests access to the application and are redirected to the provider's login page.

3. After the user enters their credentials, the provider redirects the them to the application's callback URL including their user identification code and a request token.

4. The application requests an access token from the provider using the request token and the application's secret key.

5. The provider authorizes the application to a limited subset of the user's information and the API.

6. The service can use the access token to make API requests for that user's information.

## Usage

Let's use the DropBox API.
