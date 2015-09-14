# Raml
#%RAML 0.8
 
title: Get Meaning of Word
baseUri: http://dictionary.com/meaning

/meaning:
  post:
    description: adds a placement
    body:
      application/json:
        example: |
          {
            "meaning": {
              "word": "hello",
              "initialLetter": "h",
              "noOfLetters": 5
            }
          }
    responses:
      200:
        description: example response
        body:
          application/json:
            example: |
              {
                  "word":"hello",
                  "meaning":" a greeting"
              }
      400 :
        body:          
          application/json:
            example: |
                 { 
                  "message": "word not avaliable"
                  }  
      500 :
        body:
          application/json:
            example: |
                { 
                  "message": "Internal server issue"
                }
