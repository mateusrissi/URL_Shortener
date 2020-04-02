# URL Shortener
This is a backend for a URL Shortener (a service that takes any URL and generates a shorter, more readable version) application made with Django and GraphQL.


## Examples

##### Query all URLs
    query {
        urls {
            id
            fullUrl
            urlHash
            clicks
            createdAt
        }
    }

##### Adding a URL to the database
    mutation {
        createUrl(fullUrl:"https://www.linkedin.com/in/mateusrissi/") {
            url {
                id
                fullUrl
                urlHash
                clicks
                createdAt
            }
        }
    }

##### Querying URLs but with a filter
    query {
        urls(url:"linkedin") {
            id
            fullUrl
            urlHash
            clicks
            createdAt
        }
    }

##### Querying URLs but with pagination
    query {
        urls(first: null, skip: null) {
            id
            fullUrl
            urlHash
            clicks
            createdAt
        }
    }




## Many thanks to Jonatas Baldin
He is the creator of the tutorial [How To Create a URL Shortener with Django and GraphQL](https://www.digitalocean.com/community/tutorials/how-to-create-a-url-shortener-with-django-and-graphql)
