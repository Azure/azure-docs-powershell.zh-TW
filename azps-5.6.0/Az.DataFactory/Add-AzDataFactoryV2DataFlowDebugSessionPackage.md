---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: 185f01f31f8cae62e51b7b28909f66fbf37884e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912426"
---
# <span data-ttu-id="cbf70-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="cbf70-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="cbf70-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cbf70-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf70-103">將資料流程資源及其相依性新增到特定的資料流程 Debug 會話。</span><span class="sxs-lookup"><span data-stu-id="cbf70-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="cbf70-104">語法</span><span class="sxs-lookup"><span data-stu-id="cbf70-104">SYNTAX</span></span>

### <span data-ttu-id="cbf70-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="cbf70-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbf70-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cbf70-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbf70-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cbf70-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbf70-108">描述</span><span class="sxs-lookup"><span data-stu-id="cbf70-108">DESCRIPTION</span></span>
<span data-ttu-id="cbf70-109">此命令會將資料流程資源及其相依性附加到特定的 Debug 會話：資料流程的工作流程的 PowerShell 命令順序應該是：</span><span class="sxs-lookup"><span data-stu-id="cbf70-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="cbf70-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cbf70-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="cbf70-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="cbf70-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="cbf70-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (不同命令/目標重複此步驟，或重複步驟 2-3，以變更封裝) </span><span class="sxs-lookup"><span data-stu-id="cbf70-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="cbf70-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cbf70-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="cbf70-114">例子</span><span class="sxs-lookup"><span data-stu-id="cbf70-114">EXAMPLES</span></span>

### <span data-ttu-id="cbf70-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="cbf70-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="cbf70-116">將資料流程套件新增到 "WikiADF" 資料工廠的 "550effe4-93a3-485c-8525-eaf25259efbd" 的 Debug 會話。</span><span class="sxs-lookup"><span data-stu-id="cbf70-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="cbf70-117">Pakcage 檔案包含資料流程的 Debug 資源、資料集的查詢清單、連結的服務 Debug 資源清單、Debug 設定和會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf70-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="cbf70-118">例如：</span><span class="sxs-lookup"><span data-stu-id="cbf70-118">For instance:</span></span>

<span data-ttu-id="cbf70-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource (output (\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t) ,\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=HTTPs;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } ]， "debugSettings"： { "sourceSettings"： [ { "sourceName"： "source1"， "rowLimit"： 1000 } ] }， "sessionId"： "4f988caf-e765-47d2-82cd-430334a6b135" }</span><span class="sxs-lookup"><span data-stu-id="cbf70-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="cbf70-120">SessionID 參數用來取代套件檔案中現有的 sessionId 屬性。</span><span class="sxs-lookup"><span data-stu-id="cbf70-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="cbf70-121">參數</span><span class="sxs-lookup"><span data-stu-id="cbf70-121">PARAMETERS</span></span>

### <span data-ttu-id="cbf70-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cbf70-122">-DataFactory</span></span>
<span data-ttu-id="cbf70-123">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="cbf70-123">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf70-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cbf70-124">-DataFactoryName</span></span>
<span data-ttu-id="cbf70-125">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="cbf70-125">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf70-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf70-126">-DefaultProfile</span></span>
<span data-ttu-id="cbf70-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbf70-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf70-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="cbf70-128">-PackageFile</span></span>
<span data-ttu-id="cbf70-129">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="cbf70-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf70-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbf70-130">-PassThru</span></span>
<span data-ttu-id="cbf70-131">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="cbf70-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="cbf70-132">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="cbf70-132">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf70-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf70-133">-ResourceGroupName</span></span>
<span data-ttu-id="cbf70-134">資源組名。</span><span class="sxs-lookup"><span data-stu-id="cbf70-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf70-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbf70-135">-ResourceId</span></span>
<span data-ttu-id="cbf70-136">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbf70-136">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf70-137">-確認</span><span class="sxs-lookup"><span data-stu-id="cbf70-137">-Confirm</span></span>
<span data-ttu-id="cbf70-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cbf70-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf70-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbf70-139">-WhatIf</span></span>
<span data-ttu-id="cbf70-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cbf70-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbf70-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbf70-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf70-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf70-142">CommonParameters</span></span>
<span data-ttu-id="cbf70-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cbf70-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf70-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbf70-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf70-145">輸入</span><span class="sxs-lookup"><span data-stu-id="cbf70-145">INPUTS</span></span>

### <span data-ttu-id="cbf70-146">System.String</span><span class="sxs-lookup"><span data-stu-id="cbf70-146">System.String</span></span>

### <span data-ttu-id="cbf70-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cbf70-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="cbf70-148">輸出</span><span class="sxs-lookup"><span data-stu-id="cbf70-148">OUTPUTS</span></span>

### <span data-ttu-id="cbf70-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="cbf70-149">System.Void</span></span>

### <span data-ttu-id="cbf70-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbf70-150">System.Boolean</span></span>

## <span data-ttu-id="cbf70-151">筆記</span><span class="sxs-lookup"><span data-stu-id="cbf70-151">NOTES</span></span>
<span data-ttu-id="cbf70-152">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="cbf70-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cbf70-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbf70-153">RELATED LINKS</span></span>

[<span data-ttu-id="cbf70-154">Start-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="cbf70-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="cbf70-155">Get-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="cbf70-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="cbf70-156">Invoke-AzDataFactoryV2DataFlowDemediaSessionCommand</span><span class="sxs-lookup"><span data-stu-id="cbf70-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="cbf70-157">Stop-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="cbf70-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
