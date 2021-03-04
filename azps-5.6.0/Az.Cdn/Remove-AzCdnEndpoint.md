---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: e6c45f74f149cb2c087419a10f3e31cdfeb26610
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903673"
---
# <span data-ttu-id="6e15a-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e15a-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="6e15a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6e15a-102">SYNOPSIS</span></span>
<span data-ttu-id="6e15a-103">移除 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="6e15a-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="6e15a-104">語法</span><span class="sxs-lookup"><span data-stu-id="6e15a-104">SYNTAX</span></span>

### <span data-ttu-id="6e15a-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e15a-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e15a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e15a-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e15a-107">描述</span><span class="sxs-lookup"><span data-stu-id="6e15a-107">DESCRIPTION</span></span>
<span data-ttu-id="6e15a-108">**Remove-AzCdnEndpoint** Cmdlet 會移除 CDN 端點 (Azure) 網路。</span><span class="sxs-lookup"><span data-stu-id="6e15a-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6e15a-109">例子</span><span class="sxs-lookup"><span data-stu-id="6e15a-109">EXAMPLES</span></span>

## <span data-ttu-id="6e15a-110">參數</span><span class="sxs-lookup"><span data-stu-id="6e15a-110">PARAMETERS</span></span>

### <span data-ttu-id="6e15a-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e15a-111">-CdnEndpoint</span></span>
<span data-ttu-id="6e15a-112">指定此 Cmdlet 移除的端點。</span><span class="sxs-lookup"><span data-stu-id="6e15a-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e15a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e15a-113">-DefaultProfile</span></span>
<span data-ttu-id="6e15a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6e15a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e15a-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6e15a-115">-EndpointName</span></span>
<span data-ttu-id="6e15a-116">指定此 Cmdlet 移除的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="6e15a-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e15a-117">-強制</span><span class="sxs-lookup"><span data-stu-id="6e15a-117">-Force</span></span>
<span data-ttu-id="6e15a-118">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6e15a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e15a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e15a-119">-PassThru</span></span>
<span data-ttu-id="6e15a-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="6e15a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6e15a-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6e15a-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e15a-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6e15a-122">-ProfileName</span></span>
<span data-ttu-id="6e15a-123">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="6e15a-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e15a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e15a-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e15a-125">指定端點所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6e15a-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e15a-126">-確認</span><span class="sxs-lookup"><span data-stu-id="6e15a-126">-Confirm</span></span>
<span data-ttu-id="6e15a-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6e15a-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e15a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e15a-128">-WhatIf</span></span>
<span data-ttu-id="6e15a-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e15a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e15a-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e15a-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e15a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e15a-131">CommonParameters</span></span>
<span data-ttu-id="6e15a-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6e15a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e15a-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e15a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e15a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6e15a-134">INPUTS</span></span>

### <span data-ttu-id="6e15a-135">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e15a-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="6e15a-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6e15a-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6e15a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="6e15a-137">OUTPUTS</span></span>

### <span data-ttu-id="6e15a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e15a-138">System.Boolean</span></span>

## <span data-ttu-id="6e15a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6e15a-139">NOTES</span></span>

## <span data-ttu-id="6e15a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e15a-140">RELATED LINKS</span></span>

[<span data-ttu-id="6e15a-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e15a-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="6e15a-142">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e15a-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="6e15a-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e15a-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="6e15a-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e15a-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="6e15a-145">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e15a-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


