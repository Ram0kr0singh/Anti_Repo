create a basic express with typescript app.
make sure to following rules.
1. we have to keep separate modules in src/app/<modules>
2. each modules will have own routes.
3. <module>.route.ts
 /dto
<methods>/<entity>.dto.ts

<method>.centroller.ts
<method>.service.ts
<method>.model.ts

there will be folders in src
app.config.constant,database,logger.middleware,utils, types
and it will have app.ts and server.ts as starting file.

4. Follow the functional programming for creating controllers and services.

5. use winston for logger for all the logging purpose. Do not use console.log

6. Create response classes like ApiResponse class. keep it in utils folder.

7. Create error classes and these error will thrown at required places.keep in utils
folder.

8. Create custom express handlers and keep it in middleware folder.

9. Create a async wrapper.ts file in utils folder. and it in 

10. use Zod for dto validation.

11. use JMT for authentication and authorization.

12. env will be extracted in config/env/config.ts

13. store the required types in src/types folder

14. Don't use separate env file for separate environment like dev, staging , production

15. create zod  validation middleware to be used for validating schema.

16. Setup db to connect with supabase.(Postgress)

17. use Drizzle orm with drizzle-kit for migration.

18. API response conventions:
 success:true,
  statusCode:200,
   message:"User logged in successfully",
   data:{
    
   }

Error:
{
    success:false,
    statusCode:400,
    message:"Invalid email or password",
    error:[

    ],

}

19. healthcheck for api's 

20. this application doesn't contain any test suites.

21. setup these middlewares:
cors
helmet
compression
express-rate-limit