LDFLAGS			:= -I/usr/include/libdrm
LDFLAGS			+= -ldrm

TARGET			:= drmDevice
INCLUDE += 

STRIP           := ls
CFLAGS	+=
OBJS = \
	drmDevice.o\

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

