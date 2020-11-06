---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: ecc89a75f144a92653dd0e3c498d664df8c370e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622844"
---
# <span data-ttu-id="61dcc-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="61dcc-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="61dcc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="61dcc-103">更新 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="61dcc-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="61dcc-104">句法</span><span class="sxs-lookup"><span data-stu-id="61dcc-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61dcc-105">說明</span><span class="sxs-lookup"><span data-stu-id="61dcc-105">DESCRIPTION</span></span>
<span data-ttu-id="61dcc-106">**AzCdnProfile** Cmdlet 會更新 Azure 內容傳遞網路 (CDN) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="61dcc-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="61dcc-107">示例</span><span class="sxs-lookup"><span data-stu-id="61dcc-107">EXAMPLES</span></span>

## <span data-ttu-id="61dcc-108">參數</span><span class="sxs-lookup"><span data-stu-id="61dcc-108">PARAMETERS</span></span>

### <span data-ttu-id="61dcc-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="61dcc-109">-CdnProfile</span></span>
<span data-ttu-id="61dcc-110">指定此 Cmdlet 更新的設定檔。</span><span class="sxs-lookup"><span data-stu-id="61dcc-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="61dcc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61dcc-111">-DefaultProfile</span></span>
<span data-ttu-id="61dcc-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="61dcc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61dcc-113">-確認</span><span class="sxs-lookup"><span data-stu-id="61dcc-113">-Confirm</span></span>
<span data-ttu-id="61dcc-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61dcc-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61dcc-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61dcc-115">-WhatIf</span></span>
<span data-ttu-id="61dcc-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61dcc-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61dcc-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61dcc-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61dcc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61dcc-118">CommonParameters</span></span>
<span data-ttu-id="61dcc-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61dcc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61dcc-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61dcc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61dcc-121">輸入</span><span class="sxs-lookup"><span data-stu-id="61dcc-121">INPUTS</span></span>

### <span data-ttu-id="61dcc-122">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="61dcc-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="61dcc-123">輸出</span><span class="sxs-lookup"><span data-stu-id="61dcc-123">OUTPUTS</span></span>

### <span data-ttu-id="61dcc-124">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="61dcc-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="61dcc-125">筆記</span><span class="sxs-lookup"><span data-stu-id="61dcc-125">NOTES</span></span>

## <span data-ttu-id="61dcc-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="61dcc-126">RELATED LINKS</span></span>

[<span data-ttu-id="61dcc-127">AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="61dcc-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="61dcc-128">新-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="61dcc-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="61dcc-129">移除-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="61dcc-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

