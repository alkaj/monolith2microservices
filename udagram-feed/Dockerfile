FROM node:14

ENV POSTGRES_USERNAME=postgres \
	POSTGRES_PASSWORD=Y24HazKKYY45snf \
	POSTGRES_HOST=mono2microdb.cq2obsqhiiv6.us-east-1.rds.amazonaws.com \
	POSTGRES_DB=mono2micro \
	AWS_BUCKET=mono2micro \
	AWS_REGION=us-east-1 \
	AWS_ACCESS_KEY_ID=AKIA4XCSWIBTQQV7RXF3 \
	AWS_SECRET_ACCESS_KEY=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 \
	JWT_SECRET=mono2microtester \
	URL=http://ae68c6b4dacee4c4da57d97c5dc91b10-67604440.us-east-1.elb.amazonaws.com 

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm i

COPY . .

EXPOSE 8080

CMD ["npm", "run", "prod"]
