FROM node:12.14-alpine

RUN apk add --no-cache \
      chromium \
      nss \
      freetype \
      freetype-dev \
      harfbuzz \
      ca-certificates \
      ttf-freefont

RUN addgroup -S pptruser && adduser -S -g pptruser pptruser \
    && mkdir -p /home/pptruser/Downloads /app \
    && chown -R pptruser:pptruser /home/pptruser \
    && chown -R pptruser:pptruser /app
ENV PUPPETEER_SKIP_CHROMIUM_DOWNLOAD=true \
    PUPPETEER_EXECUTABLE_PATH=/usr/bin/chromium-browser \
    CHROME_DEVEL_SANDBOX=/usr/local/sbin/chrome-devel-sandbox
USER root
RUN npm install -g --unsafe-perm resume-cli@3.0.7 gulp-cli@2.3.0 underscore.string@3.3.5 handlebars@4.7.7
RUN npm install jsonresume-theme-elegant \
                jsonresume-theme-paper \
                jsonresume-theme-kendall \
                jsonresume-theme-flat \
                jsonresume-theme-modern \
                jsonresume-theme-classy \
                jsonresume-theme-class \
                jsonresume-theme-short \ 
                jsonresume-theme-slick \
                jsonresume-theme-onepage \
                jsonresume-theme-spartan \
                jsonresume-theme-stackoverflow \
                jsonresume-theme-macchiato \
                jsonresume-theme-caffeine \
                jsonresume-theme-macchiato-ibic \
                jsonresume-theme-kendall-ksenia \
	        jsonresume-theme-onepage-efficient \
	        jsonresume-theme-eloquent \
	        jsonresume-theme-fresh \
	        jsonresume-theme-slickoverflow \
	        jsonresume-theme-ks \
                jsonresume-theme-bootstrap-icons \
                jsonresume-theme-compact \
                jsonresume-theme-compact-extended \
                jsonresume-theme-contempo \
                jsonresume-theme-dark-classy \
                jsonresume-theme-dark-classy-responsive \
                jsonresume-theme-modern-extended \
                jsonresume-theme-nameme \
                jsonresume-theme-sceptile \
                jsonresume-theme-stackoverflow \
                jsonresume-theme-striking
                

USER node
WORKDIR /home/node
