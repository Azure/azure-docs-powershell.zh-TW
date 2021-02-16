---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139394"
---
# <span data-ttu-id="f0ffe-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f0ffe-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="f0ffe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ffe-103">移除 CDN 來源</span><span class="sxs-lookup"><span data-stu-id="f0ffe-103">Removes a CDN origin</span></span>

## <span data-ttu-id="f0ffe-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0ffe-104">SYNTAX</span></span>

### <span data-ttu-id="f0ffe-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f0ffe-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0ffe-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0ffe-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0ffe-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0ffe-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0ffe-108">說明</span><span class="sxs-lookup"><span data-stu-id="f0ffe-108">DESCRIPTION</span></span>
<span data-ttu-id="f0ffe-109">Remove-AzCdnOrigin 會從指定的端點刪除 CDN 來源。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="f0ffe-110">如果來源是指定端點內的唯一原點，則刪除會因為至少需要1個原點而失敗。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="f0ffe-111">示例</span><span class="sxs-lookup"><span data-stu-id="f0ffe-111">EXAMPLES</span></span>

### <span data-ttu-id="f0ffe-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f0ffe-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="f0ffe-113">這個 Cmdlet 會從指定的端點移除指定的來源。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="f0ffe-114">參數</span><span class="sxs-lookup"><span data-stu-id="f0ffe-114">PARAMETERS</span></span>

### <span data-ttu-id="f0ffe-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f0ffe-115">-CdnOrigin</span></span>
<span data-ttu-id="f0ffe-116">CDN 來源物件。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ffe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ffe-117">-DefaultProfile</span></span>
<span data-ttu-id="f0ffe-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ffe-119">-終結點</span><span class="sxs-lookup"><span data-stu-id="f0ffe-119">-EndpointName</span></span>
<span data-ttu-id="f0ffe-120">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="f0ffe-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="f0ffe-121">-OriginName</span></span>
<span data-ttu-id="f0ffe-122">Azure CDN 原始名稱。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="f0ffe-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0ffe-123">-PassThru</span></span>
<span data-ttu-id="f0ffe-124">傳回物件（如果已指定）。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-124">Return object if specified.</span></span>

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

### <span data-ttu-id="f0ffe-125">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f0ffe-125">-ProfileName</span></span>
<span data-ttu-id="f0ffe-126">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="f0ffe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ffe-127">-ResourceGroupName</span></span>
<span data-ttu-id="f0ffe-128">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="f0ffe-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0ffe-129">-ResourceId</span></span>
<span data-ttu-id="f0ffe-130">Azure CDN 來源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-130">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ffe-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f0ffe-131">-Confirm</span></span>
<span data-ttu-id="f0ffe-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0ffe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ffe-133">-WhatIf</span></span>
<span data-ttu-id="f0ffe-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0ffe-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0ffe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ffe-136">CommonParameters</span></span>
<span data-ttu-id="f0ffe-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ffe-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f0ffe-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ffe-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f0ffe-139">INPUTS</span></span>

### <span data-ttu-id="f0ffe-140">所有</span><span class="sxs-lookup"><span data-stu-id="f0ffe-140">None</span></span>

## <span data-ttu-id="f0ffe-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f0ffe-141">OUTPUTS</span></span>

### <span data-ttu-id="f0ffe-142">System.object</span><span class="sxs-lookup"><span data-stu-id="f0ffe-142">System.Boolean</span></span>

## <span data-ttu-id="f0ffe-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f0ffe-143">NOTES</span></span>

## <span data-ttu-id="f0ffe-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0ffe-144">RELATED LINKS</span></span>
