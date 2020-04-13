# spoke-xrchat-adapter

## HTTPRequest Spoke

### getProjects()
#### Request
    Method GET   - https://dev.reticulum.io/api/v1/projects
    Query Params:
        headers = {
        "content-type": "application/json",
        authorization: `Bearer ${token}`
        For example:
        authorization= Bearer eyJhbGciOiJIUzUxMiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJyZXQiLCJleHAiOjE1OTM3NjYzNjIsImlhdCI6MTU4NjUwODc2MiwiaXNzIjoicmV0IiwianRpIjoiNGMxYTcwZGQtYTk3MC00OGEzLTg4YjEtOGU3NDk2M2JlZTNjIiwibmJmIjoxNTg2NTA4NzYxLCJzdWIiOiI2Nzc4MjIzNTY0NzQ4MjI4OTUiLCJ0eXAiOiJhY2Nlc3MifQ.ZyDJmByhBcABI8eIqoyllnnKwyB_5jvBzd9unm96fN65LLz8IoAYo1tS3zqD1E3rF9F6Vh_C-sqiBGlJpHnlMQ
        };
        
#### Response
    Content-Type - application/json; charset=utf-8
    Body: 
        {
            "projects": []
        }



### getProject(projectId)
#### Request
    Method GET   - https://dev.reticulum.io/api/v1/projects/${projectId}
    Query Params:
        headers = {
        "content-type": "application/json",
        authorization: `Bearer ${token}`
        For example:
        authorization= Bearer eyJhbGciOiJIUzUxMiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJyZXQiLCJleHAiOjE1OTM3NjYzNjIsImlhdCI6MTU4NjUwODc2MiwiaXNzIjoicmV0IiwianRpIjoiNGMxYTcwZGQtYTk3MC00OGEzLTg4YjEtOGU3NDk2M2JlZTNjIiwibmJmIjoxNTg2NTA4NzYxLCJzdWIiOiI2Nzc4MjIzNTY0NzQ4MjI4OTUiLCJ0eXAiOiJhY2Nlc3MifQ.ZyDJmByhBcABI8eIqoyllnnKwyB_5jvBzd9unm96fN65LLz8IoAYo1tS3zqD1E3rF9F6Vh_C-sqiBGlJpHnlMQ
        https://dev.reticulum.io/api/v1/projects/nBYdkAk

        };
        
 
#### Response
    Content-Type - application/json; charset=utf-8
    Body:
    For example:
        {
            "name": "DIMA",
            "parent_scene": null,
            "project_id": "nBYdkAk",
            "project_url": "https://hubs-upload-cdn.com/files/1a011c60-18f3-4b42-9725-af20b59fc5e2.json",
            "scene": null,
            "status": "ok",
            "thumbnail_url": "https://hubs-upload-cdn.com/files/1b5b0c6a-56b5-46fc-bdf7-454ef588f939.jpg"
        }

### resolveUrl(url, index)
#### Request
    method: "POST", 
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({ media: { url, index } })
#### Response
    Content-Type - application/json; charset=utf-8
    Body 
        {
        "projects": []
        } 

### searchMedia(source, params, cursor, signal)
#### Request
    Method GET   - https://dev.reticulum.io/api/v1/media/search
    Query Params:
        source=scene_listings
        filter=featured-remixable
        q=
