#!/usr/bin/awk -f
BEGIN {
	DATA="|";
	CAT = "cat " file;
	while ((CAT | getline) > 0) {
		filter[$0]++
	}
	close(CAT);
}
{
	if (filter[$0]) {
		print "\033[0;34m" " " $0 "\033[0m"
	} else {
		print "\033[0;31m" "-" $0 "\033[0m"
	}
}
