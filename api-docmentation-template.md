# Introduction

### Welcome to Work order management 👋 

Our APIs provide the capabilities to efficiently manage both provider and deliver service work orders

The difference between provider and deliver service work orders ? delivery service work orders are the physical order items (like parcels, trucks, etc.,) and provider service work orders handles the service request like (kitchen installation)

![img_7.png](img_7.png)


# Getting started

We offer both synchronous (REST) and asynchronous APIS. You can interact with both APIs using GitHub CLI, curl, the official Octokit libraries, and third party libraries. Occasionally, a feature may be supported on one API but not the other.

You should use the API that best aligns with your needs and that you are most comfortable using. You don't need to exclusively use one API over the other. Node IDs let you move between the REST API and GraphQL API. For more information, see "Using global node IDs."

This article discusses the benefits of each API. For more information about the GraphQL API, see "About the GraphQL API." For more information about the REST API, see the REST documentation.

How can you use our APIs ?

![img_3.png](img_3.png)

Let's start with the business object model. The main business object is the work order which contains packages and usually has items.

The shipment has a reference and contains, among other things, information about the shipper, recipient, shipping date, terms of delivery, carrier, and service.


# Authentication

The work order API uses API keys to authenticate requests. You can view and manage your API keys in the work order Dashboard.

Test mode secret keys have the prefix sk_test_ and live mode secret keys have the prefix sk_live_. Alternatively, you can use restricted API keys for granular permissions.

Your API keys carry many privileges, so be sure to keep them secure! Do not share your secret API keys in publicly accessible areas such as GitHub, client-side code, and so forth.

Authentication to the API is performed via HTTP Basic Auth. Provide your API key as the basic auth username value. You do not need to provide a password.

If you need to authenticate via bearer auth (e.g., for a cross-origin request), use -H "Authorization: Bearer sk_test_4eC39HqLyjWDarjtT1zdp7dc" instead of -u sk_test_4eC39HqLyjWDarjtT1zdp7dc.

All API requests must be made over HTTPS. Calls made over plain HTTP will fail. API requests without authentication will also fail.

Related video: Authentication.

```bash
curl https://api.stripe.com/v1/customers \
  -u sk_test_4eC39HqLyjWDarjtT1zdp7dc:
# The colon prevents curl from asking for a password.
```
<blockquote>
API KEY

A sample test API key is included in all the examples here, so you can test any example right away. Do not submit any personally identifiable information in requests made with this key.

To test requests using your account, replace the sample API key with your actual API key or sign in.
</blockquote>

# Delivery service
<details>
    <summary>Parcel</summary>
        <p>The team worked closely with us to define our requirements, delivering the project over agreed phases to time and on budget</p>
    <blockquote><h4>Business object model</h4></blockquote>
        <p>The team worked closely with us to define our requirements, delivering the project over agreed phases to time and on budget</p>
        <img src="./img_10.png" width="30%" alt="Social Icons">
    <blockquote><h4>End points</h4></blockquote>
        <details>
            <summary>Retrieve a parcel</summary>
            <blockquote><blockquote>GET /api/v2/parcels</blockquote> 
            <p> This endpoint allows you to retrieve a list of all the parcels which you have created or imported into your account under your API credentials. You can filter the results based on the query parameters provided below, in order to retrieve a specific parcel or list of parcels which match the defined criteria.
            <blockquote>Request sample: Shell or cURL</blockquote>
            <code style="display:block; white-space:pre-wrap">curl --request GET 
             --url https://ingka.ikea.com/api/v2/parcels
             --header 'Accept: application/json' 
             --header 'Authorization: Basic undefined'
            </code>
            </blockquote>
        </details>
        <details>
            <summary>Create a new parcel</summary>
            <p>GET /workorder</p>
        </details>
    <blockquote><h4>Code snippets</h4></blockquote>
    <blockquote><h4>Sample responses</h4></blockquote>
    <blockquote><h4>Schemas</h4></blockquote>
</details>

<details>
    <summary>Truck</summary>
        <p>The team worked closely with us to define our requirements, delivering the project over agreed phases to time and on budget</p>
    <blockquote><h3>Business object model</h3></blockquote>
        <p>The team worked closely with us to define our requirements, delivering the project over agreed phases to time and on budget</p>
        <img src="./img_10.png" width="30%" alt="Social Icons">
    <blockquote><h3>End points</h3></blockquote>
        <details>
            <summary>Retrieve a parcel</summary>
            <p>GET /workorder</p>
        </details>
        <details>
            <summary>Create a new parcel</summary>
            <p>GET /workorder</p>
        </details>
    <blockquote><h3>Code snippets</h3></blockquote>
    <blockquote><h3>Sample responses</h3></blockquote>
    <blockquote><h3>Schemas</h3></blockquote>
</details>

# Provider service
<details>
    <summary>Installation</summary>
        <p>The team worked closely with us to define our requirements, delivering the project over agreed phases to time and on budget</p>
    <blockquote><h3>Business object model</h3></blockquote>
        <p>The team worked closely with us to define our requirements, delivering the project over agreed phases to time and on budget</p>
        <img src="./img_10.png" width="30%" alt="Social Icons">
    <blockquote><h3>End points</h3></blockquote>
        <details>
            <summary>Retrieve a parcel</summary>
            <p>GET /workorder</p>
        </details>
        <details>
            <summary>Create a new parcel</summary>
            <p>GET /workorder</p>
        </details>
    <blockquote><h3>Code snippets</h3></blockquote>
    <blockquote><h3>Sample responses</h3></blockquote>
    <blockquote><h3>Schemas</h3></blockquote>
</details>

<details>
    <summary>Kitchen</summary>
        <p>The team worked closely with us to define our requirements, delivering the project over agreed phases to time and on budget</p>
    <blockquote><h3>Business object model</h3></blockquote>
        <p>The team worked closely with us to define our requirements, delivering the project over agreed phases to time and on budget</p>
        <img src="./img_10.png" width="30%" alt="Social Icons">
    <blockquote><h3>End points</h3></blockquote>
        <details>
            <summary>Retrieve a parcel</summary>
            <p>GET /workorder</p>
        </details>
        <details>
            <summary>Create a new parcel</summary>
            <p>GET /workorder</p>
        </details>
    <blockquote><h3>Code snippets</h3></blockquote>
    <blockquote><h3>Sample responses</h3></blockquote>
    <blockquote><h3>Schemas</h3></blockquote>
</details>