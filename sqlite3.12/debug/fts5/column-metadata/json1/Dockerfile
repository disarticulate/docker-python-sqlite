
FROM prolocutor/docker-python-sqlite:3.12

RUN cd /tmp/sqlite-autoconf-3120200 \                                                                    
        && ./configure --prefix=/usr --disable-static \                                                  
                CFLAGS="-g -DSQLITE_ENABLE_COLUMN_METADATA -DSQLITE_DEBUG -DSQLITE_ENABLE_FTS5 -DSQLITE_ENABLE_JSON1"         && make \                                                                                        
        && make install \                                                                                
        && rm -r /tmp/*                                                                                  
                                                                                                         
CMD ["python3"]
