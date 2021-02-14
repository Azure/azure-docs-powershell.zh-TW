---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: eb108e665bce54d2b94fc4ab4a56c9573248289a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129926"
---
# <span data-ttu-id="572fa-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="572fa-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="572fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="572fa-102">SYNOPSIS</span></span>
<span data-ttu-id="572fa-103">清除 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="572fa-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="572fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="572fa-104">SYNTAX</span></span>

### <span data-ttu-id="572fa-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="572fa-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="572fa-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="572fa-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="572fa-107">說明</span><span class="sxs-lookup"><span data-stu-id="572fa-107">DESCRIPTION</span></span>
<span data-ttu-id="572fa-108">[ **取消發佈 AzCdnEndpointContent** ] Cmdlet 會清除 Azure 內容傳遞網路 (CDN) 端點中的內容。</span><span class="sxs-lookup"><span data-stu-id="572fa-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="572fa-109">示例</span><span class="sxs-lookup"><span data-stu-id="572fa-109">EXAMPLES</span></span>

## <span data-ttu-id="572fa-110">參數</span><span class="sxs-lookup"><span data-stu-id="572fa-110">PARAMETERS</span></span>

### <span data-ttu-id="572fa-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="572fa-111">-CdnEndpoint</span></span>
<span data-ttu-id="572fa-112">指定此 Cmdlet 清除的端點。</span><span class="sxs-lookup"><span data-stu-id="572fa-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="572fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572fa-113">-DefaultProfile</span></span>
<span data-ttu-id="572fa-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="572fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="572fa-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="572fa-115">-EndpointName</span></span>
<span data-ttu-id="572fa-116">指定此 Cmdlet 清除的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="572fa-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="572fa-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="572fa-117">-PassThru</span></span>
<span data-ttu-id="572fa-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="572fa-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="572fa-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="572fa-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="572fa-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="572fa-120">-ProfileName</span></span>
<span data-ttu-id="572fa-121">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="572fa-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="572fa-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="572fa-122">-PurgeContent</span></span>
<span data-ttu-id="572fa-123">指定此 Cmdlet 所清除之原始伺服器內容的相對路徑陣列。</span><span class="sxs-lookup"><span data-stu-id="572fa-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="572fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="572fa-125">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="572fa-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="572fa-126">-確認</span><span class="sxs-lookup"><span data-stu-id="572fa-126">-Confirm</span></span>
<span data-ttu-id="572fa-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="572fa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="572fa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="572fa-128">-WhatIf</span></span>
<span data-ttu-id="572fa-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="572fa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="572fa-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="572fa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="572fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572fa-131">CommonParameters</span></span>
<span data-ttu-id="572fa-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="572fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572fa-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="572fa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572fa-134">輸入</span><span class="sxs-lookup"><span data-stu-id="572fa-134">INPUTS</span></span>

### <span data-ttu-id="572fa-135">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="572fa-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="572fa-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="572fa-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="572fa-137">輸出</span><span class="sxs-lookup"><span data-stu-id="572fa-137">OUTPUTS</span></span>

### <span data-ttu-id="572fa-138">System.object</span><span class="sxs-lookup"><span data-stu-id="572fa-138">System.Boolean</span></span>

## <span data-ttu-id="572fa-139">筆記</span><span class="sxs-lookup"><span data-stu-id="572fa-139">NOTES</span></span>

## <span data-ttu-id="572fa-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="572fa-140">RELATED LINKS</span></span>

[<span data-ttu-id="572fa-141">發佈-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="572fa-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


