# mono-monolith

- [ ] FE apps & BE services together in a mono repo
- [ ] One build which runs only the stuff that’s changed 
- [ ] Full stack testing which can target FE or BE 
- [ ] Acceptance testing BE services 
- [ ] Acceptance testing FE app
- [ ] Composable developer environment
- [ ] Deployable full stack feature branches
- [ ] Developer experience... one command dev env setup 


docker-compose -f app-docker-compose.yml exec fe-app ng test --watch=false

docker-compose -f app-docker-compose.yml exec fe-app ng e2e --port 4201
