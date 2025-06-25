# -REST-API-CLIENT
*COMPANY*: CODETECH IT SOLUTIONS

*NAME*: K N VENKATA SAI SWARUP

*INTERN ID*: CT04DG3076

*DOMAIN*: JAVA PROGRAMMING

*DURATION*: 4 WEEKS

*MENTOR*: NEELA SANTHOSH KUMAR

**Reset API Client in Java is a software module or application that interacts with RESTful web services over HTTP to perform operations such as retrieving, updating, creating, or deleting resources. REST (Representational State Transfer) is an architectural style widely used for building scalable and stateless web services. A REST API client sends requests to a server and receives responses, typically in JSON or XML format.
Java provides various libraries and tools to build robust REST API clients. Some of the most commonly used libraries include HttpURLConnection, Apache HttpClient, OkHttp, and JAX-RS client (like Jersey). Among modern applications, developers often use the HttpClient introduced in Java 11 for its ease of use and efficiency.

Key Features of a REST API Client in Java
Request Construction:
The client constructs HTTP requests (GET, POST, PUT, DELETE) with appropriate headers, URL parameters, and request bodies. For instance, sending a GET request to retrieve user data or a POST request to submit a form.
Data Serialization/Deserialization:
JSON is the most popular format for data exchange. Libraries like Jackson or Gson are used to serialize Java objects to JSON and deserialize JSON responses into Java objects.
Error Handling:
REST clients must handle various HTTP status codes (e.g., 200 OK, 404 Not Found, 500 Internal Server Error) and manage exceptions such as connection timeouts or malformed responses.
Authentication:
Clients often need to authenticate using mechanisms such as API keys, Bearer tokens (OAuth), or Basic Authentication. Headers are set accordingly in the request.

Example Use Case
Consider a Java REST API client that connects to a weather API to fetch real-time weather data based on a city name. The client would:
Construct the request URL with query parameters (e.g., city name and API key).
Send an HTTP GET request.
Parse the JSON response to extract temperature, humidity, etc.
Display the data in a readable format.

Sample Workflow
Build URL:
java
Copy
Edit
String url = "https://api.weatherapi.com/v1/current.json?key=API_KEY&q=London";

Send GET Request:
java
Copy
Edit
HttpClient client = HttpClient.newHttpClient();
HttpRequest request = HttpRequest.newBuilder()
        .uri(URI.create(url))
        .GET()
        .build();
        
Handle Response:
java
Copy
Edit
HttpResponse<String> response = client.send(request, HttpResponse.BodyHandlers.ofString());
System.out.println(response.body());
Parse JSON:

java
Copy
Edit
ObjectMapper mapper = new ObjectMapper();
WeatherData data = mapper.readValue(response.body(), WeatherData.class);

Advantages of a REST API Client in Java
Cross-platform and portable: Java runs on any platform with the JVM.
Reliable and secure: Java supports HTTPS, authentication, and custom headers.
Extensible: Can be integrated with frameworks like Spring Boot for advanced features.
In conclusion, a REST API client in Java plays a crucial role in connecting applications with web services. With Java’s powerful libraries and clear syntax, developers can build efficient and scalable clients to consume APIs across various domains such as weather data, e-commerce, finance, and more.
**OUTPUT
---- Weather Data ----
Location: London, City of London, Greater London, United Kingdom
Temperature: 19.0°C
Condition: Partly cloudy

