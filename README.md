# -
流通
void KEY_task(void *pvParameters)
{
	BaseType_t err=pdFALSE;
	printf("KEY_task Start......\r\n");
	while(1)
	{
		if(KEY_BS != NULL)
		{
			err = xSemaphoreTake(KEY_BS,portMAX_DELAY);							//»ñÈ¡ÐÅºÅÁ¿
			if(err==pdTRUE)														//»ñÈ¡ÐÅºÅÁ¿³É¹¦
			{
				Key_Mode_Manage();	
			}
		}
	}
}
