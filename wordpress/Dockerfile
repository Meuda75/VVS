# Utilise l'image officielle WordPress
FROM wordpress:latest

# Installe unzip et d'autres utilitaires nécessaires
RUN apt-get update && \
    apt-get install -y unzip file && \
    rm -rf /var/lib/apt/lists/*

# Télécharge et installe le plugin WooCommerce (version spécifique pour stabilité)
RUN curl --retry 3 -L -o /tmp/woocommerce.zip https://downloads.wordpress.org/plugin/woocommerce.9.8.1.zip && \
    unzip -t /tmp/woocommerce.zip && \
    unzip /tmp/woocommerce.zip -d /usr/src/wordpress/wp-content/plugins && \
    rm /tmp/woocommerce.zip

# Optionnel : ajoute d'autres plugins ou thèmes ici
# Exemple pour le thème Astra
RUN curl --retry 3 -L -o /tmp/astra.zip https://downloads.wordpress.org/theme/astra.latest-stable.zip && \
    unzip -t /tmp/astra.zip && \
    unzip /tmp/astra.zip -d /usr/src/wordpress/wp-content/themes && \
    rm /tmp/astra.zip