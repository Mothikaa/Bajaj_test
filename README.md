# BFHL API — Node (Vercel)

## What this does
Serverless function that handles POST /bfhl and returns:
- is_success, user_id, email, roll_number
- odd_numbers, even_numbers (as strings)
- alphabets (uppercase)
- special_characters
- sum (as string)
- concat_string (reverse alphabetical characters with alternating caps)

## Run locally
```bash
npm i -g vercel
vercel dev
# POST http://localhost:3000/bfhl
```

## Deploy to Vercel
1. Push this folder to a GitHub repo.
2. Import the repo in Vercel.
3. In Vercel Project Settings → Environment Variables, set:
   - FULL_NAME = Mothikaa K
   - DOB_DDMMYYYY = 20042005  # example
   - EMAIL_ID = your_email@vitstudent.ac.in
   - ROLL_NUMBER = 22XXXXXXX
4. Deploy. Your endpoint will be:
   `https://<your-project>.vercel.app/bfhl`

## Test
```bash
curl -X POST https://<your-project>.vercel.app/bfhl   -H "Content-Type: application/json"   -d '{"data":["a","1","334","4","R","$"]}'
```
