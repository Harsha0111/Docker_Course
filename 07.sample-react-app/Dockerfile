FROM node:14.16.0-alpine3.13

# RUN addgroup <grp_name> && adduser -S -G <grp_name> <user_name>
RUN addgroup app && adduser -S -G app app 
USER app
WORKDIR /app
COPY . .
RUN pnpm install
ENV MSG=Welcome_All!!
# or
#ENV MSG Welcome_All!!
EXPOSE 3000 

# RUN addgroup app && adduser -S -G app app 
# USER app

# 2 types of CMD 
# Shell form it's env is  /bin/sh and runs the CMD in shell env
# CMD npm start
# CMD npm start
# CMD npm start If we've 'n' no.of.CMD in Shell form the last one will be picked

# Exec form 
CMD ["npm" ,"start"]

# ENTRYPOINT is similar to CMD i.e., it can use both Shellform & Exec form 
#  whereas in CMD shell & exec form can be easily overwritten while run by passing arguments as e 
ENTRYPOINT ["npm" ,"start"]
# or
# ENTRYPOINT npm start









# NOTE RUN used in build-time i.e., building an img
# NOTE CMD used in run-time i.e., after build an img used to run cmnds 