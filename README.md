<!-- NextJS Installation -->
npx create-next-app@latest
<!-- Shadcn UI Installation -->
npx shadcn@latest init
<!-- shadcn components Installation  -->
npx shadcn@latest add
press a and then enter to add all components

<!-- prisma setup -->
npx prisma init

<!-- eg prisma/schema.prisma -->
generator client {
  provider = "prisma-client-js"
}

datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}

model User {
  id    Int    @id @default(autoincrement())
  name  String
  email String @unique
  age   Int?
}
<!-- we communicate with our database with the help of prisma client  -->
 npm i @prisma/client
<!-- prisma code conversion to postgresql queries code -->
npx prisma migrate dev --name <migration-name>
<!-- push the user model to database -->
npx prisma db push
<!-- neon postgress db creation -->
1.login with github on https://console.neon.tech/app/projects/rough-cloud-53617953/branches/br-polished-brook-b4s3xf8d?database=neondb
2.create a project
3.press on connect and copy the db url and store it in .env

<!-- Clerk auth installation -->
 npm install @clerk/nextjs


<!-- prisma 7 installation -->
npm install -D prisma@7
npm install @prisma/client@7