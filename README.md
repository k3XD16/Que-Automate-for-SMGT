# Automate Que Ingestion in SMGT

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




