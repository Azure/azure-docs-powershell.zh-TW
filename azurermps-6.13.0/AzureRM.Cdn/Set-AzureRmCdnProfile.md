---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: e80b82f567dd1c0935dd56d8e3996a63bcce72e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450261"
---
# <span data-ttu-id="df696-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="df696-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="df696-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df696-102">SYNOPSIS</span></span>
<span data-ttu-id="df696-103">更新 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="df696-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df696-104">句法</span><span class="sxs-lookup"><span data-stu-id="df696-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df696-105">說明</span><span class="sxs-lookup"><span data-stu-id="df696-105">DESCRIPTION</span></span>
<span data-ttu-id="df696-106">**AzureRmCdnProfile** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="df696-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="df696-107">示例</span><span class="sxs-lookup"><span data-stu-id="df696-107">EXAMPLES</span></span>

## <span data-ttu-id="df696-108">參數</span><span class="sxs-lookup"><span data-stu-id="df696-108">PARAMETERS</span></span>

### <span data-ttu-id="df696-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="df696-109">-CdnProfile</span></span>
<span data-ttu-id="df696-110">指定此 Cmdlet 更新的設定檔。</span><span class="sxs-lookup"><span data-stu-id="df696-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df696-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df696-111">-DefaultProfile</span></span>
<span data-ttu-id="df696-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="df696-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df696-113">-確認</span><span class="sxs-lookup"><span data-stu-id="df696-113">-Confirm</span></span>
<span data-ttu-id="df696-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="df696-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df696-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df696-115">-WhatIf</span></span>
<span data-ttu-id="df696-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df696-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df696-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df696-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df696-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df696-118">CommonParameters</span></span>
<span data-ttu-id="df696-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df696-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df696-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df696-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df696-121">輸入</span><span class="sxs-lookup"><span data-stu-id="df696-121">INPUTS</span></span>

### <span data-ttu-id="df696-122">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="df696-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="df696-123">參數： CdnProfile (ByValue) </span><span class="sxs-lookup"><span data-stu-id="df696-123">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="df696-124">輸出</span><span class="sxs-lookup"><span data-stu-id="df696-124">OUTPUTS</span></span>

### <span data-ttu-id="df696-125">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="df696-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="df696-126">筆記</span><span class="sxs-lookup"><span data-stu-id="df696-126">NOTES</span></span>

## <span data-ttu-id="df696-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="df696-127">RELATED LINKS</span></span>

[<span data-ttu-id="df696-128">AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="df696-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="df696-129">新-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="df696-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="df696-130">移除-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="df696-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


