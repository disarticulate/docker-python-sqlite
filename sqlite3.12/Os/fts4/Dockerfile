
FROM prolocutor/docker-python-sqlite:3.12

RUN cd /tmp/sqlite-autoconf-3120200 \                                                                    
        && ./configure --prefix=/usr --disable-static \                                                  
                CFLAGS="-g -Os -DSQLITE_ENABLE_FTS4"         && make \                                                                                        
        && make install \                                                                                
        && rm -r /tmp/*                                                                                  
                                                                                                         
CMD ["python3"]
