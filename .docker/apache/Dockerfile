FROM httpd:alpine

ENV HTTPD_CONF_DIR=/usr/local/apache2/conf \
    HTTPD_CONF_FILE=/usr/local/apache2/conf/httpd.conf \
    HTTPD_MODULES=authz_core_module|deflate_module|dir_module|env_module|expires_module|filter_module|headers_module|log_config_module|logio_module|mime_module|mpm_worker_module|proxy_fcgi_module|proxy_module|remoteip_module|rewrite_module|setenvif_module|ssl_module|unixd_module

# Disable all modules
RUN sed -ri "s/^\s*LoadModule/#LoadModule/g" $HTTPD_CONF_FILE && \
    # Enable only necessary modules
    sed -ri "/LoadModule ($HTTPD_MODULES)\s/s/^\s*#\s*//g" $HTTPD_CONF_FILE && \
    # Add configuration
    echo "Include $HTTPD_CONF_DIR/apache-config.conf" >> $HTTPD_CONF_FILE
