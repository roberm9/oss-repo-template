# Lab 10 Report - Database LAb - Michael Robertson - 8/1/2022    

###### Checkpoint 1:  
http://localhost:5984/ :  
![snip](https://user-images.githubusercontent.com/95317029/182267112-f662b22f-bb92-4d79-9a8d-12c213fc0f8f.PNG)  

###### Checkpoint 2:  
Tutorial steps 1.6.1 - 1.6.6:  
![2 1](https://user-images.githubusercontent.com/95317029/182272805-d9d4818f-32aa-4a8c-a45c-cdc0c59980a8.PNG)  
![2 2-3](https://user-images.githubusercontent.com/95317029/182272810-3e3fd8f9-cd66-4d63-ad28-1530657b677b.PNG)  
![2 verify](https://user-images.githubusercontent.com/95317029/182272812-d5edb9e0-62bb-464e-83f8-721ac9a47158.PNG)  
![2,4](https://user-images.githubusercontent.com/95317029/182272813-f1f1edab-a9a7-4512-8d3c-fc934f8bcaae.PNG)  
![2 5](https://user-images.githubusercontent.com/95317029/182272814-2754ab46-ade3-4137-ac95-51b6424dc534.PNG)  
![2 6](https://user-images.githubusercontent.com/95317029/182272815-1df838eb-65df-4bf9-8a14-0c363e7d3387.PNG)  

###### Checkpoint 3:  
![3 1](https://user-images.githubusercontent.com/95317029/182280956-ee454848-5688-4674-8c9f-013f36b932c0.PNG)  
![3 2](https://user-images.githubusercontent.com/95317029/182280957-6d7e45c2-291a-4ff3-87f4-bdd5260bb3f7.PNG)  
![3 3 0](https://user-images.githubusercontent.com/95317029/182280958-9da6ed97-d04a-4985-b2a4-5fc52c5215f8.PNG)  
![3 3 1](https://user-images.githubusercontent.com/95317029/182280960-7f27985a-1e04-4cdd-bd84-de3c55ec3560.PNG)  
![3 3 3](https://user-images.githubusercontent.com/95317029/182280962-2ee381cb-b61e-4315-8bbf-a75264b79a71.PNG)  
![3 3 5](https://user-images.githubusercontent.com/95317029/182280963-c48fe2d3-dbc6-4ce6-91d5-2c26550e67da.PNG)  

###### Checkpoint 4:  
curl -X POST admin:password@localhost:5984/hello-world/_find -d '{  
   "selector": {  
      "year": {  
         "$gt": 1987  
    }  
  }  
}' -H 'Content-Type: application/json'   
![4 1](https://user-images.githubusercontent.com/95317029/182281257-658ae466-4baa-452a-b5bd-ddc7bb6031cf.PNG)  

    
curl -X POST admin:password@localhost:5984/mango/_find -d '{  
   "selector": {  
      "title": {  
         "$eq": "L"  
    }  
  }  
}' -H 'Content-Type: application/json'  
  
curl -X POST admin:password@localhost:5984/hello-world/_index -d '{  
   "index": {  
      "fields": [  
         "year"  
      ]  
   },  
   "name": "year-json-index",  
   "type": "json"  
}' -H 'Content-Type: application/json'  
  
  
curl -X POST admin:password@localhost:5984/hello-world/_index -d '{  
   "index": {  
      "fields": [  
         "title"  
      ]  
   },  
   "name": "title-json-index",  
   "type": "json"  
}' -H 'Content-Type: application/json'  
  

![bl](https://user-images.githubusercontent.com/95317029/182281603-40c14254-4f63-41f7-ba57-03a8c1b8f13e.PNG)
