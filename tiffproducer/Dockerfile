FROM java:latest

# install libreoffice
RUN wget http://download.documentfoundation.org/libreoffice/stable/5.0.3/deb/x86_64/LibreOffice_5.0.3_Linux_x86-64_deb.tar.gz \
&& tar -xvf LibreOffice_5.0.3_Linux_x86-64_deb.tar.gz --no-same-owner \
&& cd LibreOffice_5.0.3.2_Linux_x86-64_deb/DEBS \
&& dpkg -i *.deb \
&& cd ../.. \
&& rm -rf LibreOffice_5.0*


#install ghostscript
RUN wget http://downloads.ghostscript.com/public/binaries/ghostscript-9.18-linux-x86_64.tgz \
&& tar -xvf ghostscript-9.18-linux-x86_64.tgz --no-same-owner \
&& rm ghostscript-9.18-linux-x86_64.tgz \
&& mv ghostscript-9.18-linux-x86_64 /opt/ \
&& ln -s /opt/ghostscript-9.18-linux-x86_64/gs-918-linux_x86_64 /usr/local/bin/gs

