# Copyright 2023 ETH Zurich and University of Bologna.
# Licensed under the Apache License, Version 2.0, see LICENSE for details.
# SPDX-License-Identifier: Apache-2.0
#
# Luca Colagrande <colluca@iis.ee.ethz.ch>

# Usage of absolute paths is required to externally include this Makefile
MK_DIR   := $(dir $(realpath $(lastword $(MAKEFILE_LIST))))
DATA_DIR := $(realpath $(MK_DIR)/data)
SRC_DIR  := $(realpath $(MK_DIR)/src)

LENGTH  ?= 24
SECTION ?=

APP     ?= axpy
SRCS    ?= $(SRC_DIR)/main.c
INCDIRS += $(DATA_DIR) $(SRC_DIR)

DATAGEN_PY = $(DATA_DIR)/datagen.py
DATA_H     = $(DATA_DIR)/data.h

$(DATA_H): $(DATAGEN_PY)
	$< $(LENGTH) --section="$(SECTION)" > $@

.PHONY: clean-data clean

clean-data:
	rm -f $(DATA_H)

clean: clean-data
