X_LIBS		+= libxlibc-0.0.1.a libgapi-0.1.0.a

X_INCDIRS	+= bosh/include

NAME		:= bosh
SRC			+= main.c shell/ terminal/

define CUSTOM_TARGET_CMD
echo [APP] $@; \
$(LD) $(X_LDFLAGS) $(X_OBJS) -o $@ $(patsubst %, -L%, $(X_LIBDIRS)) --start-group $(patsubst %, -l:%, $(X_LIBS)) --end-group; \
cp $@ $(srctree)/../develop/rom/usr
endef
