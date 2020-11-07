---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 6c17b3732cf5eab46f5826896dacafd3639aa788
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958786"
---
# <span data-ttu-id="5830a-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5830a-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="5830a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5830a-102">SYNOPSIS</span></span>
<span data-ttu-id="5830a-103">建立 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5830a-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="5830a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5830a-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5830a-105">說明</span><span class="sxs-lookup"><span data-stu-id="5830a-105">DESCRIPTION</span></span>
<span data-ttu-id="5830a-106">**新的-AzCdnProfile** Cmdlet 會在 (CDN) 設定檔] 中建立 Azure 內容傳遞網路。</span><span class="sxs-lookup"><span data-stu-id="5830a-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="5830a-107">示例</span><span class="sxs-lookup"><span data-stu-id="5830a-107">EXAMPLES</span></span>

## <span data-ttu-id="5830a-108">參數</span><span class="sxs-lookup"><span data-stu-id="5830a-108">PARAMETERS</span></span>

### <span data-ttu-id="5830a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5830a-109">-DefaultProfile</span></span>
<span data-ttu-id="5830a-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5830a-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5830a-111">-位置</span><span class="sxs-lookup"><span data-stu-id="5830a-111">-Location</span></span>
<span data-ttu-id="5830a-112">指定設定檔的資源位置。</span><span class="sxs-lookup"><span data-stu-id="5830a-112">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="5830a-113">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5830a-113">-ProfileName</span></span>
<span data-ttu-id="5830a-114">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="5830a-114">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="5830a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5830a-115">-ResourceGroupName</span></span>
<span data-ttu-id="5830a-116">指定設定檔所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5830a-116">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="5830a-117">-Sku</span><span class="sxs-lookup"><span data-stu-id="5830a-117">-Sku</span></span>
<span data-ttu-id="5830a-118">指定設定檔的 SKU。</span><span class="sxs-lookup"><span data-stu-id="5830a-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn, Standard_Microsoft

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5830a-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="5830a-119">-Tag</span></span>
<span data-ttu-id="5830a-120">要與 Azure CDN 設定檔相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="5830a-120">The tags to associate with the Azure CDN profile.</span></span>

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

### <span data-ttu-id="5830a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="5830a-121">-Confirm</span></span>
<span data-ttu-id="5830a-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5830a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5830a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5830a-123">-WhatIf</span></span>
<span data-ttu-id="5830a-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5830a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5830a-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5830a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5830a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5830a-126">CommonParameters</span></span>
<span data-ttu-id="5830a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5830a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5830a-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5830a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5830a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5830a-129">INPUTS</span></span>

### <span data-ttu-id="5830a-130">System.object</span><span class="sxs-lookup"><span data-stu-id="5830a-130">System.String</span></span>

## <span data-ttu-id="5830a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5830a-131">OUTPUTS</span></span>

### <span data-ttu-id="5830a-132">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5830a-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="5830a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5830a-133">NOTES</span></span>

## <span data-ttu-id="5830a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5830a-134">RELATED LINKS</span></span>

[<span data-ttu-id="5830a-135">AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5830a-135">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="5830a-136">移除-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5830a-136">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="5830a-137">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5830a-137">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


