# Planetary Pro

开发团队：洪秋鑫（独立开发者）、刘智业（西南大学）、李姗姗*（广东财经大学）

*李姗姗博士为项目的指导与通讯。

Development Team: Qiuxin Hong (Independent developer), Zhiye Liu (Southwest University), Shanshan Li * (Guangdong University of Finance and Economics)

*Dr. Shanshan Li is the project's director and communications.

## 项目简介 Project Overview

Planetary Pro是一款依托遥感云计算平台的软件，用于快速导出影像和进行区域统计，为不愿学习或使用编程的研究人员提供便利。

Planetary Pro is a software designed for rapid image export and regional statistics, leveraging remote sensing cloud computing platforms. It caters to researchers who prefer not to learn or use programming. 

Planetary Pro是一款免费的非盈利产品，在使用过程中不收取任何费用，并且不为商用产品。

Planetary Pro is a free, non-profit product that doesn't charge any fees during use. It is **NOT** intended for commercial purposes.

**Planetary Pro目前处于公众测试阶段。**

**Planetary Pro is currently in public beta testing.**

## 功能特性 Features

软件主要提供两大功能：
1. **影像导出功能** - 根据查询条件从遥感云平台中筛选影像，内置影像裁剪等基础模块，直接导出研究区域内的即用影像。
2. **影像统计功能** - 直接统计研究区域内影像产品信息，不需要下载影像后再执行影像统计。

The software has two main functions:
1. **Export Image** - Filter images from remote sensing cloud platforms based on query criteria. Built-in modules for image cropping and other basic operations allow direct export of ready-to-use images for the study area.
2. **Zonal Statistics** - Directly compute statistics for image products in the study area without the need to download images first.


软件目前支持40+款遥感产品。

The software currently supports 40+ products.

## 安装指南 Installation Guide

### 1. Windows
软件提供Windows安装包，安装后在目录中查找 **planetarypro.exe** ，打开后即可使用。如果用户在桌面或者开始菜单中创建了快捷方式，那么点击快捷方式即可使用。

A Windows installation package is provided. After installation, locate and run **planetarypro.exe** in the installation directory. If shortcuts were created on the desktop or in the Start menu, you can launch the software by clicking these shortcuts.

软件卸载可在设置中进行卸载。

To uninstall the software, use the Windows Settings.

### 2. Liunx
软件的Liunx版本处于内部测试阶段，即将进入公众测试阶段，敬请期待。

The Linux version is currently undergoing internal testing and will soon enter public beta. Stay tuned!

### 3. MacOS
软件的MacOS版本处于内部测试阶段，即将进入公众测试阶段，敬请期待。

The MacOS version is currently undergoing internal testing and will soon enter public beta. Stay tuned!

## 使用说明 User Guide
软件提供四种类型的数据产品，每种类型下有不同的二级分类和数据产品，总共支持40+款数据产品。

The software offers 4 types of data products, with different secondary classifications and data products under each tab, supporting 40+ data products in total.

用户可以根据以下步骤进行 **导出影像**：
1. （必选）Choose Imagery：用户根据需要选择Dataset，即导出的影像产品。Dataset根据用户选择的Classification而不同，而Classification根据用户选择的数据类型而不同。
2. （必选）Filter Region：定义感兴趣区，用户可以通过shp文件或手动输入研究区域的四至来进行下载。其中，shp文件必须为面要素文件。
3. （必选）Filter Time：用户根据需要筛选导出影像产品的时间。超出影像产品时间，会出现查询影像数为0或者查询失败等问题。
4. （必选）Download Options：下载方式，默认为中位数影像。选择中位数影像将导出所有时间段的中位数影像（一幅含多波段的影像），选择所有影像将导出查询到的所有影像（多幅含多波段的影像）。
5. （可选）Filter Cloud Coverage：当用户选择光学遥感时，可以筛选含云量少于指定参数的影像。其他类型影像不受该字段影响。

