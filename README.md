# Load Testing

# Project Description
     I have performed performance testing on multiple api's from restful-booker.herokuapp.com with 6500 threads
     by applying api chaining and also using data from csv file

# Walk-through
      1.Used api from https://restful-booker.herokuapp.com/ and information about api is in API Testing.pdf file
      2.Defined variables which includes env variable to select environment
![1](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/ca3a6e84-34bb-4c83-aeda-6798b1e6ed15)

       accroding to env value slected environment and gave initial values to variables for create http request
![2](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/85c1ac26-548b-4ef0-a2e5-f6842956d00a)

      3.project has 4 HTTP requests
![1](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/ca3a6e84-34bb-4c83-aeda-6798b1e6ed15)

      4.HTTP requests create(POST)
        Taken data from defined variables in body data of create http request
![5](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/48da98ab-2dd3-45ee-88fe-3a2bb006e448)

        JSON Extractor captures booking id as id from response
![6](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/f4467005-1499-45db-995a-59d57a34b593)

        Response data

![7](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/f83e77ef-8561-4f0b-a268-a4e894728361)
          
      5.HTTP requests get(GET)
         Sample result from get http request
![8](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/364361c3-592d-4db7-92eb-7ca6bf27930f)

      6.HTTP requests auth(POST)
         generated token and captured as variable token for update HTTP requests
![9](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/004fb20c-4ef5-4498-941f-48b3ad561dd1)

      7.HTTP requests update(PUT)
         Used csv data from data1.csv and initialized in CSV Data Set Config file and used token value
         for authorization 

![4](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/a076fdc8-d20a-4e19-a94c-17605bc761b6)
![3](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/b093dfa9-b15e-49e5-8778-43a5abe1b734)
![10](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/92eca405-9f68-444b-8083-e1ce58830af6)

      8.Result in GUI mode with 6500 threads
![10 5](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/5e229f76-466d-4994-a0b5-94a08897398c)
![11](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/95ad9a2b-a3a3-424f-9a25-d309b0cc380c)


      9.Code to run in non GUI mode

        jmeter -n -t project_t6500.jmx -l report\project_t6500.jtl
        jmeter -g report\project_t6500.jtl -o report\project_t6500.jtl.html

      10.Result in non GUI mode
![12](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/57bda4d0-faa9-4eec-8d3a-12d7dd4a2458)
![13](https://github.com/nahidanik97/jmeter-performance-test-project-on-multiple-restful-booker.herokuapp.com-api-s/assets/157117314/7258e4db-4ed9-4e02-8336-1b650941700b)
