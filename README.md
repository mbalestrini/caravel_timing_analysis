# Caravel timing analysis test 


## Requirements

The caravel repository is needed inside ./caravel folder

You can get it by running `make get_caravel`

The environment variable `PDK_ROOT` must be set to the pdk folder

---

## run the default empty caravel with no user project inside 
`make caravel_sta-empty`

## run some custom user project
`make caravel_sta-[NAME_OF_PROJECT_FOLDER]`

## create a new user project
- Create the folder `/user_projects/[NAME_OF_PROJECT_FOLDER]` (you can duplicate `user_projects/empty` to use as a template)
- Add the extra verilog and spef files you need to `/user_projects/[NAME_OF_PROJECT_FOLDER]`
- Create or modify the script file `/user_projects/[NAME_OF_PROJECT_FOLDER]/caravel_timing-[NAME_OF_PROJECT_FOLDER].tcl` to use the extra files
- The folder `/user_projects/[NAME_OF_PROJECT_FOLDER]` is going to be mapped to `/project_files`, so use that path in the .tcl script to refer to your extra files (ej: read_verilog /project_files/verilog/user_project_wrapper.v)
- Create or modify the SDC file `/user_projects/[NAME_OF_PROJECT_FOLDER]/caravel.sdc`

## results

openSTA log files in `/results/[NAME_OF_PROJECT_FOLDER]` 
