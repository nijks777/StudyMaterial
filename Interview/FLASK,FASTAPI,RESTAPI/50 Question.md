EASY (10 Questions)

What is Flask and why is it called a micro-framework?
What is the difference between Flask and Django?
What are the main HTTP methods (GET, POST, PUT, DELETE, PATCH) used in REST APIs?
What does REST stand for and what are RESTful web services?
What is FastAPI and what are its main advantages over Flask?
How do you create a simple "Hello World" application in Flask?
What is the purpose of @app.route() decorator in Flask?
What are HTTP status codes and why are they important in REST APIs?
What is the difference between synchronous and asynchronous programming?
What is the purpose of __name__ parameter in Flask(__name__)?


MEDIUM (25 Questions)

Scenario: You need to handle user authentication in your Flask API. How would you implement session management vs JWT tokens?
What is the difference between PUT and POST methods? When would you use each?
Explain dependency injection in FastAPI with a practical example.
What are Flask Blueprints and when would you use them in a large application?
How does FastAPI leverage Python type hints and Pydantic for request validation?
What is the difference between g object and session object in Flask?
Scenario: Your API receives 10,000 requests per minute. How would you implement rate limiting in Flask/FastAPI?
What is CORS (Cross-Origin Resource Sharing) and how do you handle it in Flask?
Explain the difference between async def and def route handlers in FastAPI. When should you use each?
What is idempotency in REST APIs? Which HTTP methods are idempotent?
How do you implement pagination in a REST API?
Scenario: You need to connect your Flask application to a PostgreSQL database. What steps would you take and which extensions would you use?
What is the purpose of middleware in Flask and FastAPI?
How does FastAPI automatically generate API documentation?
What are template engines in Flask? Explain Jinja2 templates.
Scenario: Your API needs to process large file uploads. How would you handle this efficiently in Flask or FastAPI?
What is the difference between application context and request context in Flask?
How do you implement OAuth2 authentication in FastAPI?
What are the key principles of REST architecture (statelessness, client-server, uniform interface, etc.)?
How would you implement API versioning in Flask? (e.g., /api/v1/, /api/v2/)
Scenario: You need to send emails from your Flask application. How would you implement this feature?
What is Flask-RESTful and how does it differ from using Flask directly?
Explain the use of background tasks in FastAPI.
What is the difference between Flask-SQLAlchemy and raw SQL queries?
How do you handle error handling and custom exceptions in FastAPI?


HARD (15 Questions)

Scenario: You're building a real-time chat application. Compare WebSocket implementation in Flask vs FastAPI and explain which you'd choose and why.
How would you design and implement a microservices architecture using Flask/FastAPI? What challenges would you face?
Explain the event loop and how async/await works in FastAPI. What are the performance implications of misusing async?
Scenario: Your REST API needs to handle transactions across multiple database operations. How would you ensure ACID properties and handle rollbacks?
How do you implement a plugin architecture in Flask for a large-scale application?
What is the N+1 query problem in REST APIs and how would you solve it?
Scenario: You need to optimize an API endpoint that takes 5 seconds to respond. Walk through your debugging and optimization process.
How would you implement a circuit breaker pattern for external API calls in your application?
Explain the differences between REST and GraphQL. When would you choose GraphQL over REST?
Scenario: You're deploying a Flask/FastAPI application to production. Explain your complete deployment strategy including WSGI/ASGI servers, reverse proxy, and scaling considerations.
How do you implement distributed caching (Redis) in a FastAPI application for high-performance APIs?
What are the security considerations for REST APIs? How do you protect against SQL injection, XSS, CSRF, and other vulnerabilities?
Scenario: Your API serves data from multiple sources (database, external APIs, cache). How would you implement a repository pattern or service layer?
How would you implement graceful degradation and retry logic for a REST API that depends on multiple external services?
Scenario: You need to implement a rate limiter that works across multiple instances of your API (distributed rate limiting). How would you design this system?