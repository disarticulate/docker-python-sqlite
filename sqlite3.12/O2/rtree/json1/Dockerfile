
FROM prolocutor/docker-python-sqlite:3.12
#FROM 229931fb6377
RUN cd /tmp/sqlite-autoconf-3120200 \                                                                    
        && ./configure --prefix=/usr --disable-static \                                                  
                CFLAGS="-g -O2 -DSQLITE_ENABLE_JSON1 -DSQLITE_ENABLE_RTREE"         && make \                                                                                        
        && make install \                                                                                
        && rm -r /tmp/*                                                                                  

CMD ["python3"]
