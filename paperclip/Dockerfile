FROM node:20-slim

# Install pnpm and git
RUN npm install -g pnpm && apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*

WORKDIR /app

# Clone Paperclip source
RUN git clone https://github.com/paperclipai/paperclip.git .

# Install dependencies
RUN pnpm install

# Build all packages
RUN pnpm build

EXPOSE 3100

CMD ["pnpm", "--filter", "@paperclipai/server", "start"]
