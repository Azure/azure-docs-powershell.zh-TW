---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280677"
---
# <span data-ttu-id="c2a1a-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c2a1a-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="c2a1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a1a-103">更新 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c2a1a-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="c2a1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2a1a-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2a1a-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2a1a-105">DESCRIPTION</span></span>
<span data-ttu-id="c2a1a-106">**AzCdnProfile** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c2a1a-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="c2a1a-107">示例</span><span class="sxs-lookup"><span data-stu-id="c2a1a-107">EXAMPLES</span></span>

## <span data-ttu-id="c2a1a-108">參數</span><span class="sxs-lookup"><span data-stu-id="c2a1a-108">PARAMETERS</span></span>

### <span data-ttu-id="c2a1a-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c2a1a-109">-CdnProfile</span></span>
<span data-ttu-id="c2a1a-110">指定此 Cmdlet 更新的設定檔。</span><span class="sxs-lookup"><span data-stu-id="c2a1a-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="c2a1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a1a-111">-DefaultProfile</span></span>
<span data-ttu-id="c2a1a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c2a1a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2a1a-113">-確認</span><span class="sxs-lookup"><span data-stu-id="c2a1a-113">-Confirm</span></span>
<span data-ttu-id="c2a1a-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2a1a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2a1a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2a1a-115">-WhatIf</span></span>
<span data-ttu-id="c2a1a-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2a1a-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2a1a-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2a1a-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2a1a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a1a-118">CommonParameters</span></span>
<span data-ttu-id="c2a1a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2a1a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a1a-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c2a1a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a1a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="c2a1a-121">INPUTS</span></span>

### <span data-ttu-id="c2a1a-122">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2a1a-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c2a1a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="c2a1a-123">OUTPUTS</span></span>

### <span data-ttu-id="c2a1a-124">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2a1a-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c2a1a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="c2a1a-125">NOTES</span></span>

## <span data-ttu-id="c2a1a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2a1a-126">RELATED LINKS</span></span>

[<span data-ttu-id="c2a1a-127">AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c2a1a-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="c2a1a-128">新-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c2a1a-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="c2a1a-129">移除-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c2a1a-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


