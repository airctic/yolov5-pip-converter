# yolov5-pip-converter

The original [yolov5](`https://github.com/ultralytics/yolov5`) project does not provide a pip-installable version. Therefore, we decide to create our fork and make it pip-installable. 

This is our internal procedure to create or re-sync our fork with the original yolov5 repository (https://github.com/ultralytics/yolov5):

- Remove the [yolov5-icevision](https://github.com/airctic/yolov5-icevision) fork from airctic if there is one
- Fork the original `yolov5` repository in airctic: That's what we are calling "our fork". Its name will be `yolov5`
- Clone our fork on a local machine
- Outside the `yolov5` folder, run the script to create a new repo (pip compatible) using: `python from_yolov5repo_to_fork.py yolov5`
- A new repo, called `yolov5-icevision` is separately created: that repo still has its origin pointing to `https://github.com/airctic/yolov5.git`
- Commit all changes, and push them back to origin
- Rename the original repo `yolov5` (located in `https://github.com/airctic/yolov5`) `yolov5-icevision`