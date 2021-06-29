# Solução desafio devops
- Inicialmente foi analisado o arquivo do docker-compose.yaml onde encontrados as seguintes divergencias:
   - O nome do redis estava escrito errado (reids) linha 22
   - Não havia porta descrita no redis
   - No Networks na linha 26 só havia descrito o backend, estava faltando o frontend que constava que também era chamado conforme linha 9

- A segunda parte da análise foi verificar se as portas informadas no docker-compose estavam iguais nos arquivos de frontend,reader e writer contidas na pasta services. Lá vericamos as seguinter divergencias:

  - A porta do reader estava errada no docker-compose, a porta correta era a 8080 conforme arquivo main.go dentro da pasta reader
  - A porta do redis era a 6379 conforme informado no arquivo main.go dentro da pasta reader
  - A porta do whiter também estava errada, a porta correta era a 8081 conforma arquivo main.py dentro da pasta writer

- Após a análise foram aplicadas todas modificações no arquivo docker-compose.yaml conforme os pontos citados acima. 