#### Response
    Content-Type - application/json; charset=utf-8
    Body
        {
            "meta": {
                "source": "scene_listings",
                "next_cursor": null
            },
            "entries": [
                {
                    "allow_remixing": true,
                    "attributions": {
                        "content": [],
                        "creator": "JCo"
                    },
                    "description": null,
                    "id": "8MGx5ja",
                    "images": {
                        "preview": {
                            "url": "https://hubs-upload-cdn.com/files/1cf4498d-b54f-4f8a-b9f5-e9bc8981ffd9.jpg"
                        }
                    },
                    "name": "Crater",
                    "project_id": "oE85XeZ",
                    "type": "scene_listing",
                    "url": "https://dev.reticulum.io/scenes/8MGx5ja/crater"
                },
                {
                    "allow_remixing": true,
                    "attributions": {
                        "content": [],
                        "creator": "JCo"
                    },
                    "description": null,
                    "id": "eP5SjvW",
                    "images": {
                        "preview": {
                            "url": "https://hubs-upload-cdn.com/files/32b1e698-741f-48e2-b6af-6b540cf4f3b2.jpg"
                        }
                    },
                    "name": "Surrounded Lake",
                    "project_id": "ai2PpSn",
                    "type": "scene_listing",
                    "url": "https://dev.reticulum.io/scenes/eP5SjvW/surrounded-lake"
                },
                {
                    "allow_remixing": true,
                    "attributions": {
                        "content": [
                            {
                                "author": "mozillareality",
                                "name": "House with Open Atrium",
                                "url": "https://sketchfab.com/models/bc1046092d334bbbacdb40c1cf8796cd"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Couch - midcentury modern",
                                "url": "https://sketchfab.com/models/f8def3c5f656454c935fe3d626ed9fab"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Armchair - midcentury modern",
                                "url": "https://sketchfab.com/models/f26063c8ca6a438d9e328b28434d1c44"
                            },
                            {
                                "author": "mozillareality",
                                "name": "End table - wooden with magazine rack",
                                "url": "https://sketchfab.com/models/7fab655234e84e0ea6a3ada36ece2ad1"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Ceiling Fan",
                                "url": "https://sketchfab.com/models/ec2c6087d4824211abc827f2a4c2b578"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Light Fixture - Ceiling Recessed",
                                "url": "https://sketchfab.com/models/269fd427629548a8a0949a6493c5b223"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Dresser - modern light wood",
                                "url": "https://sketchfab.com/models/25134a84c07e420b93cae181731fd7a0"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Bookshelf - tall wooden",
                                "url": "https://sketchfab.com/models/efe2a35b92c443519fab5a5b515e92ab"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Desk - marble top",
                                "url": "https://sketchfab.com/models/328eb54341cc4b3f9c7a07fa1cb71a02"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Desk Lamp - brushed aluminum",
                                "url": "https://sketchfab.com/models/da4b9020b0614309ab787b67f63c1dba"
                            },
                            {
                                "author": "gromorg",
                                "name": "plant",
                                "url": "https://sketchfab.com/models/fb13bf916dac4bd59f34f2d7d73a49dc"
                            },
                            {
                                "author": "nenjo",
                                "name": "Spruce Tree - Low Poly",
                                "url": "https://sketchfab.com/models/b68f79aee62f4e849be265c903f724f5"
                            },
                            {
                                "author": "sirenko",
                                "name": "Radiola Deep Image 209C",
                                "url": "https://sketchfab.com/models/adf58ffecf8b434bbbecf46596348c56"
                            },
                            {
                                "author": "吉木さゆみザ日本のプリンセス (PrincessSayumi92)",
                                "name": "美人画 2",
                                "url": "https://sketchfab.com/models/8ed0cbfccfa1449996ff0b06875b1863"
                            }
                        ],
                        "creator": "JCo"
                    },
                    "description": null,
                    "id": "Cpc7BNg",
                    "images": {
                        "preview": {
                            "url": "https://hubs-upload-cdn.com/files/36261ffd-8033-4a15-af65-d2c7d62fca38.jpg"
                        }
                    },
                    "name": "MozAtrium",
                    "project_id": "kCkmigY",
                    "type": "scene_listing",
                    "url": "https://dev.reticulum.io/scenes/Cpc7BNg/mozatrium"
                },
                {
                    "allow_remixing": true,
                    "attributions": {
                        "content": [
                            {
                                "author": "mozillareality",
                                "name": "Table - Hightop",
                                "url": "https://sketchfab.com/models/e49e5780b5724c4d9dc747b6f0b0ad0e"
                            }
                        ],
                        "creator": "JCo"
                    },
                    "description": null,
                    "id": "cHILDgx",
                    "images": {
                        "preview": {
                            "url": "https://hubs-upload-cdn.com/files/799af698-39a1-4514-9221-ac02d45fd4c3.jpg"
                        }
                    },
                    "name": "Outdoor Meetup",
                    "project_id": "6SPCHbY",
                    "type": "scene_listing",
                    "url": "https://dev.reticulum.io/scenes/cHILDgx/outdoor-meetup"
                },
                {
                    "allow_remixing": true,
                    "attributions": {
                        "content": [
                            {
                                "author": "Kagelok",
                                "name": "The River",
                                "url": "https://uploads-prod.reticulum.io/files/4efcd6f5-e7a8-47ac-8de1-9d4b174dd70b.glb"
                            }
                        ],
                        "creator": "JCo"
                    },
                    "description": null,
                    "id": "EdaLEhH",
                    "images": {
                        "preview": {
                            "url": "https://hubs-upload-cdn.com/files/4388a2c6-bebd-45f4-8f92-6ed2ba3969c9.jpg"
                        }
                    },
                    "name": "River Island",
                    "project_id": "U7mN4Pz",
                    "type": "scene_listing",
                    "url": "https://dev.reticulum.io/scenes/EdaLEhH/river-island"
                },
                {
                    "allow_remixing": true,
                    "attributions": {
                        "content": [
                            {
                                "author": "mozillareality",
                                "name": "Nightclub"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Disco Ball"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Table - Hightop"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Light Fixture - Ceiling Recessed",
                                "url": "https://sketchfab.com/models/269fd427629548a8a0949a6493c5b223"
                            }
                        ],
                        "creator": "JCo"
                    },
                    "description": null,
                    "id": "dhJdsGe",
                    "images": {
                        "preview": {
                            "url": "https://hubs-upload-cdn.com/files/f477ca40-b297-4de2-940c-6a221d4e88f7.jpg"
                        }
                    },
                    "name": "Club Hub",
                    "project_id": "UdrNVgn",
                    "type": "scene_listing",
                    "url": "https://dev.reticulum.io/scenes/dhJdsGe/club-hub"
                },
                {
                    "allow_remixing": true,
                    "attributions": {
                        "content": [
                            {
                                "author": "mozillareality",
                                "name": "Meeting Space - Hubs Original",
                                "url": "https://sketchfab.com/models/bdcd3132591f4d0082505189ba826042"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Cliff Vista - Hubs Original",
                                "url": "https://sketchfab.com/models/36f4e5b68dce4931a5384ec903309d6b"
                            },
                            {
                                "author": "mozillareality",
                                "name": "Light Fixture - Ceiling Recessed",
                                "url": "https://sketchfab.com/models/269fd427629548a8a0949a6493c5b223"
                            }
                        ],
                        "creator": "JCo"
                    },
                    "description": null,
                    "id": "hi1LwJS",
                    "images": {
                        "preview": {
                            "url": "https://hubs-upload-cdn.com/files/d7aa64b8-f898-4151-b845-0a4d7a6f474d.jpg"
                        }
                    },
                    "name": "Cliffside Meeting Room",
                    "project_id": "K2XmNFN",
                    "type": "scene_listing",
                    "url": "https://dev.reticulum.io/scenes/hi1LwJS/cliffside-meeting-room"
                },
                {
                    "allow_remixing": true,
                    "attributions": {
                        "content": [
                            {
                                "author": "Thomas Kole",
                                "name": "Cudillero Diorama Bake"
                            }
                        ],
                        "creator": "JCo"
                    },
                    "description": null,
                    "id": "xvX4qCa",
                    "images": {
                        "preview": {
                            "url": "https://hubs-upload-cdn.com/files/bda54641-ff53-4d2b-8354-3ead117f70b1.jpg"
                        }
                    },
                    "name": "Cudillero Diorama",
                    "project_id": "Yiv8Ejf",
                    "type": "scene_listing",
                    "url": "https://dev.reticulum.io/scenes/xvX4qCa/cudillero-diorama"
                },
                {
                    "allow_remixing": true,
                    "attributions": {
                        "content": [
                            {
                                "author": "roelandvermeulen",
                                "name": "Stylized Hunter's Lodge",
                                "url": "https://sketchfab.com/models/b750361a12b64deabca4418cda8ec3ed"
                            }
                        ],
                        "creator": "JCo"
                    },
                    "description": null,
                    "id": "YpW55Ft",
                    "images": {
                        "preview": {
                            "url": "https://hubs-upload-cdn.com/files/bacc92ae-dacf-4937-9c80-dd3d83c162d8.jpg"
                        }
                    },
                    "name": "Hunters Lodge",
                    "project_id": "teLef5x",
                    "type": "scene_listing",
                    "url": "https://dev.reticulum.io/scenes/YpW55Ft/hunters-lodge"
                },
                {
                    "allow_remixing": true,
                    "attributions": {
                        "content": [
                            {
                                "author": "j-conrad",
                                "name": "Trippy Tunnel v2",
                                "url": "https://sketchfab.com/models/8a48afd0bea749a786f6f16a203a93e8"
                            }
                        ],
                        "creator": "JCo"
                    },
                    "description": null,
                    "id": "qnwcbrL",
                    "images": {
                        "preview": {
                            "url": "https://hubs-upload-cdn.com/files/ab2144e0-f715-446e-97a4-00b27688910c.jpg"
                        }
                    },
                    "name": "Trippy Tunnel",
                    "project_id": "eRtigkL",
                    "type": "scene_listing",
                    "url": "https://dev.reticulum.io/scenes/qnwcbrL/trippy-tunnel"
                },
                {
                    "allow_remixing": true,
                    "attributions": {
                        "content": [],
                        "creator": "JCo"
                    },
                    "description": null,
                    "id": "dkzQCHO",
                    "images": {
                        "preview": {
                            "url": "https://hubs-upload-cdn.com/files/916736ed-2e57-4439-a977-537528a79040.jpg"
                        }
                    },
                    "name": "Wide Open Space",
                    "project_id": "aoqAQ4F",
                    "type": "scene_listing",
                    "url": "https://dev.reticulum.io/scenes/dkzQCHO/wide-open-space"
                }
            ],
            "suggestions": null
        }






