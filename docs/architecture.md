# System Architecture

## Overview
<<<<<<< HEAD
DevOps Simulator follows a microservices architecture designed for high availability and scalability. This document covers both production and development configurations.
=======
DevOps Simulator follows a microservices architecture designed for high availability and scalability.

**Development Version**: This document describes the development architecture with experimental features.
>>>>>>> dev

## Components

### 1. Application Server
<<<<<<< HEAD
- **Technology**: Node.js + Express
- **Production Port**: 8080
- **Development Port**: 3000
- **Scaling**: Horizontal auto-scaling (production only)
- **Development Features**: Hot reload, debug mode

### 2. Database Layer
- **Database**: PostgreSQL 14
- **Production**: Master-slave replication with automated backups
- **Development**: Single local instance with seed data

### 3. Monitoring System
- **Production**: Prometheus + Grafana with email alerts
- **Development**: Console logging with verbose output
- **Metrics**: CPU, Memory, Disk, Network

## Deployment Strategy

### Production
- **Method**: Rolling updates
- **Zero-downtime**: Yes
- **Rollback**: Automated on failure
- **Region**: us-east-1

### Development
- **Method**: Docker Compose
- **Features**: Hot reload, instant feedback
- **Testing**: Automated tests before deployment

## Security
- **Production**: SSL/TLS encryption, strict access controls
- **Development**: Relaxed security for easier debugging
=======
- **Technology**: Node.js + Express (with hot reload)
- **Port**: 3000 (development)
- **Scaling**: Manual (single instance for development)
- **Debug**: Chrome DevTools debugger on port 9229

### 2. Database Layer
- **Database**: PostgreSQL 14 (local instance)
- **Configuration**: Single instance (no replication in dev)
- **Backup**: Manual backups only
- **Seeding**: Auto-seed with test data on startup

### 3. Monitoring System
- **Tool**: Basic console logging + Prometheus (optional)
- **Metrics**: CPU, Memory, Disk, Network, Build time
- **Alerts**: Console warnings (no email in dev)
- **Dashboard**: In-development web dashboard

### 4. NEW: Container Orchestration
- **Tool**: Docker Compose (local)
- **Services**: App, Database, Redis cache
- **Volume Mounts**: Code directory for hot reload

### 5. NEW: Authentication System (Beta)
- **Method**: OAuth2 + JWT
- **Providers**: Google, GitHub (for testing)
- **Sessions**: Redis-based session storage

## Deployment Strategy
- **Method**: Docker Compose hot reload
- **Zero-downtime**: Not applicable (dev environment)
- **Rollback**: Git checkout previous commit

## Development Workflow
1. Make code changes
2. Auto-reload triggers rebuild
3. Run unit tests
4. Check console logs
5. Commit when ready

## Security
- SSL/TLS disabled for local development
- Database credentials in plain text (dev only)
- CORS enabled for all origins
- Debug endpoints exposed

## Experimental Features
⚠️ **Warning**: The following features are experimental:
- Multi-cloud deployment
- AI-powered log analysis
- Automatic rollback on anomaly detection
>>>>>>> dev
