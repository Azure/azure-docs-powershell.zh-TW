---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436171"
---
# <span data-ttu-id="37949-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="37949-101">New-AzSignalR</span></span>

## <span data-ttu-id="37949-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37949-102">SYNOPSIS</span></span>
<span data-ttu-id="37949-103">建立 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="37949-103">Create a SignalR service.</span></span>

## <span data-ttu-id="37949-104">句法</span><span class="sxs-lookup"><span data-stu-id="37949-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37949-105">說明</span><span class="sxs-lookup"><span data-stu-id="37949-105">DESCRIPTION</span></span>
<span data-ttu-id="37949-106">建立 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="37949-106">Create a SignalR service.</span></span>
<span data-ttu-id="37949-107">如果沒有指定，下列值將用於參數：</span><span class="sxs-lookup"><span data-stu-id="37949-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="37949-108">`ResourceGroupName`：預設資源群組的設定依據 `Set-AzDefault -ResourceGroupName` 。</span><span class="sxs-lookup"><span data-stu-id="37949-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="37949-109">`Location`：資源群組的位置</span><span class="sxs-lookup"><span data-stu-id="37949-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="37949-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="37949-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="37949-111">示例</span><span class="sxs-lookup"><span data-stu-id="37949-111">EXAMPLES</span></span>

### <span data-ttu-id="37949-112">建立 SignalR 服務</span><span class="sxs-lookup"><span data-stu-id="37949-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="37949-113">指定 ServiceMode 和 AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="37949-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="37949-114">參數</span><span class="sxs-lookup"><span data-stu-id="37949-114">PARAMETERS</span></span>

### <span data-ttu-id="37949-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="37949-115">-AllowedOrigin</span></span>
<span data-ttu-id="37949-116">SignalR 服務的允許來源。</span><span class="sxs-lookup"><span data-stu-id="37949-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="37949-117">若要全部允許，請使用 "\*"，然後從清單中移除所有其他來源。</span><span class="sxs-lookup"><span data-stu-id="37949-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="37949-118">不允許使用斜杠作為網域的一部分或在 TLD 之後</span><span class="sxs-lookup"><span data-stu-id="37949-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="37949-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37949-119">-AsJob</span></span>
<span data-ttu-id="37949-120">在背景作業中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37949-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="37949-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37949-121">-DefaultProfile</span></span>
<span data-ttu-id="37949-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37949-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37949-123">-位置</span><span class="sxs-lookup"><span data-stu-id="37949-123">-Location</span></span>
<span data-ttu-id="37949-124">SignalR 服務位置。</span><span class="sxs-lookup"><span data-stu-id="37949-124">The SignalR service location.</span></span> <span data-ttu-id="37949-125">如果沒有指定，則會使用資源群組位置。</span><span class="sxs-lookup"><span data-stu-id="37949-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="37949-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="37949-126">-Name</span></span>
<span data-ttu-id="37949-127">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="37949-127">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37949-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37949-128">-ResourceGroupName</span></span>
<span data-ttu-id="37949-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="37949-129">The resource group name.</span></span> <span data-ttu-id="37949-130">如果沒有指定，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="37949-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="37949-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="37949-131">-ServiceMode</span></span>
<span data-ttu-id="37949-132">SignalR 服務的服務模式。</span><span class="sxs-lookup"><span data-stu-id="37949-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="37949-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="37949-133">-Sku</span></span>
<span data-ttu-id="37949-134">SignalR 服務 SKU。</span><span class="sxs-lookup"><span data-stu-id="37949-134">The SignalR service SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Standard_S1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37949-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="37949-135">-Tag</span></span>
<span data-ttu-id="37949-136">SignalR 服務的標記。</span><span class="sxs-lookup"><span data-stu-id="37949-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="37949-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="37949-137">-UnitCount</span></span>
<span data-ttu-id="37949-138">SignalR 服務單位元數目（1到10）。</span><span class="sxs-lookup"><span data-stu-id="37949-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="37949-139">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="37949-139">Default to 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37949-140">-確認</span><span class="sxs-lookup"><span data-stu-id="37949-140">-Confirm</span></span>
<span data-ttu-id="37949-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="37949-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37949-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37949-142">-WhatIf</span></span>
<span data-ttu-id="37949-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37949-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37949-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37949-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37949-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37949-145">CommonParameters</span></span>
<span data-ttu-id="37949-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37949-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37949-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="37949-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37949-148">輸入</span><span class="sxs-lookup"><span data-stu-id="37949-148">INPUTS</span></span>

### <span data-ttu-id="37949-149">System.object</span><span class="sxs-lookup"><span data-stu-id="37949-149">System.String</span></span>

## <span data-ttu-id="37949-150">輸出</span><span class="sxs-lookup"><span data-stu-id="37949-150">OUTPUTS</span></span>

### <span data-ttu-id="37949-151">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="37949-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="37949-152">筆記</span><span class="sxs-lookup"><span data-stu-id="37949-152">NOTES</span></span>

## <span data-ttu-id="37949-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="37949-153">RELATED LINKS</span></span>
