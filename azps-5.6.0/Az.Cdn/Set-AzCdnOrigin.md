---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 5636aeef0b1c04ffbb0faa7e44161628824e9f1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917417"
---
# <span data-ttu-id="0e141-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="0e141-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="0e141-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0e141-102">SYNOPSIS</span></span>
<span data-ttu-id="0e141-103">更新 CDN 原始伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e141-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="0e141-104">語法</span><span class="sxs-lookup"><span data-stu-id="0e141-104">SYNTAX</span></span>

### <span data-ttu-id="0e141-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0e141-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e141-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e141-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e141-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e141-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e141-108">描述</span><span class="sxs-lookup"><span data-stu-id="0e141-108">DESCRIPTION</span></span>
<span data-ttu-id="0e141-109">**Set-AzCdnOrigin** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e141-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="0e141-110">例子</span><span class="sxs-lookup"><span data-stu-id="0e141-110">EXAMPLES</span></span>

## <span data-ttu-id="0e141-111">參數</span><span class="sxs-lookup"><span data-stu-id="0e141-111">PARAMETERS</span></span>

### <span data-ttu-id="0e141-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="0e141-112">-CdnOrigin</span></span>
<span data-ttu-id="0e141-113">指定此 Cmdlet 更新的來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e141-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="0e141-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e141-114">-DefaultProfile</span></span>
<span data-ttu-id="0e141-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0e141-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e141-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0e141-116">-EndpointName</span></span>
<span data-ttu-id="0e141-117">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="0e141-117">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="0e141-118">-HostName</span></span>
<span data-ttu-id="0e141-119">Azure CDN 來源主機名稱稱。</span><span class="sxs-lookup"><span data-stu-id="0e141-119">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-120">-HTTPPort</span><span class="sxs-lookup"><span data-stu-id="0e141-120">-HttpPort</span></span>
<span data-ttu-id="0e141-121">Azure CDN 來源 HTTP 埠。</span><span class="sxs-lookup"><span data-stu-id="0e141-121">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-122">-HTTPsPort</span><span class="sxs-lookup"><span data-stu-id="0e141-122">-HttpsPort</span></span>
<span data-ttu-id="0e141-123">Azure CDN 來源 HTTPs 埠。</span><span class="sxs-lookup"><span data-stu-id="0e141-123">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="0e141-124">-OriginHostHeader</span></span>
<span data-ttu-id="0e141-125">Azure CDN 來源主機標題。</span><span class="sxs-lookup"><span data-stu-id="0e141-125">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="0e141-126">-OriginName</span></span>
<span data-ttu-id="0e141-127">Azure CDN 來源名稱。</span><span class="sxs-lookup"><span data-stu-id="0e141-127">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-128">-優先順序</span><span class="sxs-lookup"><span data-stu-id="0e141-128">-Priority</span></span>
<span data-ttu-id="0e141-129">Azure CDN 來源優先順序。</span><span class="sxs-lookup"><span data-stu-id="0e141-129">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="0e141-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="0e141-131">要包含在核准要求中以連結至私人連結的自訂訊息。</span><span class="sxs-lookup"><span data-stu-id="0e141-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="0e141-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="0e141-133">Azure CDN 來源私人連結位置。</span><span class="sxs-lookup"><span data-stu-id="0e141-133">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="0e141-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="0e141-135">Azure CDN 來源私人連結資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e141-135">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0e141-136">-ProfileName</span></span>
<span data-ttu-id="0e141-137">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="0e141-137">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e141-138">-ResourceGroupName</span></span>
<span data-ttu-id="0e141-139">Azure CDN 設定檔的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0e141-139">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-140">-重量</span><span class="sxs-lookup"><span data-stu-id="0e141-140">-Weight</span></span>
<span data-ttu-id="0e141-141">Azure CDN 來源粗細。</span><span class="sxs-lookup"><span data-stu-id="0e141-141">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e141-142">-確認</span><span class="sxs-lookup"><span data-stu-id="0e141-142">-Confirm</span></span>
<span data-ttu-id="0e141-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0e141-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e141-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e141-144">-WhatIf</span></span>
<span data-ttu-id="0e141-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e141-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e141-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e141-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e141-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e141-147">CommonParameters</span></span>
<span data-ttu-id="0e141-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0e141-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e141-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e141-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e141-150">輸入</span><span class="sxs-lookup"><span data-stu-id="0e141-150">INPUTS</span></span>

### <span data-ttu-id="0e141-151">Microsoft.Azure.Commands.Cdn.models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="0e141-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="0e141-152">輸出</span><span class="sxs-lookup"><span data-stu-id="0e141-152">OUTPUTS</span></span>

### <span data-ttu-id="0e141-153">Microsoft.Azure.Commands.Cdn.models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="0e141-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="0e141-154">筆記</span><span class="sxs-lookup"><span data-stu-id="0e141-154">NOTES</span></span>

## <span data-ttu-id="0e141-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e141-155">RELATED LINKS</span></span>

[<span data-ttu-id="0e141-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="0e141-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


