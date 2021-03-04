---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 35acbbaeb4983def89711049fc3284a63611bbec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907742"
---
# <span data-ttu-id="f3313-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f3313-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="f3313-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f3313-102">SYNOPSIS</span></span>
<span data-ttu-id="f3313-103">使用 Azure Data Factory 取得所有使用中資料流程的 Debug 會話</span><span class="sxs-lookup"><span data-stu-id="f3313-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="f3313-104">語法</span><span class="sxs-lookup"><span data-stu-id="f3313-104">SYNTAX</span></span>

### <span data-ttu-id="f3313-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="f3313-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3313-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3313-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3313-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f3313-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3313-108">描述</span><span class="sxs-lookup"><span data-stu-id="f3313-108">DESCRIPTION</span></span>
<span data-ttu-id="f3313-109">列出 Azure Data Factory 的所有使用中資料流程 Debug 會話，並包含詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f3313-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="f3313-110">例子</span><span class="sxs-lookup"><span data-stu-id="f3313-110">EXAMPLES</span></span>

### <span data-ttu-id="f3313-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f3313-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="f3313-112">取得 Azure Data Factory "WikiADF" 中所有使用中資料流程的 Debug 會話。</span><span class="sxs-lookup"><span data-stu-id="f3313-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="f3313-113">參數</span><span class="sxs-lookup"><span data-stu-id="f3313-113">PARAMETERS</span></span>

### <span data-ttu-id="f3313-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f3313-114">-DataFactory</span></span>
<span data-ttu-id="f3313-115">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="f3313-115">The data factory object.</span></span>

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

### <span data-ttu-id="f3313-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f3313-116">-DataFactoryName</span></span>
<span data-ttu-id="f3313-117">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="f3313-117">The data factory name.</span></span>

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

### <span data-ttu-id="f3313-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3313-118">-DefaultProfile</span></span>
<span data-ttu-id="f3313-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3313-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3313-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3313-120">-ResourceGroupName</span></span>
<span data-ttu-id="f3313-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f3313-121">The resource group name.</span></span>

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

### <span data-ttu-id="f3313-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3313-122">-ResourceId</span></span>
<span data-ttu-id="f3313-123">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3313-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f3313-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3313-124">CommonParameters</span></span>
<span data-ttu-id="f3313-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f3313-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3313-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3313-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3313-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f3313-127">INPUTS</span></span>

### <span data-ttu-id="f3313-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f3313-128">System.String</span></span>

### <span data-ttu-id="f3313-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f3313-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f3313-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f3313-130">OUTPUTS</span></span>

### <span data-ttu-id="f3313-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDFlowDesessionInfo</span><span class="sxs-lookup"><span data-stu-id="f3313-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="f3313-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f3313-132">NOTES</span></span>
<span data-ttu-id="f3313-133">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="f3313-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f3313-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3313-134">RELATED LINKS</span></span>

[<span data-ttu-id="f3313-135">Start-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="f3313-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="f3313-136">Add-AzDataFactoryV2DataFlowDemediaSessionPackage</span><span class="sxs-lookup"><span data-stu-id="f3313-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="f3313-137">Invoke-AzDataFactoryV2DataFlowDemediaSessionCommand</span><span class="sxs-lookup"><span data-stu-id="f3313-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="f3313-138">Stop-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="f3313-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)