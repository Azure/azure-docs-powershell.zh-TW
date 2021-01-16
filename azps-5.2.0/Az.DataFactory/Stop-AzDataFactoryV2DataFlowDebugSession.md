---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281033"
---
# <span data-ttu-id="bace0-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="bace0-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="bace0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bace0-102">SYNOPSIS</span></span>
<span data-ttu-id="bace0-103">停止 Azure 資料工廠中的資料資料流程調試會話</span><span class="sxs-lookup"><span data-stu-id="bace0-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="bace0-104">句法</span><span class="sxs-lookup"><span data-stu-id="bace0-104">SYNTAX</span></span>

### <span data-ttu-id="bace0-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="bace0-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bace0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bace0-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bace0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bace0-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bace0-108">說明</span><span class="sxs-lookup"><span data-stu-id="bace0-108">DESCRIPTION</span></span>
<span data-ttu-id="bace0-109">這個命令會停止調試會話，如果不是，則會根據調試會話的即時設定，自動關閉會話。</span><span class="sxs-lookup"><span data-stu-id="bace0-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="bace0-110">示例</span><span class="sxs-lookup"><span data-stu-id="bace0-110">EXAMPLES</span></span>

### <span data-ttu-id="bace0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="bace0-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="bace0-112">在資料工廠 "WikiADF" 中停止資料流程程調試會話 "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d"</span><span class="sxs-lookup"><span data-stu-id="bace0-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="bace0-113">參數</span><span class="sxs-lookup"><span data-stu-id="bace0-113">PARAMETERS</span></span>

### <span data-ttu-id="bace0-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bace0-114">-DataFactory</span></span>
<span data-ttu-id="bace0-115">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="bace0-115">The data factory object.</span></span>

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

### <span data-ttu-id="bace0-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bace0-116">-DataFactoryName</span></span>
<span data-ttu-id="bace0-117">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="bace0-117">The data factory name.</span></span>

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

### <span data-ttu-id="bace0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bace0-118">-DefaultProfile</span></span>
<span data-ttu-id="bace0-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bace0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bace0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bace0-120">-PassThru</span></span>
<span data-ttu-id="bace0-121">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="bace0-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="bace0-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="bace0-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="bace0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bace0-123">-ResourceGroupName</span></span>
<span data-ttu-id="bace0-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bace0-124">The resource group name.</span></span>

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

### <span data-ttu-id="bace0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bace0-125">-ResourceId</span></span>
<span data-ttu-id="bace0-126">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bace0-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="bace0-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="bace0-127">-SessionId</span></span>
<span data-ttu-id="bace0-128">資料流程調試會話 ID。</span><span class="sxs-lookup"><span data-stu-id="bace0-128">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bace0-129">-確認</span><span class="sxs-lookup"><span data-stu-id="bace0-129">-Confirm</span></span>
<span data-ttu-id="bace0-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bace0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bace0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bace0-131">-WhatIf</span></span>
<span data-ttu-id="bace0-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bace0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bace0-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bace0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bace0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bace0-134">CommonParameters</span></span>
<span data-ttu-id="bace0-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bace0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bace0-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bace0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bace0-137">輸入</span><span class="sxs-lookup"><span data-stu-id="bace0-137">INPUTS</span></span>

### <span data-ttu-id="bace0-138">System.object</span><span class="sxs-lookup"><span data-stu-id="bace0-138">System.String</span></span>

### <span data-ttu-id="bace0-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bace0-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="bace0-140">輸出</span><span class="sxs-lookup"><span data-stu-id="bace0-140">OUTPUTS</span></span>

### <span data-ttu-id="bace0-141">System.void</span><span class="sxs-lookup"><span data-stu-id="bace0-141">System.Void</span></span>

### <span data-ttu-id="bace0-142">System.object</span><span class="sxs-lookup"><span data-stu-id="bace0-142">System.Boolean</span></span>

## <span data-ttu-id="bace0-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bace0-143">NOTES</span></span>
<span data-ttu-id="bace0-144">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="bace0-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bace0-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="bace0-145">RELATED LINKS</span></span>

[<span data-ttu-id="bace0-146">開始-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="bace0-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="bace0-147">AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="bace0-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="bace0-148">附加 AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="bace0-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="bace0-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="bace0-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)