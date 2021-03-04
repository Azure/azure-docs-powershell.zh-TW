---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: 93b1c0869793c30b6f733699029aca7bba9d613e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902125"
---
# <span data-ttu-id="7711e-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7711e-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="7711e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7711e-102">SYNOPSIS</span></span>
<span data-ttu-id="7711e-103">停止 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="7711e-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="7711e-104">語法</span><span class="sxs-lookup"><span data-stu-id="7711e-104">SYNTAX</span></span>

### <span data-ttu-id="7711e-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7711e-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7711e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7711e-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7711e-107">描述</span><span class="sxs-lookup"><span data-stu-id="7711e-107">DESCRIPTION</span></span>
<span data-ttu-id="7711e-108">**Stop-AzCdnEndpoint** Cmdlet 會停止 Azure 內容傳遞網路 (CDN) 端點。</span><span class="sxs-lookup"><span data-stu-id="7711e-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7711e-109">例子</span><span class="sxs-lookup"><span data-stu-id="7711e-109">EXAMPLES</span></span>

## <span data-ttu-id="7711e-110">參數</span><span class="sxs-lookup"><span data-stu-id="7711e-110">PARAMETERS</span></span>

### <span data-ttu-id="7711e-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7711e-111">-CdnEndpoint</span></span>
<span data-ttu-id="7711e-112">指定此 Cmdlet 停止的端點物件。</span><span class="sxs-lookup"><span data-stu-id="7711e-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="7711e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7711e-113">-DefaultProfile</span></span>
<span data-ttu-id="7711e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7711e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7711e-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7711e-115">-EndpointName</span></span>
<span data-ttu-id="7711e-116">指定此 Cmdlet 停止的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="7711e-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="7711e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7711e-117">-PassThru</span></span>
<span data-ttu-id="7711e-118">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="7711e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7711e-119">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7711e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7711e-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7711e-120">-ProfileName</span></span>
<span data-ttu-id="7711e-121">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="7711e-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="7711e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7711e-122">-ResourceGroupName</span></span>
<span data-ttu-id="7711e-123">指定端點所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7711e-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="7711e-124">-確認</span><span class="sxs-lookup"><span data-stu-id="7711e-124">-Confirm</span></span>
<span data-ttu-id="7711e-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7711e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7711e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7711e-126">-WhatIf</span></span>
<span data-ttu-id="7711e-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7711e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7711e-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7711e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7711e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7711e-129">CommonParameters</span></span>
<span data-ttu-id="7711e-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7711e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7711e-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7711e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7711e-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7711e-132">INPUTS</span></span>

### <span data-ttu-id="7711e-133">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7711e-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="7711e-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7711e-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7711e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7711e-135">OUTPUTS</span></span>

### <span data-ttu-id="7711e-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7711e-136">System.Boolean</span></span>

## <span data-ttu-id="7711e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7711e-137">NOTES</span></span>

## <span data-ttu-id="7711e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7711e-138">RELATED LINKS</span></span>

[<span data-ttu-id="7711e-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7711e-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="7711e-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7711e-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="7711e-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7711e-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="7711e-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7711e-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="7711e-143">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7711e-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


