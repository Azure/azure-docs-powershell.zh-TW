---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 21c8d30cfeec7e0138ec659074a94bd5914e5124
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916185"
---
# <span data-ttu-id="bec0f-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="bec0f-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="bec0f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bec0f-102">SYNOPSIS</span></span>
<span data-ttu-id="bec0f-103">在 Azure Data Factory 中停止資料流程的 Debug 會話</span><span class="sxs-lookup"><span data-stu-id="bec0f-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="bec0f-104">語法</span><span class="sxs-lookup"><span data-stu-id="bec0f-104">SYNTAX</span></span>

### <span data-ttu-id="bec0f-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="bec0f-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bec0f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bec0f-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec0f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bec0f-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec0f-108">描述</span><span class="sxs-lookup"><span data-stu-id="bec0f-108">DESCRIPTION</span></span>
<span data-ttu-id="bec0f-109">此命令會停止 Debug 會話，如果沒有的話，系統就會根據該 Debug 會話的 Time To Live 設定自動關閉會話。</span><span class="sxs-lookup"><span data-stu-id="bec0f-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="bec0f-110">例子</span><span class="sxs-lookup"><span data-stu-id="bec0f-110">EXAMPLES</span></span>

### <span data-ttu-id="bec0f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bec0f-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="bec0f-112">在資料工廠 "WikiADF" 中停止資料流程的 「fd76cd0d-8b37-4dc0-a370-3f9d43ac686d」</span><span class="sxs-lookup"><span data-stu-id="bec0f-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="bec0f-113">參數</span><span class="sxs-lookup"><span data-stu-id="bec0f-113">PARAMETERS</span></span>

### <span data-ttu-id="bec0f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bec0f-114">-DataFactory</span></span>
<span data-ttu-id="bec0f-115">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="bec0f-115">The data factory object.</span></span>

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

### <span data-ttu-id="bec0f-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bec0f-116">-DataFactoryName</span></span>
<span data-ttu-id="bec0f-117">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="bec0f-117">The data factory name.</span></span>

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

### <span data-ttu-id="bec0f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec0f-118">-DefaultProfile</span></span>
<span data-ttu-id="bec0f-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bec0f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bec0f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bec0f-120">-PassThru</span></span>
<span data-ttu-id="bec0f-121">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="bec0f-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="bec0f-122">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bec0f-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="bec0f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec0f-123">-ResourceGroupName</span></span>
<span data-ttu-id="bec0f-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="bec0f-124">The resource group name.</span></span>

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

### <span data-ttu-id="bec0f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bec0f-125">-ResourceId</span></span>
<span data-ttu-id="bec0f-126">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bec0f-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="bec0f-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="bec0f-127">-SessionId</span></span>
<span data-ttu-id="bec0f-128">資料流程的 Debug 會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="bec0f-128">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="bec0f-129">-確認</span><span class="sxs-lookup"><span data-stu-id="bec0f-129">-Confirm</span></span>
<span data-ttu-id="bec0f-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bec0f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec0f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec0f-131">-WhatIf</span></span>
<span data-ttu-id="bec0f-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bec0f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec0f-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bec0f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec0f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec0f-134">CommonParameters</span></span>
<span data-ttu-id="bec0f-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bec0f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec0f-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bec0f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec0f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="bec0f-137">INPUTS</span></span>

### <span data-ttu-id="bec0f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bec0f-138">System.String</span></span>

### <span data-ttu-id="bec0f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bec0f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="bec0f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="bec0f-140">OUTPUTS</span></span>

### <span data-ttu-id="bec0f-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="bec0f-141">System.Void</span></span>

### <span data-ttu-id="bec0f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bec0f-142">System.Boolean</span></span>

## <span data-ttu-id="bec0f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bec0f-143">NOTES</span></span>
<span data-ttu-id="bec0f-144">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="bec0f-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bec0f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="bec0f-145">RELATED LINKS</span></span>

[<span data-ttu-id="bec0f-146">Start-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="bec0f-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="bec0f-147">Get-AzDataFactoryV2DataFlowDemediaSession</span><span class="sxs-lookup"><span data-stu-id="bec0f-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="bec0f-148">Add-AzDataFactoryV2DataFlowDemediaSessionPackage</span><span class="sxs-lookup"><span data-stu-id="bec0f-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="bec0f-149">Invoke-AzDataFactoryV2DataFlowDemediaSessionCommand</span><span class="sxs-lookup"><span data-stu-id="bec0f-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)