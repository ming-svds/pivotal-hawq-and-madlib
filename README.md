# pivotal-hawq-and-madlib

This document details steps involved in preparing a Pivotal-Hawq and Madlib environment through Docker containers. 

##### Notes:
Where initial goal was to integrate Pivotal Hawq into Cloudera or Hortonworks Data Platform. The following difficulties listed below were quickly discovered that resulted in taking alternative option of using Docker containers. 

###### June 2015
Installation instructions from Pivotal website (http://hawq.docs.pivotal.io/) is out-of-sync with actual content of jars from download links. With most documentations referencing the complete Pivotal HD suite, but no instructions on how to install standalone Hawq.

Take CentOS distribution for example, installation instructions are vague in terms of the base rpm package required. After PADS-1.3.x.x.tar.gz is extracted, execute the provided setup script but encounter list of missing rpm dependencies.   

###### Getting Pivotal HD on Docker
This blog post provides details on obtaining Pivotal HD on Docker with 3 containers. 
http://blog.pivotal.io/pivotal/products/6-easy-steps-deploy-pivotals-hadoop-on-docker

###### Installing Madlib on Pivotal HD
It's interesting on Madlib's official installation page. When it comes to Pivotal HD Section, it indicates to contact Pivotal personnel. (https://github.com/madlib/madlib/wiki/Installation-Guide)

>For the Pivotal HAWQ and Greenplum Database, see your Pivotal account representative >(http://pivotal.io)

Latest Madlib installation doc provided by Pivotal that can be found is dated back in 2010. (http://pivotalhd-210.docs.pivotal.io/doc/2010/InstallingtheHAWQComponents.html#InstallingtheHAWQComponents-InstallingMADlibonHAWQ) 


The install script 'hawq_install.sh' mentioned is no where to be found on Pivotal HD.

> Once HAWQ installation is complete, run the following command to install MADlib:
> hawq_install.sh -r <RPM_FILEPATH> -f <HOSTFILE> [-s] [-d <GPHOME>] [--prefix <MADLIB_INSTALL_PATH>]


