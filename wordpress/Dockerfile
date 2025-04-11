FROM wordpress:latest

# Exemple : pré-installer des plugins ou thèmes
RUN curl -o /tmp/woocommerce.zip https://downloads.wordpress.org/plugin/woocommerce.latest-stable.zip && \
    unzip /tmp/woocommerce.zip -d /usr/src/wordpress/wp-content/plugins && \
    rm /tmp/woocommerce.zip

# Même chose possible pour un thème Astra ou autre
