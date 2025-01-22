# stack-ngrok

Run the Ngrok stack:
```
docker stack deploy -c docker-compose.yml ngrok
```

Run Ngrok directly in an existing stack for a single service, with a fixed domain:
```yml
ngrok-grafana:
    image: ngrok/ngrok:latest
    command: http 192.168.56.101:3000 --hostname=sleeping-next-wasp.ngrok-free.app
    environment:
      - NGROK_AUTHTOKEN=2ryzBSvswHIIaf8seacA....Z_6Atq8CcjF6CFK18QDytzV
```