Users can follow these steps to **Export Images**:
1. (Required) Choose Imagery: Select the Dataset to export. Available Datasets vary based on the chosen Classification, which in turn depends on the selected data type.
2. (Required) Filter Region: Define the area of interest. Users can download based on a shapefile or by manually inputting the study area's bounding box. Note that shapefiles must contain polygon features.
3. (Required) Filter Time: Select the time range. Querying outside the product's available time range may result in 0 images found or query failures.
4. (Required) Download Options: Choose the download method, defaulting to median imagery. Selecting median imagery will export the median image for the entire time range (single multi-band image), while selecting all images will export all queried images (multiple multi-band images).
5. (Optional) Filter Cloud Coverage: When selecting optical remote sensing data, users can filter images with less than a specified cloud cover percentage. This field doesn't affect other types of imagery.


用户可以根据以下步骤进行 **导出统计值**：
1. （必选）Choose Imagery：用户根据需要选择Dataset，即导出的影像产品。Dataset根据用户选择的Classification而不同，而Classification根据用户选择的数据类型而不同。
2. （必选）Filter Region：定义感兴趣区，用户可以通过shp文件或手动输入研究区域的四至来进行下载。其中，shp文件必须为面要素文件。
3. （必选）Filter Time：用户根据需要筛选导出影像产品的时间。超出影像产品时间，会出现查询影像数为0或者查询失败等问题。
4. （必选）Statistical Parameters：用户根据需要选择导出区域内的统计参数，该字段仅在Export Statistics中生效。不选择参数将会导出空表。
5. （可选）Filter Cloud Coverage：当用户选择光学遥感时，可以筛选含云量少于指定参数的影像。其他类型影像不受该字段影响。

Users can follow these steps to **Export Statistics**:
1. (Required) Choose Imagery: Select the Dataset to analyze. Available Datasets vary based on the chosen Classification, which in turn depends on the selected data type.
2. (Required) Filter Region: Define the area of interest. Users can analyze based on a shapefile or by manually inputting the study area's bounding box. Note that shapefiles must contain polygon features.
3. (Required) Filter Time: Select the time range. Querying outside the product's available time range may result in zero images found or query failures.
4. (Required) Statistical Parameters: Select the statistical parameters to export for the region. This field is only effective in the Export Statistics function. Not selecting any parameters will result in an empty table.
5. (Optional) Filter Cloud Coverage: When selecting optical remote sensing data, users can filter images with less than a specified cloud cover percentage. This field doesn't affect other types of imagery.

注意：如果Choose Imagery、Filter Region和Filter Time中任一处出现缺失值，导出功能将失效。

Note: If any required field (Choose Imagery, Filter Region, or Filter Time) is left empty, the export function will be disabled.

注意：为了保护遥感云计算服务器，单次下载的数据量会受到限制，并且两次下载期间会有30秒的冷却时间。

Note: To protect the cloud servers, there are limits on the amount of data that can be downloaded in a session, and a 30-second cooldown period between downloads.


## 免责申明 Disclaimer
免责申明: 
1. 软件目前处于公众测试阶段，可能由于设备或系统不同而出现Bug或兼容性问题。
2. 软件定位为免费非盈利产品，不进行商用，不产生盈利。用户将软件用于学习外的其他用途，开发者不承担相关或者连带责任。
3. 软件仅提供基础服务，用户需要自行检验结果的准确性，开发者不对导出结果或者进一步的产出进行负责。

Disclaimer:
1. The software is currently in public beta testing and may experience bugs or compatibility issues due to varying devices and systems.
2. This software is positioned as a free, non-profit product and is not intended for commercial use or profit generation. The developers are not responsible for any related or consequential liabilities if users employ the software for purposes other than learning.
3. The software provides only basic services. Users are responsible for verifying the accuracy of the results. The developers are not liable for exported results or any further outputs.

## 联系方式 Contact Information
如果您对项目或软件有任何问题和建议,欢迎在GitHub的issue中提出,或通过邮件联系 geohqx@outlook.com 。

If you have any questions or suggestions about the project or software, please feel free to raise an issue or contact us via geohqx@outlook.com.

