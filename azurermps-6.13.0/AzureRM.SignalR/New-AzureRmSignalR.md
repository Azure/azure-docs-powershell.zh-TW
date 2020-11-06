---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
ms.openlocfilehash: d5b7e5480ea3078dadf5280b4f683280dcd00ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449722"
---
# <span data-ttu-id="55baf-101">New-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="55baf-101">New-AzureRmSignalR</span></span>

## <span data-ttu-id="55baf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55baf-102">SYNOPSIS</span></span>
<span data-ttu-id="55baf-103">建立 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="55baf-103">Create a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55baf-104">句法</span><span class="sxs-lookup"><span data-stu-id="55baf-104">SYNTAX</span></span>

```
New-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55baf-105">說明</span><span class="sxs-lookup"><span data-stu-id="55baf-105">DESCRIPTION</span></span>
<span data-ttu-id="55baf-106">建立 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="55baf-106">Create a SignalR service.</span></span>
<span data-ttu-id="55baf-107">如果沒有指定，下列值將用於參數：</span><span class="sxs-lookup"><span data-stu-id="55baf-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="55baf-108">`ResourceGroupName`：預設資源群組的設定依據 `Set-AzureRmDefault -ResourceGroupName` 。</span><span class="sxs-lookup"><span data-stu-id="55baf-108">`ResourceGroupName`: the default resource group set by `Set-AzureRmDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="55baf-109">`Location`：資源群組的位置</span><span class="sxs-lookup"><span data-stu-id="55baf-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="55baf-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="55baf-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="55baf-111">示例</span><span class="sxs-lookup"><span data-stu-id="55baf-111">EXAMPLES</span></span>

### <span data-ttu-id="55baf-112">建立 SignalR 的</span><span class="sxs-lookup"><span data-stu-id="55baf-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzureRmSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="55baf-113">參數</span><span class="sxs-lookup"><span data-stu-id="55baf-113">PARAMETERS</span></span>

### <span data-ttu-id="55baf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55baf-114">-AsJob</span></span>
<span data-ttu-id="55baf-115">在背景作業中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55baf-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="55baf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55baf-116">-DefaultProfile</span></span>
<span data-ttu-id="55baf-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55baf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55baf-118">-位置</span><span class="sxs-lookup"><span data-stu-id="55baf-118">-Location</span></span>
<span data-ttu-id="55baf-119">SignalR 服務位置。</span><span class="sxs-lookup"><span data-stu-id="55baf-119">The SignalR service location.</span></span> <span data-ttu-id="55baf-120">如果沒有指定，則會使用資源群組位置。</span><span class="sxs-lookup"><span data-stu-id="55baf-120">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="55baf-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="55baf-121">-Name</span></span>
<span data-ttu-id="55baf-122">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="55baf-122">The SignalR service name.</span></span>

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

### <span data-ttu-id="55baf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55baf-123">-ResourceGroupName</span></span>
<span data-ttu-id="55baf-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55baf-124">The resource group name.</span></span> <span data-ttu-id="55baf-125">如果沒有指定，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="55baf-125">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="55baf-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="55baf-126">-Sku</span></span>
<span data-ttu-id="55baf-127">SignalR 服務 SKU。</span><span class="sxs-lookup"><span data-stu-id="55baf-127">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="55baf-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="55baf-128">-Tag</span></span>
<span data-ttu-id="55baf-129">SignalR 服務的標記。</span><span class="sxs-lookup"><span data-stu-id="55baf-129">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="55baf-130">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="55baf-130">-UnitCount</span></span>
<span data-ttu-id="55baf-131">SignalR 服務單位元數目（1到10）。</span><span class="sxs-lookup"><span data-stu-id="55baf-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="55baf-132">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="55baf-132">Default to 1.</span></span>

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

### <span data-ttu-id="55baf-133">-確認</span><span class="sxs-lookup"><span data-stu-id="55baf-133">-Confirm</span></span>
<span data-ttu-id="55baf-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55baf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55baf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55baf-135">-WhatIf</span></span>
<span data-ttu-id="55baf-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55baf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55baf-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55baf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55baf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55baf-138">CommonParameters</span></span>
<span data-ttu-id="55baf-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55baf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55baf-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55baf-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55baf-141">輸入</span><span class="sxs-lookup"><span data-stu-id="55baf-141">INPUTS</span></span>

### <span data-ttu-id="55baf-142">所有</span><span class="sxs-lookup"><span data-stu-id="55baf-142">None</span></span>

## <span data-ttu-id="55baf-143">輸出</span><span class="sxs-lookup"><span data-stu-id="55baf-143">OUTPUTS</span></span>

### <span data-ttu-id="55baf-144">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="55baf-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="55baf-145">筆記</span><span class="sxs-lookup"><span data-stu-id="55baf-145">NOTES</span></span>

## <span data-ttu-id="55baf-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="55baf-146">RELATED LINKS</span></span>
