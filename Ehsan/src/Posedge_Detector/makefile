VERILOG_FILES = src/posedge_detector.sv test/tb_posedge_detector.sv
TOP_MODULE = tb
OUTPUT_FILE = simulation.vvp
VCD_FILE = waveform.vcd

IVERILOG = iverilog
VVP = vvp
GTKWAVE = gtkwave

all: compile simulate

install:
	sudo apt install $(IVERILOG)
	sudo apt install $(GTKWAVE)

compile:
	$(IVERILOG) -o $(OUTPUT_FILE) -g2012 $(VERILOG_FILES)
simulate:
	$(VVP) $(OUTPUT_FILE)
view_simulation:
	$(GTKWAVE) $(VCD_FILE)
clean:
	rm -f $(OUTPUT_FILE) $(VCD_FILE)

.PHONY: all compile simulate view clean
