---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 1521f0f4f3b90010e24185a036dca047860e27c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613005"
---
# <span data-ttu-id="47298-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="47298-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="47298-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47298-102">SYNOPSIS</span></span>
<span data-ttu-id="47298-103">透過 Azure 資料工廠取得所有活動的資料流程程調試會話</span><span class="sxs-lookup"><span data-stu-id="47298-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="47298-104">句法</span><span class="sxs-lookup"><span data-stu-id="47298-104">SYNTAX</span></span>

### <span data-ttu-id="47298-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="47298-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47298-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="47298-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47298-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="47298-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47298-108">說明</span><span class="sxs-lookup"><span data-stu-id="47298-108">DESCRIPTION</span></span>
<span data-ttu-id="47298-109">使用詳細資料列出 Azure 資料工廠中的所有活動資料流程調試會話。</span><span class="sxs-lookup"><span data-stu-id="47298-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="47298-110">示例</span><span class="sxs-lookup"><span data-stu-id="47298-110">EXAMPLES</span></span>

### <span data-ttu-id="47298-111">範例1</span><span class="sxs-lookup"><span data-stu-id="47298-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="47298-112">在 Azure 資料工廠 "WikiADF" 中取得所有活動的資料流程調試會話。</span><span class="sxs-lookup"><span data-stu-id="47298-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="47298-113">參數</span><span class="sxs-lookup"><span data-stu-id="47298-113">PARAMETERS</span></span>

### <span data-ttu-id="47298-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="47298-114">-DataFactory</span></span>
<span data-ttu-id="47298-115">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="47298-115">The data factory object.</span></span>

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

### <span data-ttu-id="47298-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="47298-116">-DataFactoryName</span></span>
<span data-ttu-id="47298-117">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="47298-117">The data factory name.</span></span>

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

### <span data-ttu-id="47298-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47298-118">-DefaultProfile</span></span>
<span data-ttu-id="47298-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47298-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47298-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47298-120">-ResourceGroupName</span></span>
<span data-ttu-id="47298-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="47298-121">The resource group name.</span></span>

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

### <span data-ttu-id="47298-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47298-122">-ResourceId</span></span>
<span data-ttu-id="47298-123">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="47298-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="47298-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47298-124">CommonParameters</span></span>
<span data-ttu-id="47298-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47298-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47298-126">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="47298-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47298-127">輸入</span><span class="sxs-lookup"><span data-stu-id="47298-127">INPUTS</span></span>

### <span data-ttu-id="47298-128">System.object</span><span class="sxs-lookup"><span data-stu-id="47298-128">System.String</span></span>

### <span data-ttu-id="47298-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="47298-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="47298-130">輸出</span><span class="sxs-lookup"><span data-stu-id="47298-130">OUTPUTS</span></span>

### <span data-ttu-id="47298-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="47298-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="47298-132">筆記</span><span class="sxs-lookup"><span data-stu-id="47298-132">NOTES</span></span>
<span data-ttu-id="47298-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="47298-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="47298-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="47298-134">RELATED LINKS</span></span>

[<span data-ttu-id="47298-135">開始-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="47298-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="47298-136">附加 AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="47298-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="47298-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="47298-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="47298-138">停止 AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="47298-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)