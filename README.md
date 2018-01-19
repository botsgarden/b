# B the 🤖
pronounce "bee"

- 🚧 WIP

## What?

**B** is a bot (chat bot)

- scalable
- polyglot (augmentable by microservices, so...)
- multi chat

## Architecture Draft

- 🚧 WIP

- **B** the main microservice
- Redis (discovery backend)
- middlewares (chat drivers) are microservices (to be validate)
- features are microservices

```                                                                                         
    ┌─────┐               model(s) allows to                                                  
    │     │               choose/trigger the appropriate                                      
    ▼     │               feature when B receive a                                            
┌──────┐  │  ┌──────┐     sentence                                                            
│ NLP  │  └─▶│Models│                                                                         
└──────┘     └──────┘                                                                         
    ▲                                                                                         
    └─────────────────┐                     ┌─────────────────────────┐                        
                      ▼             ┌──────▶│  RocketChat middleware  │◀──┐                    
                 ┌───────────┐      │       └─────────────────────────┘   │                    
          ┌─────▶│   B Bot   ◀◀─────┤                                     │   ┌──────────────┐ 
          │      └───────────┘      │                                     └──▶│  RocketChat  │ 
          │           ▲             │       ┌─────────────────────────┐       └──────────────┘ 
          │           │             └──────▶│    Slack middleware     │◀──┐                    
          │           │                     └─────────────────────────┘   │                    
          │           │                                                   │    ┌──────────────┐
          │           │                                                   └───▶│    Slack     │
          ▼           │                                                        └──────────────┘
┌─────────────────┐   │                     ┌──────────────────┐                              
│  Redis Backend  │   │                     │    Feature N     │                              
└─────────────────┘   ├────────────────────▶│    what to do    │                              
                      │                     │ (Microservice N) │                              
                      │                     └──────────────────┘                              
                      │                     ┌──────────────────┐                              
                      │                     │    Feature Z     │                              
                      ├────────────────────▶│    what to do    │                              
                      │                     │ (Microservice Z) │                              
                      │                     └──────────────────┘                              
                      │                                                                       
                      │                     ┌──────────────────┐          ┌──────────────┐    
                      │                     │Feature "Persist" │          │   DataBase   │    
                      └────────────────────▶│  (Microservice   │◀────────▶│   MongoDB    │    
                                            │    "Persist")    │          │              │    
                                            └──────────────────┘          └──────────────┘    
```

## Components

- 🚧 WIP

## Various things and resources

- https://github.com/localtunnel/localtunnel


## Test routes


See: https://github.com/kylebebak/Requester

post(
  'http://localhost:8080/yo',
  json={
    "message": "Yo it's John Doe",
    "who": "Sam Le Pirate..."
  }
)

## Run

See: https://github.com/Wramberg/TerminalView
