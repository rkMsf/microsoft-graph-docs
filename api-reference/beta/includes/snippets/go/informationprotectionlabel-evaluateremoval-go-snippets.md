---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := msgraphsdk.New()
contentInfo := msgraphsdk.NewContentInfo()
requestBody.SetContentInfo(contentInfo)
format := "default"
contentInfo.SetFormat(&format)
contentInfo.SetIdentifier(nil)
state := "rest"
contentInfo.SetState(&state)
contentInfo.SetMetadata( []KeyValuePair {
	msgraphsdk.NewKeyValuePair(),
	SetAdditionalData(map[string]interface{}{
		"@odata.type": "#microsoft.graph.keyValuePair",
		"name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Enabled",
		"value": "True",
	}
	msgraphsdk.NewKeyValuePair(),
	SetAdditionalData(map[string]interface{}{
		"@odata.type": "#microsoft.graph.keyValuePair",
		"name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Method",
		"value": "Standard",
	}
	msgraphsdk.NewKeyValuePair(),
	SetAdditionalData(map[string]interface{}{
		"@odata.type": "#microsoft.graph.keyValuePair",
		"name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SetDate",
		"value": "1/1/0001 12:00:00 AM",
	}
	msgraphsdk.NewKeyValuePair(),
	SetAdditionalData(map[string]interface{}{
		"@odata.type": "#microsoft.graph.keyValuePair",
		"name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SiteId",
		"value": "cfa4cf1d-a337-4481-aa99-19d8f3d63f7c",
	}
	msgraphsdk.NewKeyValuePair(),
	SetAdditionalData(map[string]interface{}{
		"@odata.type": "#microsoft.graph.keyValuePair",
		"name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Name",
		"value": "General",
	}
	msgraphsdk.NewKeyValuePair(),
	SetAdditionalData(map[string]interface{}{
		"@odata.type": "#microsoft.graph.keyValuePair",
		"name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ContentBits",
		"value": "0",
	}
	msgraphsdk.NewKeyValuePair(),
	SetAdditionalData(map[string]interface{}{
		"@odata.type": "#microsoft.graph.keyValuePair",
		"name": "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ActionId",
		"value": "00000000-0000-0000-0000-000000000000",
	}
}
contentInfo.SetAdditionalData(map[string]interface{}{
	"@odata.type": "#microsoft.graph.contentInfo",
	"format@odata.type": "#microsoft.graph.contentFormat",
	"state@odata.type": "#microsoft.graph.contentState",
	"metadata@odata.type": "#Collection(microsoft.graph.keyValuePair)",
}
downgradeJustification := msgraphsdk.NewDowngradeJustification()
requestBody.SetDowngradeJustification(downgradeJustification)
justificationMessage := "The information has been declassified."
downgradeJustification.SetJustificationMessage(&justificationMessage)
isDowngradeJustified := true
downgradeJustification.SetIsDowngradeJustified(&isDowngradeJustified)
headers := map[string]string{
	"User-Agent": "ContosoLOBApp/1.0"
}
options := &msgraphsdk.EvaluateRemovalRequestBuilderPostOptions{
	Body: requestBody,
	H: headers,
}
result, err := graphClient.InformationProtection().Policy().Labels().EvaluateRemoval().Post(options)


```