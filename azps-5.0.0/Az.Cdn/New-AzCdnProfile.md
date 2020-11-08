---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 7f609a72adfc7fe023d090028f95d607da4efb2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137707"
---
# <span data-ttu-id="d30c5-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d30c5-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="d30c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d30c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d30c5-103">建立 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d30c5-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="d30c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d30c5-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d30c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="d30c5-105">DESCRIPTION</span></span>
<span data-ttu-id="d30c5-106">**新的-AzCdnProfile** Cmdlet 會在 (CDN) 設定檔] 中建立 Azure 內容傳遞網路。</span><span class="sxs-lookup"><span data-stu-id="d30c5-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="d30c5-107">示例</span><span class="sxs-lookup"><span data-stu-id="d30c5-107">EXAMPLES</span></span>

### <span data-ttu-id="d30c5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d30c5-108">Example 1</span></span>

<span data-ttu-id="d30c5-109">建立 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d30c5-109">Creates a CDN profile.</span></span> <span data-ttu-id="d30c5-110"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="d30c5-110">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzCdnProfile -Location westus -ProfileName <String> -ResourceGroupName myresourcegroup -Sku Standard_Verizon
```

## <span data-ttu-id="d30c5-111">參數</span><span class="sxs-lookup"><span data-stu-id="d30c5-111">PARAMETERS</span></span>

### <span data-ttu-id="d30c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d30c5-112">-DefaultProfile</span></span>
<span data-ttu-id="d30c5-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d30c5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d30c5-114">-位置</span><span class="sxs-lookup"><span data-stu-id="d30c5-114">-Location</span></span>
<span data-ttu-id="d30c5-115">指定設定檔的資源位置。</span><span class="sxs-lookup"><span data-stu-id="d30c5-115">Specifies the resource location of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30c5-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d30c5-116">-ProfileName</span></span>
<span data-ttu-id="d30c5-117">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="d30c5-117">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30c5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d30c5-118">-ResourceGroupName</span></span>
<span data-ttu-id="d30c5-119">指定設定檔所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d30c5-119">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30c5-120">-Sku</span><span class="sxs-lookup"><span data-stu-id="d30c5-120">-Sku</span></span>
<span data-ttu-id="d30c5-121">指定設定檔的 SKU。</span><span class="sxs-lookup"><span data-stu-id="d30c5-121">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_Microsoft, Standard_ChinaCdn, Premium_ChinaCdn, Standard_955BandWidth_ChinaCdn, Standard_AvgBandWidth_ChinaCdn, StandardPlus_ChinaCdn, StandardPlus_955BandWidth_ChinaCdn, StandardPlus_AvgBandWidth_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30c5-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="d30c5-122">-Tag</span></span>
<span data-ttu-id="d30c5-123">要與 Azure CDN 設定檔相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="d30c5-123">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30c5-124">-確認</span><span class="sxs-lookup"><span data-stu-id="d30c5-124">-Confirm</span></span>
<span data-ttu-id="d30c5-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d30c5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d30c5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d30c5-126">-WhatIf</span></span>
<span data-ttu-id="d30c5-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d30c5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d30c5-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d30c5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d30c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d30c5-129">CommonParameters</span></span>
<span data-ttu-id="d30c5-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d30c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d30c5-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d30c5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d30c5-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d30c5-132">INPUTS</span></span>

### <span data-ttu-id="d30c5-133">System.object</span><span class="sxs-lookup"><span data-stu-id="d30c5-133">System.String</span></span>

## <span data-ttu-id="d30c5-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d30c5-134">OUTPUTS</span></span>

### <span data-ttu-id="d30c5-135">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d30c5-135">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="d30c5-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d30c5-136">NOTES</span></span>

## <span data-ttu-id="d30c5-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d30c5-137">RELATED LINKS</span></span>

[<span data-ttu-id="d30c5-138">AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d30c5-138">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="d30c5-139">移除-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d30c5-139">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="d30c5-140">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d30c5-140">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)

