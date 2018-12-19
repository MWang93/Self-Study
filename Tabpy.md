1. Download Tabpy from https://github.com/tableau/TabPy
2. Unzip Tabpy file, run setup.sh, it will automatically download and install Anaconda, activate the environment, install dependencies, start server, after you see the “Web service listening on 0.0.0.0 port 9004”, which means initializing TabPy successfully. Then you could open localhost:9004 and see a big Tableau icon, Now you are good to go! 
3. Open jupyter notebook, write a simple function and deploy it to Tabpy server, You can open localhost:9004/endspoints to check the deployed ‘add’ python functions(or models) on Tabpy server.
4. Open a Tableau desktop
	  
    ```Create a calculation field: SCRIPT_REAL("return tabpy.query('add',_arg1,_arg2)['response’]”,[A],[B])```
	  
    A, B are the columns or parameters, SCRIPT_REAL means the returned values is numeric.

5. Then finish!
6. You can also embed python script directly in calculation rather than deploy them to Tabpy server. There’re some examples: https://www.tableau.com/about/blog/2018/8/working-external-services-tableau-tabpy-r-matlab-93351
7. Useful Resources
  - Tableau community(Tableau integration with Python -Step by Step) https://community.tableau.com/thread/236479
  - Forecast example: https://www.clearpeaks.com/tableau-python/
  - Advanced example: https://www.tableau.com/about/blog/2017/1/building-advanced-analytics-applications-tabpy-64916
  - Work with external service in Tableau: https://www.tableau.com/about/blog/2018/8/working-external-services-tableau-tabpy-r-matlab-93351


