---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 62beafd5546a52bd8e9cc61fae8ff90f7cd2ed1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902793"
---
# <span data-ttu-id="384b0-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="384b0-101">New-AzSignalR</span></span>

## <span data-ttu-id="384b0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="384b0-102">SYNOPSIS</span></span>
<span data-ttu-id="384b0-103">建立 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="384b0-103">Create a SignalR service.</span></span>

## <span data-ttu-id="384b0-104">語法</span><span class="sxs-lookup"><span data-stu-id="384b0-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="384b0-105">描述</span><span class="sxs-lookup"><span data-stu-id="384b0-105">DESCRIPTION</span></span>
<span data-ttu-id="384b0-106">建立 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="384b0-106">Create a SignalR service.</span></span>
<span data-ttu-id="384b0-107">如果未指定，下列值將會用於參數：</span><span class="sxs-lookup"><span data-stu-id="384b0-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="384b0-108">`ResourceGroupName`：預設資源群組的設定者 `Set-AzDefault -ResourceGroupName` 。</span><span class="sxs-lookup"><span data-stu-id="384b0-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="384b0-109">`Location`：資源群組的位置</span><span class="sxs-lookup"><span data-stu-id="384b0-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="384b0-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="384b0-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="384b0-111">例子</span><span class="sxs-lookup"><span data-stu-id="384b0-111">EXAMPLES</span></span>

### <span data-ttu-id="384b0-112">建立訊號服務</span><span class="sxs-lookup"><span data-stu-id="384b0-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="384b0-113">指定 ServiceMode 和 AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="384b0-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="384b0-114">參數</span><span class="sxs-lookup"><span data-stu-id="384b0-114">PARAMETERS</span></span>

### <span data-ttu-id="384b0-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="384b0-115">-AllowedOrigin</span></span>
<span data-ttu-id="384b0-116">SignalR 服務的允許來源。</span><span class="sxs-lookup"><span data-stu-id="384b0-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="384b0-117">若要允許全部使用，請使用 "\*"，然後從清單中移除所有其他來源。</span><span class="sxs-lookup"><span data-stu-id="384b0-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="384b0-118">不允許斜線做為網域的一部分或 TLD 之後</span><span class="sxs-lookup"><span data-stu-id="384b0-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="384b0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="384b0-119">-AsJob</span></span>
<span data-ttu-id="384b0-120">在背景工作中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="384b0-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="384b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="384b0-121">-DefaultProfile</span></span>
<span data-ttu-id="384b0-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="384b0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="384b0-123">-位置</span><span class="sxs-lookup"><span data-stu-id="384b0-123">-Location</span></span>
<span data-ttu-id="384b0-124">SignalR 服務位置。</span><span class="sxs-lookup"><span data-stu-id="384b0-124">The SignalR service location.</span></span> <span data-ttu-id="384b0-125">如果未指定，將會使用資源群組位置。</span><span class="sxs-lookup"><span data-stu-id="384b0-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="384b0-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="384b0-126">-Name</span></span>
<span data-ttu-id="384b0-127">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="384b0-127">The SignalR service name.</span></span>

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

### <span data-ttu-id="384b0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="384b0-128">-ResourceGroupName</span></span>
<span data-ttu-id="384b0-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="384b0-129">The resource group name.</span></span> <span data-ttu-id="384b0-130">如果沒有指定，將會使用預設選項。</span><span class="sxs-lookup"><span data-stu-id="384b0-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="384b0-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="384b0-131">-ServiceMode</span></span>
<span data-ttu-id="384b0-132">SignalR 服務的服務模式。</span><span class="sxs-lookup"><span data-stu-id="384b0-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="384b0-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="384b0-133">-Sku</span></span>
<span data-ttu-id="384b0-134">SignalR 服務 SKU。</span><span class="sxs-lookup"><span data-stu-id="384b0-134">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="384b0-135">-標記</span><span class="sxs-lookup"><span data-stu-id="384b0-135">-Tag</span></span>
<span data-ttu-id="384b0-136">SignalR 服務的標記。</span><span class="sxs-lookup"><span data-stu-id="384b0-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="384b0-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="384b0-137">-UnitCount</span></span>
<span data-ttu-id="384b0-138">SignalR 服務單位元數目，從 1 到 10。</span><span class="sxs-lookup"><span data-stu-id="384b0-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="384b0-139">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="384b0-139">Default to 1.</span></span>

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

### <span data-ttu-id="384b0-140">-確認</span><span class="sxs-lookup"><span data-stu-id="384b0-140">-Confirm</span></span>
<span data-ttu-id="384b0-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="384b0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="384b0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="384b0-142">-WhatIf</span></span>
<span data-ttu-id="384b0-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="384b0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="384b0-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="384b0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="384b0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384b0-145">CommonParameters</span></span>
<span data-ttu-id="384b0-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="384b0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384b0-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="384b0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384b0-148">輸入</span><span class="sxs-lookup"><span data-stu-id="384b0-148">INPUTS</span></span>

### <span data-ttu-id="384b0-149">System.String</span><span class="sxs-lookup"><span data-stu-id="384b0-149">System.String</span></span>

## <span data-ttu-id="384b0-150">輸出</span><span class="sxs-lookup"><span data-stu-id="384b0-150">OUTPUTS</span></span>

### <span data-ttu-id="384b0-151">Microsoft.Azure.Commands.SignalR.models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="384b0-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="384b0-152">筆記</span><span class="sxs-lookup"><span data-stu-id="384b0-152">NOTES</span></span>

## <span data-ttu-id="384b0-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="384b0-153">RELATED LINKS</span></span>
