# Number Classification API

A FastAPI-based API that analyzes numbers and returns their mathematical properties along with fun facts.

## Project Structure

number-classification-api/
├── main.py
├── README.md
└── requirements.txt

## Features

- Determines if a number is prime
- Checks if a number is perfect
- Identifies Armstrong numbers
- Calculates digit sum
- Provides various number properties (odd/even, perfect square, etc.)
- Generates fun facts about the number
- CORS enabled for cross-origin requests
- Error handling for invalid inputs

## API Specification

### Endpoint

```
GET /api/classify-number?number={number}
```

### Success Response (200 OK)

```json
{
    "number": 371,
    "is_prime": false,
    "is_perfect": false,
    "properties": ["armstrong", "odd"],
    "digit_sum": 11,
    "fun_fact": "371 is an Armstrong number because 3^3 + 7^3 + 1^3 = 371"
}
```

### Error Response (400 Bad Request)

```json
{
    "number": "invalid_input",
    "error": true
}
```

## Setup and Installation

1. Clone the repository:
```bash
git clone https://github.com/mabirhire1/number-classification-api.git
cd number-classification-api
```

2. Create a virtual environment and activate it:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install fastapi uvicorn
```

4. Run the application:
```bash
uvicorn main:app --reload
```

The API will be available at `http://localhost:8000`

## Dependencies

- Python 3.8+
- FastAPI
- Uvicorn
- Requests

## Testing the API

You can test the API using curl:

```bash
curl "http://localhost:8000/api/classify-number?number=371"
```

Or visit the interactive API documentation at:
```
http://localhost:8000/docs
```

## Deployment

This API can be deployed to any platform that supports Python applications. Some popular options include:

- AWS
- DigitalOcean
- Heroku
- Google Cloud Platform

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

MIT License