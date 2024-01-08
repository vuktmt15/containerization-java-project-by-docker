FROM nginx
LABEL "Project"="Vprofile"
LABEL "Author"="Ajay Tekam"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
