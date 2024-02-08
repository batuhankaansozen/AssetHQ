<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->

<a name="readme-top"></a>

<br />
<div align="center">
  
<br/>
  <h2 align="center">AssetHQ Documentation
</h2>

</div>
<br/>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#how-to-install">How to Install</a>
    </li>
    <li><a href="#api-reference">Api Reference</a></li>
    <li><a href="#screenshots">Screenshots</a></li>
    <li><a href="#technologies-used">Technologies Used</a></li>
  </ol>
</details>

<!-- GETTING STARTED -->

## How to Install
AssetHQ is a part of the cms port.backend project, so when the port.backend is up and running AssetHQ will automatically runs.

#### Run Port.Backend on dev environment.

```bash
  nvm use 14
  npm i
  add "development.yaml" to config folder
  npm run develop
```
    
#### Run Port.Backend on production environment.

```bash
  rename "development.yaml" into "production.yaml"
  create "secrets.yaml" with social sharing secrets
  npm run build
```
<p align="right">(<a href="#readme-top">back to top</a>)</p>

## API Reference

### Prefix: assets

```http
  POST /
```
this will go the handler "save" in the code to save an asset into AssetHQ

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |

#### GET Upload Url 

```http
  GET /uploadurl
```
Gets an pre-signed url for uploading new asset

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |

#### Create Upload Url 

```http
  POST /uploadurl
```
Gets an pre-signed url for uploading new asset

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |


#### Multipart uploading 

```http
  POST /multipartuploadurl
```
Gets an pre-signed urls for uploading a large asset

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |


#### Complete Multipart

```http
  POST /completemultipart
```
complete a multipart upload


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |


#### Search

```http
  POST /search
```
Search assets


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |


#### Search Scroll

```http
  POST /search/scroll
```
Get next page of given scroll id


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |

#### Search Raw

```http
  POST /search/raw
```
Raw query to ES


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |

#### Download Url

```http
  GET /:assetId/downloadurl
```
Temporary URL for asset download


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |

#### Master ID

```http
  GET /masterid/:masterId
```
Asset detail


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |

#### Get Asset Details

```http
  GET /:assetId
```
Gets asset details for given id


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |

#### Update Assets

```http
  PATCH /:assetId
```
Update asset


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |

#### Delete Assets

```http
  DELETE /:assetId
```
Delete asset


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `string` | **Required**. when user is authenticated |

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Screenshots

![App Screenshot](https://i.ibb.co/x1ttYkw/Screenshot-2024-01-29-at-16-54-16.png)


![App Screenshot](https://i.ibb.co/9wd9jgP/Screenshot-2024-01-29-at-16-55-03.png)


![App Screenshot](https://i.ibb.co/Rpbh6pX/Screenshot-2024-01-29-at-16-54-19.png)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
