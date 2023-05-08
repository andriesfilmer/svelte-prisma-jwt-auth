# SvelteKit Auth with JWT

Related blog post: https://okupter.com/blog/handling-auth-with-jwt-in-sveltekit.

Some changes to work with mysql instead of sqlite.

    npm create svelte@latest sveltekit-auth-jwt
    npm install prisma
    npm install bcryptjs jsonwebtoken @prisma/client
    npm install -D @types/bcryptjs @types/jsonwebtoken
    npx prisma init --datasource-provider mysql
    npx prisma db push
    npx prisma generate

# Create a .env file in the root.

    DATABASE_URL="mysql://pim:some-password@localhost:3306/pim"
    JWT_ACCESS_SECRET="some-seed-pass"
