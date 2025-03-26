`/dev` (Virtual Device Interface)

- A virtual [[file systems]] that represents hardware devices as files.
- Allows de OS to interact with hardware devices using standard file operations.

- Common Device Files:

- `/dev/sda`, `/dev/sdb`, etc. : Represents hard disk drives.
- `/dev/cdrom` : Represents a CD-ROM drive.
- `/dev/ttyUSB0`, `/dev/ttyUSB1`, etc. : Represents USB [serial ports](https://en.wikipedia.org/wiki/Serial_port)
- `/dev/null` : A special file that discards any data written to it.
- `/dev/zero`: A special file that produces an infinite stream of zeros.