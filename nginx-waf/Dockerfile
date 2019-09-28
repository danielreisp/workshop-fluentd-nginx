FROM owasp/modsecurity:3.0-nginx

# https://docs.nginx.com/nginx-waf/admin-guide/nginx-plus-modsecurity-waf-owasp-crs/
#RUN wget https://github.com/SpiderLabs/owasp-modsecurity-crs/archive/v3.0.2.tar.gz && \
#    tar -xzvf v3.0.2.tar.gz && \
#    rm v3.0.2.tar.gz && \
#    mv owasp-modsecurity-crs-3.0.2 /usr/local && \
#    cp /usr/local/owasp-modsecurity-crs-3.0.2/crs-setup.conf.example /usr/local/owasp-modsecurity-crs-3.0.2/crs-setup.conf

#Refer CRS OWASP
COPY include.conf /etc/modsecurity.d/include.conf

#Enable WAF
RUN sed -i "s/SecRuleEngine DetectionOnly/SecRuleEngine On/" /etc/modsecurity.d/modsecurity.conf
