# Makefile for MUSE Unilever Hackathon #

ROOT := .

include $(ROOT)/make-include.mk

all: setup

setup:
	sudo mkdir -p $(HUL_INSTALL_DIR)

	sudo mkdir -p $(HUL_INSTALL_DIR)/$(BARCODE_DATA)
	sudo cp ./$(BARCODE_DATA)/$(BARCODE_DATAFILE) $(HUL_INSTALL_DIR)/$(BARCODE_DATA)

	sudo mkdir -p $(HUL_INSTALL_DIR)/$(IMAGE_DATA)
	sudo touch $(HUL_INSTALL_DIR)/$(ONLINE_THRESHOLD)
	echo "0" > $(HUL_INSTALL_DIR)/$(ONLINE_THRESHOLD) 2>&1
	sudo touch $(HUL_INSTALL_DIR)/$(OFFLINE_THRESHOLD)
	echo "0" > $(HUL_INSTALL_DIR)/$(OFFLINE_THRESHOLD) 2>&1
	sudo touch $(HUL_INSTALL_DIR)/$(IS_OFFLINE)
	echo "0" > $(HUL_INSTALL_DIR)/$(IS_OFFLINE) 2>&1
	sudo cp CheckNetwork.py $(HUL_INSTALL_DIR)
	sudo cp InvokeCheckNetwork.sh $(HUL_INSTALL_DIR)
	sudo cp DataUpload.py $(HUL_INSTALL_DIR)
	sudo cp InvokeDataUpload.sh $(HUL_INSTALL_DIR)
	bash setupCron.sh

clean:
	#TODO: Implement clean operation
