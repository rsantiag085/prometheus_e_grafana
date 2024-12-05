# Docker Compose: Prometheus e Grafana

Este repositório contém um arquivo `docker-compose.yml` que configura e executa o **Prometheus** e o **Grafana** em containers Docker. 

## Detalhes do Projeto

- **Prometheus**:
  - **Porta exposta**: `9090`
  - **Volume configurado** para persistência de dados.
  - Configurado para coletar e exibir métricas de forma eficiente.

- **Grafana**:
  - **Porta exposta**: `3000`
  - Painel de visualização de métricas.
  - Senha padrão para login: `admin`.

---

## Requisitos

- [Docker](https://www.docker.com/) e [Docker Compose](https://docs.docker.com/compose/) instalados.

---

## Como Usar

1. **Clone este repositório**:
   ```bash
   git clone https://github.com/seu-usuario/docker-compose-prometheus.git
   cd docker-compose-prometheus
   ```

2. **Inicie os serviços**:
   ```bash
   docker-compose up -d
   ```

3. **Acesse os serviços**:
   - Prometheus: [http://localhost:9090](http://localhost:9090)
   - Grafana: [http://localhost:3000](http://localhost:3000)  
     (Login: `admin` / Senha: `admin`)

4. *(Opcional)* Configure fontes de dados e dashboards no Grafana para visualizar métricas.

---

## Configurações Personalizadas

- **Volumes**:  
  O volume `prometheus-data` armazena os dados do Prometheus, garantindo a persistência após reinicializações.

- **Rede**:  
  A rede `monitoring` permite a comunicação entre os containers Prometheus e Grafana.

---

