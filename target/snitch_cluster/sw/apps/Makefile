# Copyright 2023 ETH Zurich and University of Bologna.
# Licensed under the Apache License, Version 2.0, see LICENSE for details.
# SPDX-License-Identifier: Apache-2.0
#
# Luca Colagrande <colluca@iis.ee.ethz.ch>

SUBDIRS  = lto
SUBDIRS += nop
SUBDIRS += blas/axpy
SUBDIRS += blas/gemm
SUBDIRS += dnn/batchnorm
SUBDIRS += dnn/conv2d
SUBDIRS += dnn/fusedconv
SUBDIRS += dnn/gelu
SUBDIRS += dnn/gemm
SUBDIRS += dnn/layernorm
SUBDIRS += dnn/linear
SUBDIRS += dnn/maxpool
SUBDIRS += dnn/softmax
SUBDIRS += montecarlo/pi_estimation
SUBDIRS += snax-mac
SUBDIRS += snax-mac-simple/untiled
SUBDIRS += snax-mac-simple/tiled
SUBDIRS += snax-gemm-engine
SUBDIRS += snax-gemm-base
SUBDIRS += snax-block-gemm

.PHONY: all clean $(SUBDIRS)

all: $(SUBDIRS)

$(SUBDIRS):
	$(MAKE) -C $@ $(TARGET)
