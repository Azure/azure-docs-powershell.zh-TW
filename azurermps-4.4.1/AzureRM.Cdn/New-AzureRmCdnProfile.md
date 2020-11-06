---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 0e69e48d29c96163acbb82ffe691de6affe8d131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452564"
---
# <span data-ttu-id="351fc-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="351fc-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="351fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="351fc-102">SYNOPSIS</span></span>
<span data-ttu-id="351fc-103">建立 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="351fc-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="351fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="351fc-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="351fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="351fc-105">DESCRIPTION</span></span>
<span data-ttu-id="351fc-106">**新的-AzureRmCdnProfile** Cmdlet 會在 (CDN) 設定檔] 中建立 Azure 內容傳遞網路。</span><span class="sxs-lookup"><span data-stu-id="351fc-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="351fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="351fc-107">EXAMPLES</span></span>

## <span data-ttu-id="351fc-108">參數</span><span class="sxs-lookup"><span data-stu-id="351fc-108">PARAMETERS</span></span>

### <span data-ttu-id="351fc-109">-位置</span><span class="sxs-lookup"><span data-stu-id="351fc-109">-Location</span></span>
<span data-ttu-id="351fc-110">指定設定檔的資源位置。</span><span class="sxs-lookup"><span data-stu-id="351fc-110">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="351fc-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="351fc-111">-ProfileName</span></span>
<span data-ttu-id="351fc-112">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="351fc-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="351fc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="351fc-113">-ResourceGroupName</span></span>
<span data-ttu-id="351fc-114">指定設定檔所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="351fc-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="351fc-115">-Sku</span><span class="sxs-lookup"><span data-stu-id="351fc-115">-Sku</span></span>
<span data-ttu-id="351fc-116">指定設定檔的 SKU。</span><span class="sxs-lookup"><span data-stu-id="351fc-116">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351fc-117">-標記</span><span class="sxs-lookup"><span data-stu-id="351fc-117">-Tags</span></span>
<span data-ttu-id="351fc-118">Sepcifies 與此設定檔相關聯的標記雜湊表。</span><span class="sxs-lookup"><span data-stu-id="351fc-118">Sepcifies a hash table of tags that are associated with this profile.</span></span>

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

### <span data-ttu-id="351fc-119">-確認</span><span class="sxs-lookup"><span data-stu-id="351fc-119">-Confirm</span></span>
<span data-ttu-id="351fc-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="351fc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="351fc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="351fc-121">-WhatIf</span></span>
<span data-ttu-id="351fc-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="351fc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="351fc-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="351fc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="351fc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351fc-124">-DefaultProfile</span></span>
<span data-ttu-id="351fc-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="351fc-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351fc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351fc-126">CommonParameters</span></span>
<span data-ttu-id="351fc-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="351fc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351fc-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="351fc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351fc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="351fc-129">INPUTS</span></span>

## <span data-ttu-id="351fc-130">輸出</span><span class="sxs-lookup"><span data-stu-id="351fc-130">OUTPUTS</span></span>

### <span data-ttu-id="351fc-131">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="351fc-131">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="351fc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="351fc-132">NOTES</span></span>

## <span data-ttu-id="351fc-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="351fc-133">RELATED LINKS</span></span>

[<span data-ttu-id="351fc-134">AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="351fc-134">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="351fc-135">移除-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="351fc-135">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="351fc-136">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="351fc-136">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


