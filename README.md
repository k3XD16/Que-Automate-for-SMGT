# Automate Que Ingestion in SMGT



**Current Scenario:** 
In SMGT we'll are using n number of queues for the task allocation in various programs like **Faces, Tangelo, Labels, Textract, etc.** But every time once the que got completed/over, DA's need to inform POC's then they'll manually ingest new queue for the particular task allocation. So it consume some time while ingesting ques. By that time DA's were also become idle because of the no ques to annotate.

**Solution:** 
To avoid manually ingestion in SMGT, We can try using the script or open source tool to automate the queue ingestion every time the before the previous que got to over. 
For an Example, if there is 1000 hits in a particular que. DA's started using the que by end of the que if there is 900/1000 hits left, we can automate using the script if that que hit less than 100 will automatically ingested next set of que in the SMGT. 
This save lot of time and also improves to achieve DA's Productivity as well as Quality. why because quality, in some day ques were not ingested for long so DA's were idle for long and then queue ingested means they rush to complete the target so it might have some quality misses too.  

**Pseudo Code:** 
<pre><code>
while True: {
        if(status == inprogress){
                //Task_ProdQue == Tasks bucket
                //Prod-task-1 == working que
                if(count(Task_ProdQue.Prod-task-1) <= 100){  
                        // do ingest another queue
                        // Prod-task-2 ingesting         
                        Print("Successfully Ingested 2nd Que!")
                } else if (Task_ProdQue.Prod-task-2) <= 100){
                        // again do ingest another queue
                        // Prod-task-3 ingesting         
                        Print("Successfully Ingested 3rd Que!")                
                }else if (Task_ProdQue != 0){
                        continue:
                }
	} else if (Task_ProdQue == 0){
		break:
                // Particular Task is completed
                }
        Print("script will be exited successfully!")
}
</code></pre>

**Try Power Automate**

It is a open source tool build by Microsoft. It's Pre Installed in Win11 and for Win10 need to install from own [Microsoft store](https://apps.microsoft.com/store/detail/power-automate/9NFTCH6J7FHV?hl=en-us&gl=us).  




