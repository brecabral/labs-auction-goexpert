# Usage

Run Docker Compose in the root folder:
```sh
docker compose up
```

Create an auction:
```sh
curl -X POST http://localhost:8080/auction \
  -H "Content-Type: application/json" \
  -d '{
    "product_name": "teste",
    "category": "teste",
    "description": "testetesteteste",
    "condition": 0
  }'
```

Verify the auction at:  
http://localhost:8080/auction?status=0

After the `AUCTION_INTERVAL` environment variable time, the status should change to 1, indicating that the auction has been completed.
