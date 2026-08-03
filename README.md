<img width="1842" height="854" alt="desk-compass" src="https://github.com/user-attachments/assets/cb7ecc61-ad32-4feb-9ea2-a3bf2bee88e6" /><img width="1842" height="854" alt="desk-compass" src="https://github.com/user-attachments/assets/503f2d00-c4f8-4d0a-ae11-a210cb9fbc97" />


# Supply Chain Compass

**"Where is my inventory?" – Search no more.**

Supply Chain Compass is an open-source platform for visualizing warehouses, distribution centers, factories, and logistics hubs. Manage facility layouts, track inventory and equipment locations, and give operations teams a live overview of everything happening inside your supply chain facilities.

---

## Overview

Supply Chain Compass provides an interactive map of your warehouse where every physical asset can be represented as a marker.

Instead of static warehouse drawings or spreadsheets, operations teams can quickly locate:

- Inventory
- Pallets
- Containers
- Forklifts
- AGVs and robots
- Picking carts
- Dock doors
- Storage racks
- Safety equipment
- Employees (optional)
- Orders in progress

Designed to integrate with Warehouse Management Systems (WMS), ERP platforms, barcode scanners, RFID readers, and IoT devices.

---

## Features

### Interactive Warehouse Map

- Visualize warehouse layouts
- Support multiple warehouse zones
- Organize storage locations
- Display racks, bins, docks, and workstations

### Asset Tracking

Display different types of assets including:

- Inventory
- Storage locations
- Pallets
- Containers
- Forklifts
- AGVs
- Picking carts
- Robots
- Shipping docks
- Receiving areas
- Packing stations
- Safety equipment

### Search & Filtering

Quickly locate assets by:

- SKU
- Order Number
- Pallet ID
- Container ID
- Batch
- Lot Number
- Vehicle
- Warehouse Zone

Filter by:

- Available Inventory
- Reserved Inventory
- Damaged Goods
- Inbound Shipments
- Outbound Shipments
- Cold Storage
- High Value Inventory

### Live Operations Dashboard

Visualize:

- Active Picking
- Receiving
- Shipping
- Packing
- Inventory Status
- Equipment Utilization

### Asset Management

- Move assets
- Rotate assets
- Edit properties
- Upload images
- Assign ownership
- Update operational status

### API

REST API with OpenAPI documentation.

### Monitoring

- Health endpoint
- Metrics endpoint
- Prometheus compatible metrics

---

## Typical Use Cases

- Warehouses
- Distribution Centers
- Manufacturing Plants
- Retail Fulfillment Centers
- Cold Storage Facilities
- Ports & Logistics Hubs
- Cross Dock Operations

---

## Technology

- Node.js
- TypeScript
- React
- REST API
- OpenAPI
- Docker
- Prometheus Metrics

---

## Getting Started

### Development

Requirements:

- Node.js >= 18
- Yarn

Install dependencies

```bash
yarn install
```

Start development

```bash
yarn start
```

Application

```
http://localhost:3000
```

API

```
http://localhost:3030/api/swagger
```

Health

```
http://localhost:3030/health
```

Metrics

```
http://localhost:3033/metrics
```

---

## Production

```bash
cp environments/.env.development environments/.env

yarn install --frozen-lockfile --ignore-scripts

yarn build
```

Deploy the generated backend and frontend as described below.

---

## Docker

```bash
docker build -t supply-chain-compass .

docker run \
  --rm \
  --name supply-chain-compass \
  -e DATABASE_PATH=/storage/db \
  -e IMAGE_STORAGE_PATH=/storage/images \
  -v "/warehouse-data:/storage" \
  -p 5000:3030 \
  supply-chain-compass
```

Open

```
http://localhost:5000
```

---

## Environment Variables

Required

- DATABASE_PATH
- IMAGE_STORAGE_PATH

Optional

- NODE_ENV
- API_PORT
- DATABASE_HUMAN_READABLE
- CORS_ALLOWED_ORIGINS
- CORS_ALLOWED_METHODS
- METRICS_PORT

---

## Roadmap

- RFID Integration
- Barcode Scanner Integration
- IoT Device Integration
- ERP Integration
- Warehouse Management System Integration
- Live Equipment Tracking
- Inventory Heatmaps
- Capacity Planning
- Yard Management
- Digital Twin Support