### createProject(scene, parentSceneId, thumbnailBlob, signal, showDialog, hideDialog) 
#### Request
    Method POST   - https://dev.reticulum.io/api/v1/projects
    { method: "POST", headers, body, signal }
    headers = {
        "content-type": "application/json",
        authorization: `Bearer ${token}`
        For example:
        authorization= Bearer eyJhbGciOiJIUzUxMiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJyZXQiLCJleHAiOjE1OTM3NjYzNjIsImlhdCI6MTU4NjUwODc2MiwiaXNzIjoicmV0IiwianRpIjoiNGMxYTcwZGQtYTk3MC00OGEzLTg4YjEtOGU3NDk2M2JlZTNjIiwibmJmIjoxNTg2NTA4NzYxLCJzdWIiOiI2Nzc4MjIzNTY0NzQ4MjI4OTUiLCJ0eXAiOiJhY2Nlc3MifQ.ZyDJmByhBcABI8eIqoyllnnKwyB_5jvBzd9unm96fN65LLz8IoAYo1tS3zqD1E3rF9F6Vh_C-sqiBGlJpHnlMQ
        https://dev.reticulum.io/api/v1/projects/nBYdkAk

        };
    body:
        {name: scene.name,
        thumbnail_file_id,
        thumbnail_file_token,
        project_file_id,
        project_file_token}
    signal
