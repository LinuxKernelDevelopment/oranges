SRC:=pmtest4.asm
BIN:=$(subst .asm,.com,$(SRC))

.PHONY : everything

everything : $(BIN)
	mount -o loop pm.img /mnt/floppy/
	cp $(BIN) /mnt/floppy/ -v
	umount /mnt/floppy/

$(BIN) : $(SRC)
	nasm $< -o $@
