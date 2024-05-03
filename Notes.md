## Test driven development
- First the tests are written then code is written
## Linting
- Tool to check code formatting
- Highlights errors,typos and formatting issues
- Using flake8 package for that
- Run it through docker-compose.yml
- development dependency, not a project dependency
- docker-compose run --rm app sh -c "flake8"

## Testing
- Django test suite
- Run tests through docker-compose
- docker-compose run --rm app sh -c "python manage.py test"

## Start the project
-  docker-compose run --rm app sh -c "django-admin startproject app ."

## Bring the server
- docker-compose up

## Django Test Framework
- Built on top of unittest library
- Extra features: Test client- dummy web browser, simulate authentication, temporary db
- Django REST framework adds features: API test client
- We can use tests.py or test/* directory but not both

## SimpleTestCase
- Testcase class
- No db integration
- Useful if no db is required
- Save time 

## Testcase
- Database integration
- Useful for testing code that uses the db
- Relevant for this project

## Mocking
- Avoid relying on external services
- Can't gurantee that those would be available
- Using unittest.mock