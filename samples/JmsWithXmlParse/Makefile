# Copyright (C)2014, International Business Machines Corporation and  
# others. All Rights Reserved.                        
.PHONY: all clean

STREAMS_MESSAGING_TOOLKIT ?= ../../com.ibm.streamsx.messaging:${STREAMS_INSTALL}/toolkits/com.ibm.streamsx.messaging

SPLC_FLAGS ?= -a -t ${STREAMS_MESSAGING_TOOLKIT}

SPLC = $(STREAMS_INSTALL)/bin/sc

SPL_CMD_ARGS ?=
SPL_MAIN_COMPOSITE = application::JmsWithXmlParse
OUTPUT_DIR = output

all: 
	$(SPLC) $(SPLC_FLAGS) -M $(SPL_MAIN_COMPOSITE) --output-dir ./$(OUTPUT_DIR) $(SPL_CMD_ARGS)

clean:
	$(SPLC) $(SPLC_FLAGS) -C -M $(SPL_MAIN_COMPOSITE)


