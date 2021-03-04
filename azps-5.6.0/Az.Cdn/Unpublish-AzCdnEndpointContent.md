---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: 403c91802c70d7d5e6cfb844909dee1ca6956847
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906330"
---
# <span data-ttu-id="3da9b-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3da9b-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="3da9b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3da9b-102">SYNOPSIS</span></span>
<span data-ttu-id="3da9b-103">清除 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="3da9b-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="3da9b-104">語法</span><span class="sxs-lookup"><span data-stu-id="3da9b-104">SYNTAX</span></span>

### <span data-ttu-id="3da9b-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3da9b-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3da9b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3da9b-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3da9b-107">描述</span><span class="sxs-lookup"><span data-stu-id="3da9b-107">DESCRIPTION</span></span>
<span data-ttu-id="3da9b-108">**Unpublish-AzCdnEndpointContent** Cmdlet 會清除 Azure 內容傳遞網路或 CDN 端點 (內容) 內容。</span><span class="sxs-lookup"><span data-stu-id="3da9b-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="3da9b-109">例子</span><span class="sxs-lookup"><span data-stu-id="3da9b-109">EXAMPLES</span></span>

## <span data-ttu-id="3da9b-110">參數</span><span class="sxs-lookup"><span data-stu-id="3da9b-110">PARAMETERS</span></span>

### <span data-ttu-id="3da9b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3da9b-111">-CdnEndpoint</span></span>
<span data-ttu-id="3da9b-112">指定此 Cmdlet 清除的端點。</span><span class="sxs-lookup"><span data-stu-id="3da9b-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="3da9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da9b-113">-DefaultProfile</span></span>
<span data-ttu-id="3da9b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="3da9b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3da9b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3da9b-115">-EndpointName</span></span>
<span data-ttu-id="3da9b-116">指定此 Cmdlet 清除的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="3da9b-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="3da9b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3da9b-117">-PassThru</span></span>
<span data-ttu-id="3da9b-118">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3da9b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3da9b-119">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3da9b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3da9b-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3da9b-120">-ProfileName</span></span>
<span data-ttu-id="3da9b-121">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="3da9b-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3da9b-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="3da9b-122">-PurgeContent</span></span>
<span data-ttu-id="3da9b-123">指定此 Cmdlet 清除之源伺服器上內容的相對路徑陣列。</span><span class="sxs-lookup"><span data-stu-id="3da9b-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3da9b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3da9b-124">-ResourceGroupName</span></span>
<span data-ttu-id="3da9b-125">指定端點所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3da9b-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3da9b-126">-確認</span><span class="sxs-lookup"><span data-stu-id="3da9b-126">-Confirm</span></span>
<span data-ttu-id="3da9b-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3da9b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3da9b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3da9b-128">-WhatIf</span></span>
<span data-ttu-id="3da9b-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3da9b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3da9b-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3da9b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3da9b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da9b-131">CommonParameters</span></span>
<span data-ttu-id="3da9b-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3da9b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da9b-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3da9b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da9b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3da9b-134">INPUTS</span></span>

### <span data-ttu-id="3da9b-135">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3da9b-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="3da9b-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3da9b-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3da9b-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3da9b-137">OUTPUTS</span></span>

### <span data-ttu-id="3da9b-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3da9b-138">System.Boolean</span></span>

## <span data-ttu-id="3da9b-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3da9b-139">NOTES</span></span>

## <span data-ttu-id="3da9b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="3da9b-140">RELATED LINKS</span></span>

[<span data-ttu-id="3da9b-141">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3da9b-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


