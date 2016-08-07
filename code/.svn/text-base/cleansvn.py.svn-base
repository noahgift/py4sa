#!/usr/bin/env python
#recursively cleans .svn directories from path

import os
import optparse
import shutil

def clean_tree(path):
	for root, dir, files in os.walk(path):
		for d in dir:
			if ".svn" in d:
				shutil.rmtree(os.path.join(root,d))

def main():
	p = optparse.OptionParser(description="Cleans .svn files from path")
	options, arguments = p.parse_args()
	if len(arguments) == 1:
		clean_tree(arguments[0])
	else:
		p.print_help()

if __name__ == "__main__":
	main()	
	



