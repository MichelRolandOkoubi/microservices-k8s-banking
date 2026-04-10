# Stage 1: Build Image
FROM node:20-alpine AS builder

WORKDIR /app

# Copy package files (if any)
# COPY package*.json ./

# Install dependencies
# RUN npm install

# Stage 2: Runtime Image
FROM node:20-alpine

WORKDIR /app

# Copy build artifacts (if any)
# COPY --from=builder /app/dist ./dist

EXPOSE 8080

CMD ["node", "-v"] # Placeholder
