---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: a954b6c259b9e793ca4e35e99ecb4c710ab7a4e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902126"
---
# <span data-ttu-id="ee0a4-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="ee0a4-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="ee0a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ee0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ee0a4-103">移除 CDN 來源群組</span><span class="sxs-lookup"><span data-stu-id="ee0a4-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="ee0a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="ee0a4-104">SYNTAX</span></span>

### <span data-ttu-id="ee0a4-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ee0a4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee0a4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee0a4-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee0a4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee0a4-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee0a4-108">描述</span><span class="sxs-lookup"><span data-stu-id="ee0a4-108">DESCRIPTION</span></span>
<span data-ttu-id="ee0a4-109">Remove-AzCdnOriginGroup會從指定的端點移除 CDN 來源群組。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="ee0a4-110">例子</span><span class="sxs-lookup"><span data-stu-id="ee0a4-110">EXAMPLES</span></span>

### <span data-ttu-id="ee0a4-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ee0a4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="ee0a4-112">此 Cmdlet 會從指定的端點移除指定的原始組。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="ee0a4-113">參數</span><span class="sxs-lookup"><span data-stu-id="ee0a4-113">PARAMETERS</span></span>

### <span data-ttu-id="ee0a4-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="ee0a4-114">-CdnOriginGroup</span></span>
<span data-ttu-id="ee0a4-115">CDN 來源群組物件。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-115">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee0a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee0a4-116">-DefaultProfile</span></span>
<span data-ttu-id="ee0a4-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee0a4-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ee0a4-118">-EndpointName</span></span>
<span data-ttu-id="ee0a4-119">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="ee0a4-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="ee0a4-120">-OriginGroupName</span></span>
<span data-ttu-id="ee0a4-121">Azure CDN 來源組名。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="ee0a4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee0a4-122">-PassThru</span></span>
<span data-ttu-id="ee0a4-123">如果指定，則 Return 物件。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-123">Return object if specified.</span></span>

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

### <span data-ttu-id="ee0a4-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ee0a4-124">-ProfileName</span></span>
<span data-ttu-id="ee0a4-125">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="ee0a4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee0a4-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee0a4-127">Azure CDN 設定檔的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="ee0a4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee0a4-128">-ResourceId</span></span>
<span data-ttu-id="ee0a4-129">Azure CDN 來源群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-129">The resource id of the Azure CDN origin group.</span></span>

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

### <span data-ttu-id="ee0a4-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ee0a4-130">-Confirm</span></span>
<span data-ttu-id="ee0a4-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee0a4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee0a4-132">-WhatIf</span></span>
<span data-ttu-id="ee0a4-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee0a4-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee0a4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee0a4-135">CommonParameters</span></span>
<span data-ttu-id="ee0a4-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ee0a4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee0a4-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee0a4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee0a4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ee0a4-138">INPUTS</span></span>

### <span data-ttu-id="ee0a4-139">沒有</span><span class="sxs-lookup"><span data-stu-id="ee0a4-139">None</span></span>

## <span data-ttu-id="ee0a4-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ee0a4-140">OUTPUTS</span></span>

### <span data-ttu-id="ee0a4-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee0a4-141">System.Boolean</span></span>

## <span data-ttu-id="ee0a4-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ee0a4-142">NOTES</span></span>

## <span data-ttu-id="ee0a4-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee0a4-143">RELATED LINKS</span></span>
