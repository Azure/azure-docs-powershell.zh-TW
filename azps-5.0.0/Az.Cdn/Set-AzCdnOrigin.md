---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139090"
---
# <span data-ttu-id="b1845-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b1845-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="b1845-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1845-102">SYNOPSIS</span></span>
<span data-ttu-id="b1845-103">更新 CDN 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="b1845-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="b1845-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1845-104">SYNTAX</span></span>

### <span data-ttu-id="b1845-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b1845-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1845-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1845-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1845-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1845-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1845-108">說明</span><span class="sxs-lookup"><span data-stu-id="b1845-108">DESCRIPTION</span></span>
<span data-ttu-id="b1845-109">**AzCdnOrigin** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="b1845-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="b1845-110">示例</span><span class="sxs-lookup"><span data-stu-id="b1845-110">EXAMPLES</span></span>

## <span data-ttu-id="b1845-111">參數</span><span class="sxs-lookup"><span data-stu-id="b1845-111">PARAMETERS</span></span>

### <span data-ttu-id="b1845-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b1845-112">-CdnOrigin</span></span>
<span data-ttu-id="b1845-113">指定此 Cmdlet 更新的原始伺服器。</span><span class="sxs-lookup"><span data-stu-id="b1845-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b1845-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1845-114">-DefaultProfile</span></span>
<span data-ttu-id="b1845-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b1845-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1845-116">-終結點</span><span class="sxs-lookup"><span data-stu-id="b1845-116">-EndpointName</span></span>
<span data-ttu-id="b1845-117">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="b1845-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="b1845-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="b1845-118">-HostName</span></span>
<span data-ttu-id="b1845-119">Azure CDN 原始主機名稱。</span><span class="sxs-lookup"><span data-stu-id="b1845-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="b1845-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="b1845-120">-HttpPort</span></span>
<span data-ttu-id="b1845-121">Azure CDN 原始 HTTP 埠。</span><span class="sxs-lookup"><span data-stu-id="b1845-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="b1845-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="b1845-122">-HttpsPort</span></span>
<span data-ttu-id="b1845-123">Azure CDN 起源 HTTPs 埠。</span><span class="sxs-lookup"><span data-stu-id="b1845-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="b1845-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="b1845-124">-OriginHostHeader</span></span>
<span data-ttu-id="b1845-125">Azure CDN 來源主機標頭。</span><span class="sxs-lookup"><span data-stu-id="b1845-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="b1845-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="b1845-126">-OriginName</span></span>
<span data-ttu-id="b1845-127">Azure CDN 原始名稱。</span><span class="sxs-lookup"><span data-stu-id="b1845-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="b1845-128">-優先順序</span><span class="sxs-lookup"><span data-stu-id="b1845-128">-Priority</span></span>
<span data-ttu-id="b1845-129">Azure CDN 原始優先順序。</span><span class="sxs-lookup"><span data-stu-id="b1845-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="b1845-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="b1845-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="b1845-131">要包含在要連線到私人連結之核准要求中的自訂訊息。</span><span class="sxs-lookup"><span data-stu-id="b1845-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="b1845-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="b1845-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="b1845-133">Azure CDN 來源私人連結位置。</span><span class="sxs-lookup"><span data-stu-id="b1845-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="b1845-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="b1845-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="b1845-135">Azure CDN 來源私人連結資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1845-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="b1845-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b1845-136">-ProfileName</span></span>
<span data-ttu-id="b1845-137">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="b1845-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="b1845-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1845-138">-ResourceGroupName</span></span>
<span data-ttu-id="b1845-139">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="b1845-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="b1845-140">寬度</span><span class="sxs-lookup"><span data-stu-id="b1845-140">-Weight</span></span>
<span data-ttu-id="b1845-141">Azure CDN 原始重量。</span><span class="sxs-lookup"><span data-stu-id="b1845-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="b1845-142">-確認</span><span class="sxs-lookup"><span data-stu-id="b1845-142">-Confirm</span></span>
<span data-ttu-id="b1845-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1845-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1845-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1845-144">-WhatIf</span></span>
<span data-ttu-id="b1845-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1845-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1845-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1845-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1845-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1845-147">CommonParameters</span></span>
<span data-ttu-id="b1845-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1845-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1845-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1845-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1845-150">輸入</span><span class="sxs-lookup"><span data-stu-id="b1845-150">INPUTS</span></span>

### <span data-ttu-id="b1845-151">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="b1845-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b1845-152">輸出</span><span class="sxs-lookup"><span data-stu-id="b1845-152">OUTPUTS</span></span>

### <span data-ttu-id="b1845-153">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="b1845-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b1845-154">筆記</span><span class="sxs-lookup"><span data-stu-id="b1845-154">NOTES</span></span>

## <span data-ttu-id="b1845-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1845-155">RELATED LINKS</span></span>

[<span data-ttu-id="b1845-156">AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b1845-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)