#### Response
    Content-Type - application/json; charset=utf-8
    Body
        {
        }







### deleteProject(projectId) 
    method: "DELETE" - https://${RETICULUM_SERVER}/api/v1/projects/${projectId}
    headers = {
    "content-type": "application/json",
    authorization: `Bearer ${token}`
    }

    

### saveProject(projectId, editor, signal, showDialog, hideDialog) {
    method: "PATCH" -  `https://${RETICULUM_SERVER}/api/v1/projects/${projectId}`
    headers = {
    "content-type": "application/json",
    authorization: `Bearer ${token}`
    }
    body:{
      name: editor.scene.name,
      thumbnail_file_id,
      thumbnail_file_token,
      project_file_id,
      project_file_token
    };
    signal

    




### getScene(sceneId) {
    method: "POST" - `https://${RETICULUM_SERVER}/api/v1/scenes/${sceneId}`
    headers = {
      "content-type": "application/json"
    };

   

  
### upload(blob, onUploadProgress, signal)
    Method POST - https://${uploadHost}:${uploadPort}/api/v1/media 
    







### async publishProject(project, editor, showDialog, hideDialog) {
    method: "POST" - `https://${RETICULUM_SERVER}/api/v1/projects/${project.project_id}/publish`
    headers = {
        "content-type": "application/json",
        authorization: `Bearer ${token}`
    };
    body:
        {screenshot_file_id: screenshotId,
        screenshot_file_token: screenshotToken,
        model_file_id: glbId,
        model_file_token: glbToken,
        scene_file_id: sceneFileId,
        scene_file_token: sceneFileToken,
        allow_remixing: publishParams.allowRemixing,
        allow_promotion: publishParams.allowPromotion,
        name: publishParams.name,
        attributions: {
          creator: publishParams.creatorAttribution,
          content: publishParams.contentAttributions
        }

     
### uploadAsset(editor, file, onProgress, signal) {
    method: "POST" -  `https://${RETICULUM_SERVER}/api/v1/projects/${projectId}/assets`,
    headers = {
        "content-type": "application/json",
        authorization: `Bearer ${token}`
    };
    body = asset: {
        name: file.name,
        file_id: asset_file_id,
        access_token: asset_access_token,
        thumbnail_file_id,
        thumbnail_access_token
    }
    signal 

###  uploadProjectAsset(editor, projectId, file, onProgress, signal) {

    method: "POST" -  `https://${RETICULUM_SERVER}/api/v1/projects/${projectId}/assets`,
  
    headers = {
      "content-type": "application/json",
      authorization: `Bearer ${token}`
    };

    body = {
      asset: {
        name: file.name,
        file_id: asset_file_id,
        access_token: asset_access_token,
        thumbnail_file_id,
        thumbnail_access_token
      }
    };
    signal

### deleteAsset(assetId) {
    method: "DELETE" `https://${RETICULUM_SERVER}/api/v1/assets/${assetId}`
    headers = {
      "content-type": "application/json",
      authorization: `Bearer ${token}`
    };

### deleteProjectAsset(projectId, assetId) 
    method: "DELETE" `https://${RETICULUM_SERVER}/api/v1/projects/${projectId}/assets/${assetId}`
    headers = {
        "content-type": "application/json",
        authorization: `Bearer ${token}`
    };



