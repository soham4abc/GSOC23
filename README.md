<h1 align="center">Google Summer of Code 2023 <img src="https://media2.giphy.com/media/KB8MHRUq55wjXVwWyl/source.gif" width="50"></h1>

<p align="center"><i>A full report on Google Summer of Code 2023 @ FOSSology</i></p>
<p align="center"><i>Project: "REST API improvements" </i> </p>

<p align="center">
        <img src="https://www.codecademy.com/resources/blog/wp-content/uploads/2022/12/What-Is-Pair-Programming--1.png" width="400">
</p>

![image](https://user-images.githubusercontent.com/66276301/188962690-5869b53c-99bb-4012-b13f-443832568f7e.png)

## Google Summer of Code 2023 Report: "REST API Improvements" 👨‍💻
<!-- 
![ViewCount](https://views.whatilearened.today/views/github/dushimsam/GSoC-2022.svg)
![GitHub](https://img.shields.io/github/followers/dushimsam?style=social)
![Twitter](https://img.shields.io/twitter/follow/dushimsam?style=social)
![GitHub Stars](https://img.shields.io/github/stars/dushimsam/GSoC-2022?style=social) -->

A brief introduction about myself 

I am **Soham Banerjee**, a Computer Science and engineering student at RCCIIT Kolkata. I have been a Full-Stack developer and have been working for many organisations since the past 3 years. Have been an open source software enthusiast since I was introduced to it in the 1st year of my college and, I am grateful to be a part of FOSSology under the Google Summer of Code program for 2023.  

In this article I am going to outline the details of my contributions as a reference of project completion during the entire duration of Google Summer of Code 2023.


# 🌏 CONTRIBUTIONS 

During this period I have mainly worked on two modules for the Fossology Project.

- **Enhancing existing endpoints:**  In this category we redefined old endpoints and enhanced them with more features.

- **Developing REST APIs:** We introduced many more features using API endpoints so that they can used in the UI or can be used as a service.

Let's have a deeper look into the processes and flows that were implemented in this Google Summer of Code!  
## Endpoint for OpenAPI docs

This particular endpoint provides the user with the openAPI documentation for the existing APIs as a response.

- Endpoint `/openapi` 

Response format of the API: <br/>
![openapi](/img/API/openapi.png)

### 👨‍💻 PR link - [feat(api): openapi.yaml exposed through API](https://github.com/fossology/fossology/pull/2474)

### File Copyright Info

This API endpoint would provide the user with the copyright information associated with a particular Item.
- Endpoint `/uploads/{UploadId}/item/{ItemId}/copyrights`

Response format of the API: <br/>
![copyright-info](/img/API/getcopyrights.png)


### 👨‍💻 PR link - [feat(api): copyright info for file](https://github.com/fossology/fossology/pull/2475)

## Delete File Copyright

This particular endpoint can be used to delete a particular endpoint for an Item. The endpoint takes in the hash of the copyright that needs to be deleted. 

- Endpoint `DELETE`  `/uploads/{UploadId}/item/{ItemId}/copyright/<Hash>`

Response format of the API: <br/>
![delete-copyright](/img/API/deletecopyright.png)

### 👨‍💻 PR link - [feat(api): Delete Copyright for a File](https://github.com/fossology/fossology/pull/2478)

## Update Copyright for a File

This particular endpoint can be used to update the already existing copyrights for a file. The API uses the hash of the copyright to update the endpoint.

- Endpoint `PUT` `/uploads/{UploadId}/item/{ItemId}/copyright/<Hash>`

The API response: <br/>
![update-copyright](/img/API/updatecopyright.png)

### 👨‍💻 PR link - [feat(api): API for updating File copyright content](https://github.com/fossology/fossology/pull/2479)

## Restore Copyright for a file

This particular endpoint can be used to restore a deleted copyright.

- Endpoint - `PATCH` `/uploads/{UploadId}/item/{ItemId}/copyright/<Hash>`

Current response of the API: <br/>
![restore_copyright](/img/API/restorecopyright.png)

### 👨‍💻 PR link - [feat(api): restore deleted copyrights](https://github.com/fossology/fossology/pull/2486)

## Fetching details of the inactive copyrights

Developed an API endpoint to return the details of the inactive copyrights from the server

- Endpoint - `uploads/{UploadId}/item/{ItemId}/copyrights/inactive`

Response of the API: <br/>
![inactive_copyrights](/img/API/getinactivecopyrights.png)

### 👨‍💻 PR link - [feat(api): get inactive copyright details for a file](https://github.com/fossology/fossology/pull/2485)

## API endpoint for file info

This particular endpoint provides us with the info of a particular file from the Fossology server.

- Endpoint `/uploads/{UploadId}/item/{ItemId}/info`

The API response: <br/>
![info_response](/img/API/fileinfo.png)

### 👨‍💻 PR link - [feat(api): File info API](https://github.com/fossology/fossology/pull/2496)

## Endpoint for total number of copyrights in a file 


This particular endpoint provides the total number of copyrights in a file. 

- Endpoint `/uploads/{UploadId}/item/{ItemId}/totalcopyrights`

The API response: <br/>
![total_number_copyrights](/img/API/totalnumberofcopyrights.png)
<br/>

### 👨‍💻 PR link - [feat(api): API to return total number of copyrights for a file](https://github.com/fossology/fossology/pull/2488)

## Endpoint to get conf info for an upload

Developed an endpoint that provides us with the conf info for a specific upload.
- Endpoint `/uploads/{UploadId}/item/{UploadId}/conf`

The API response: <br/>
![conf](/img/API/confInfo_new.png)
<br/>

### 👨‍💻 PR link - [feat(api): conf info for upload](https://github.com/fossology/fossology/pull/2505)

## Endpoint for fetching customise page data

Created an endpoint that sends the customise page data from the fossology server

- Endpoint `/customise`

API response:<br/>
![customise_reponse](/img/API/customise.png)

### 👨‍💻 PR link - [feat(api): Get Customise page data](https://github.com/fossology/fossology/pull/2520)

## Endpoint to get the banner message

This particular endpoint provides us with the banner message that is displayed in the old UI.

- Endpoint - `/customise/banner`

API response: 

![banner_reponse](/img/API/bannermsg.png)

### 👨‍💻 PR link - [feat(api): Get banner message](https://github.com/fossology/fossology/pull/2553)

## Endpoint to get the list of obligations

Developed an endpoint to get the list of all obligations from the server. This particular endpoint can be used to get the data for the dropdown.

- Endpoint `/obligations/list`

![obligations_list](/img/API/obligations_list.png)

### 👨‍💻 PR link - [feat(api): api to get the list of obligations](https://github.com/fossology/fossology/pull/2559)

## Endpoint to get details of a particular obligation

Developed an endpoint that provides us with the details of a particular obligation. The API takes in the id of the obligation as a parameter. 

- Endpoint `/obligations/{id}`

API response: 

![obligations_details](/img/API/obligations_details.png)

### 👨‍💻 PR link - [feat(api): get details of a particular obligation using id](https://github.com/fossology/fossology/pull/2564)

## Endpoint to get details of a all obligations

Developed an endpoint that provides user with all the obligations details from the backend server.  

- Endpoint `/obligations/`

API response: 

![all_obligations_details](/img/API/all_obligations_details.png)

### 👨‍💻 PR link - [feat(api): Get details of all obligations](https://github.com/fossology/fossology/pull/2565)

## Endpoint to Delete an Obligation

This particular endpoint can be used to delete an obligation from tghe server.   

- Endpoint `DELETE` `/obligations/{ObligationID}`

API response: 

![delete_obligation](/img/API/all_obligations_details.png)

### 👨‍💻 PR link - [feat(api): Get details of all obligations](https://github.com/fossology/fossology/pull/2565)


## Documentation:📄

During the GSoC period, I got the time to create and organize documentation for  the FOSSology [**REST-API**](https://github.com/fossology/fossology). The documentation contains all the user and developer information of the project and is organized in a way to be easily accessible by all.

The weekly documentation of updates can be found at [**FOSSology/gsoc**](https://fossology.github.io/gsoc/docs/2023/rest/updates/soham/2023-06-01)


<h1 align="center">👨🏻‍🏫 DELIVERABLES </h1>

| Tasks   | Planned | Completed     | Remarks    |
| :---:       |    :----:   |    :---:      |    :---:      |
| Adding all the high priority APIs   | Yes       | :heavy_check_mark: | All the APIs with High priority have been developed and delivered during the official coding period of the Google Summer of Code 2023|
| Enhanching existing APIs for additional functionality   | Yes        | :heavy_check_mark:  | APIs with limited functionality have been enhanced with the requirements and demands of the clients and users |
| Identifying and fixing some potential the existing bugs| Yes | :heavy_check_mark: | A lot of pre-existing bugs were sptted in the backend server. Some of them were fixed and for the rest of them issues have been made in the [Fossology repository](https://github.com/fossology/fossology) |
| Creating rest of the API endpoints for the medium and low priority functionalities | Yes | :heavy_check_mark: | A lot of new endpoints with completely new features were added and discussed with the mentors in order to enhance the functionality of the Fossology Server|
| Writing Test Cases for the existing and New API endpoints | Yes (WAS OPTIONAL) | :x: | Got the overview, still test cases needs to be implemented, especially for the newer endpoints.|

## Future enhancements:🚀

- Adding test cases for the existing REST-API endpoints so that reliablity of the back-end server can be ensured.
- Working on the new UI in order to continue the migration procedure of the fossology software.
- More testing and enhancement of the APIs upon discussion with the mentors. 

## Major Takeaways: 📚

- Developing REST API endpoints gave me an in depth overview of the entire process and flow of the Fossology software.
- Proper planning tecniques and discussion with the mentors and peers hepled in the smooth execution of the entire project.
- An excellent learning experience from the mentors while solving real life problems. 

## Links of work done: 🎯

### Pull Requests 🔗

- [FOSSology](https://github.com/fossology/fossology/pulls?q=is%3Apr+author%3Asoham4abc)

# Let's get connected!

- [LinkedIn](https://www.linkedin.com/in/soham-banerjee-6091831b3/)
- [GitHub](https://github.com/soham4abc)
- [Twitter](https://twitter.com/soham4abc)
 



