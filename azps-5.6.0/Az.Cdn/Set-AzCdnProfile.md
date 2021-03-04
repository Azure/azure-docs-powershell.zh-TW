---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 88e10d5f887d290139ee465217756c598bef0a3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907797"
---
# <span data-ttu-id="4e3e4-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4e3e4-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="4e3e4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4e3e4-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3e4-103">更新 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4e3e4-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="4e3e4-104">語法</span><span class="sxs-lookup"><span data-stu-id="4e3e4-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e3e4-105">描述</span><span class="sxs-lookup"><span data-stu-id="4e3e4-105">DESCRIPTION</span></span>
<span data-ttu-id="4e3e4-106">**Set-AzCdnProfile** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4e3e4-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="4e3e4-107">例子</span><span class="sxs-lookup"><span data-stu-id="4e3e4-107">EXAMPLES</span></span>

## <span data-ttu-id="4e3e4-108">參數</span><span class="sxs-lookup"><span data-stu-id="4e3e4-108">PARAMETERS</span></span>

### <span data-ttu-id="4e3e4-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="4e3e4-109">-CdnProfile</span></span>
<span data-ttu-id="4e3e4-110">指定此 Cmdlet 更新的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4e3e4-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="4e3e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3e4-111">-DefaultProfile</span></span>
<span data-ttu-id="4e3e4-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4e3e4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e3e4-113">-確認</span><span class="sxs-lookup"><span data-stu-id="4e3e4-113">-Confirm</span></span>
<span data-ttu-id="4e3e4-114">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4e3e4-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e3e4-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e3e4-115">-WhatIf</span></span>
<span data-ttu-id="4e3e4-116">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e3e4-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e3e4-117">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e3e4-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e3e4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3e4-118">CommonParameters</span></span>
<span data-ttu-id="4e3e4-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4e3e4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3e4-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e3e4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3e4-121">輸入</span><span class="sxs-lookup"><span data-stu-id="4e3e4-121">INPUTS</span></span>

### <span data-ttu-id="4e3e4-122">Microsoft.Azure.Commands.Cdn.models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="4e3e4-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="4e3e4-123">輸出</span><span class="sxs-lookup"><span data-stu-id="4e3e4-123">OUTPUTS</span></span>

### <span data-ttu-id="4e3e4-124">Microsoft.Azure.Commands.Cdn.models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="4e3e4-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="4e3e4-125">筆記</span><span class="sxs-lookup"><span data-stu-id="4e3e4-125">NOTES</span></span>

## <span data-ttu-id="4e3e4-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e3e4-126">RELATED LINKS</span></span>

[<span data-ttu-id="4e3e4-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4e3e4-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="4e3e4-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4e3e4-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="4e3e4-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4e3e4-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


