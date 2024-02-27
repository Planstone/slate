# Authentication

> To authenticate, use http basic authentication:

```shell
export USERNAME="your_api_token" 
export PASSWORD="" # blank on purpose
curl -u $USERNAME:$PASSWORD https://apps.planion.com/feed/v1/sessions
```

> Make sure to replace `your_api_token` with your API key from Planstone.

Planstone Events uses API keys to allow access to the API. Please contact support@planstone.com (or your Account Manager) for an API key.

Planstone expects for the API key to be included in all API requests to the server in a header that looks like the following:

`authorization: Basic NadfWQwZDliZjkddtYzYwNi00MalsdkfjGMwLWIyNWMtOTNlZWZhddNjBld2ddZDg==`

<aside class="notice">
You must replace <code>your_api_token</code> with your personal API key.
</aside>
