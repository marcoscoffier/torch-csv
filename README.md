torch-csv
=========

Reader / Parser of csv files with header

Module to load and parse csv files which uses standard torch
packaging and documentation tools.

Main generator code is copied from:

Tobias Kieslich at 

    http://lua-users.org/lists/lua-l/2009-08/msg00029.html 

REQUIREMENTS:

  git clone https://github.com/andresy/torch.git

INSTALL:

  git clone https://github.com/marcoscoffier/torch-csv.git

  cd torch-csv
  torch-pkg deploy

EXAMPLE:

$torch -lcsv
t7> csvg, header,rheader = csv.open_with_header(fname)
t7> =header
{[1] = string : "bbx"
 [2] = string : "bby"
 [3] = string : "bbw"
 [4] = string : "bbh"}
t7> =rheader
{[bbx]            = 1
 [bby]            = 2
 [bbw]            = 3
 [bbh]            = 4}
t7> line = csvg()
t7> =line[rheader["bbx"]]
34398
