GeoCAD 🗺️
> Plataforma web open source para geração de bases cartográficas editáveis em DXF/DWG — alternativa gratuita ao Plex-Earth para AutoCAD LT.
![GeoCAD Banner](docs/banner.png)
✨ Funcionalidades
Módulo	Descrição
KML/KMZ → DXF	Upload e conversão automática com layers
Base Cartográfica	Geração automática via OSM, IBGE, Copernicus
Organização CAD	Layers padronizadas para projetos de infraestrutura
Ferramentas GIS	Reprojeção, recorte, união, exportação multi-formato
IA / Visão Computacional	Detecção automática de edificações, vias, vegetação
🛠 Stack
```
Frontend  → React 18 + TypeScript + Tailwind CSS + Leaflet
Backend   → Python 3.12 + FastAPI + GeoPandas + GDAL + ezdxf
Banco     → PostgreSQL 16 + PostGIS 3.4
Deploy    → Docker Compose / Cloudflare Pages / Render
```
🚀 Início Rápido
Pré-requisitos
Docker ≥ 24 e Docker Compose ≥ 2.20
Node.js 20+ (apenas desenvolvimento local do frontend)
Subir com Docker
```bash
git clone https://github.com/seu-usuario/geocad.git
cd geocad
cp .env.example .env
docker compose up --build
```
Acesse: http://localhost:5173
Desenvolvimento local (sem Docker)
Backend:
```bash
cd backend
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```
Frontend:
```bash
cd frontend
npm install
npm run dev
```
📁 Estrutura do Projeto
```
geocad/
├── frontend/          # React + TypeScript
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── store/
│       └── services/
├── backend/           # FastAPI + Python
│   └── app/
│       ├── api/v1/
│       ├── services/
│       ├── models/
│       └── core/
├── docker/            # Dockerfiles
├── docs/              # Documentação
└── .github/workflows/ # CI/CD
```
📖 Documentação da API
Após subir o backend: http://localhost:8000/docs
🤝 Contribuindo
Veja CONTRIBUTING.md.
📄 Licença
MIT — veja LICENSE.
