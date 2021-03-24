# **Readme**
>## **How to run Jupyter Notebook on Jackfruit Server**

***

### **Steps to run Jupyter Notebook :**

<div style="text-align: justify">

1. ssh to jackfruit server from your local machine on port 5555 to jackfruit server on port 7777. Do not change the port 7777 because the genomics container is runing on jackfruit server on port 7777. 

```bash
ssh -L 127.0.0.1:5555:0.0.0.0:7777 <username>@jackfruit.iitgoa.ac.in
```

</div>


<div style="text-align: justify">

2. Now start your docker container	 

```bash
docker start genomics
```

</div>


<div style="text-align: justify">

3. Now execute genomics with its pseudo terminal attched to your terminal's stdin and stdout using -it 

```bash
docker exec -it genomics bash
```

</div>

  
<div style="text-align: justify">

4. After this you will see Tensorflow printed on your screen in big font and orange color. After this run below command to start jupyter notebook

```bash
jupyter notebook
```

</div>


<div style="text-align: justify">

5. If there is an error saying Jupyter notebook is already running can't listen on port 8888 then your jupyter notebook is already running on local host just go to browser and type the following address

```
localhost:5555
```


<div style="text-align: justify">

6. Now if after going to that address they ask for token then go back to terminal in your tensorflow console and type following commnd.

```
jupyter notebook list
```

</div>


<div style="text-align: justify">

7. Copy the required token and paste it on your browser where jupyter notebook is running. Now it will open!

</div>

>## Further Queries

For further queries please contact the writer <naresh.kaushal.17003@iitgoa.ac.in>



