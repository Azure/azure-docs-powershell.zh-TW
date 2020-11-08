---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 632f271a085df8384a100392e8ed74ad7b5d0762
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971712"
---
# <span data-ttu-id="e8b2a-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="e8b2a-101">Update-AzSignalR</span></span>

## <span data-ttu-id="e8b2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b2a-103">更新 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-103">Update a SignalR service.</span></span>

## <span data-ttu-id="e8b2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8b2a-104">SYNTAX</span></span>

### <span data-ttu-id="e8b2a-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e8b2a-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8b2a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8b2a-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8b2a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8b2a-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8b2a-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8b2a-108">DESCRIPTION</span></span>
<span data-ttu-id="e8b2a-109">更新 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-109">Update a SignalR service.</span></span>
<span data-ttu-id="e8b2a-110">如果沒有指定，下列值將用於參數：</span><span class="sxs-lookup"><span data-stu-id="e8b2a-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="e8b2a-111">`ResourceGroupName`：預設資源群組的設定依據 `Set-AzDefault -ResourceGroupName` 。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="e8b2a-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="e8b2a-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="e8b2a-113">示例</span><span class="sxs-lookup"><span data-stu-id="e8b2a-113">EXAMPLES</span></span>

### <span data-ttu-id="e8b2a-114">更新特定的 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="e8b2a-115">指定 ServiceMode 和 AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="e8b2a-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="e8b2a-116">參數</span><span class="sxs-lookup"><span data-stu-id="e8b2a-116">PARAMETERS</span></span>

### <span data-ttu-id="e8b2a-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="e8b2a-117">-AllowedOrigin</span></span>
<span data-ttu-id="e8b2a-118">SignalR 服務的允許來源。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="e8b2a-119">若要全部允許，請使用 "\*"，然後從清單中移除所有其他來源。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="e8b2a-120">不允許使用斜杠作為網域的一部分或在 TLD 之後</span><span class="sxs-lookup"><span data-stu-id="e8b2a-120">Slashes are not allowed as part of domain or after TLD</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b2a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8b2a-121">-AsJob</span></span>
<span data-ttu-id="e8b2a-122">在背景作業中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="e8b2a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b2a-123">-DefaultProfile</span></span>
<span data-ttu-id="e8b2a-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8b2a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8b2a-125">-InputObject</span></span>
<span data-ttu-id="e8b2a-126">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-126">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b2a-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8b2a-127">-Name</span></span>
<span data-ttu-id="e8b2a-128">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-128">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b2a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8b2a-129">-ResourceGroupName</span></span>
<span data-ttu-id="e8b2a-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-130">The resource group name.</span></span>
<span data-ttu-id="e8b2a-131">如果沒有指定，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-131">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b2a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8b2a-132">-ResourceId</span></span>
<span data-ttu-id="e8b2a-133">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b2a-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="e8b2a-134">-ServiceMode</span></span>
<span data-ttu-id="e8b2a-135">SignalR 服務的服務模式。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-135">The service mode for the SignalR service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b2a-136">-Sku</span><span class="sxs-lookup"><span data-stu-id="e8b2a-136">-Sku</span></span>
<span data-ttu-id="e8b2a-137">SignalR 服務 SKU。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-137">The SignalR service SKU.</span></span>
<span data-ttu-id="e8b2a-138">預設為 [Standard_S1]。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-138">Default to "Standard_S1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b2a-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8b2a-139">-Tag</span></span>
<span data-ttu-id="e8b2a-140">SignalR 服務的標記。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-140">The tags for the SignalR service.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b2a-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="e8b2a-141">-UnitCount</span></span>
<span data-ttu-id="e8b2a-142">SignalR 服務單位元數目，僅限 {1，2，5，10，20，50，100} 的值。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="e8b2a-143">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-143">Default to 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b2a-144">-確認</span><span class="sxs-lookup"><span data-stu-id="e8b2a-144">-Confirm</span></span>
<span data-ttu-id="e8b2a-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8b2a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8b2a-146">-WhatIf</span></span>
<span data-ttu-id="e8b2a-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8b2a-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8b2a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b2a-149">CommonParameters</span></span>
<span data-ttu-id="e8b2a-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b2a-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b2a-152">輸入</span><span class="sxs-lookup"><span data-stu-id="e8b2a-152">INPUTS</span></span>

### <span data-ttu-id="e8b2a-153">System.object</span><span class="sxs-lookup"><span data-stu-id="e8b2a-153">System.String</span></span>

### <span data-ttu-id="e8b2a-154">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="e8b2a-155">輸出</span><span class="sxs-lookup"><span data-stu-id="e8b2a-155">OUTPUTS</span></span>

### <span data-ttu-id="e8b2a-156">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="e8b2a-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="e8b2a-157">筆記</span><span class="sxs-lookup"><span data-stu-id="e8b2a-157">NOTES</span></span>

## <span data-ttu-id="e8b2a-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8b2a-158">RELATED LINKS</span></span>
