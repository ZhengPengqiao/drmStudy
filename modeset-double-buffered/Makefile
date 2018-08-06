LDFLAGS			:= -I../Doc/libdrm-imx8/include/libdrm -I../Doc/libdrm-imx8/include
LDFLAGS			+= -L../Doc/libdrm-imx8/lib/ -ldrm

TARGET			:= modeset-double-buffered
INCLUDE += 

STRIP           := ls
CFLAGS	+=
OBJS = \
	modeset-double-buffered.o\

all:$(TARGET)

$(TARGET):$(OBJS)
	$(CXX) $(CFLAGS) -O3  -o $@ $^ $(LDFLAGS) $(INCLUDE)
	$(STRIP) $@


%.o:%.cpp
	$(CXX) $(CFLAGS) -c -O3 -o $@ $< $ $(INCLUDE) $(LDFLAGS)

%.o:%.c
	$(CXX) $(CFLAGS) -c -O3 -o $@ $< $ $(INCLUDE) $(LDFLAGS)

clean:
	@rm -rf *.o $(TARGET) $(OBJS)

