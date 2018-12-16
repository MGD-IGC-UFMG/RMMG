FROM mgdigcufmg/rmmg-wordpress
RUN chmod -R 755 /var/www  && \
    chown -R www-data:www-data /var/www
RUN find /var/www/html/ -type f -exec sed -i 's/minerais-mg.com.br/127.0.0.1/g' {} \;
    
