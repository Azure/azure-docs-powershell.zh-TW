---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965496"
---
# <span data-ttu-id="30c7c-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="30c7c-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="30c7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="30c7c-103">從 ExpressRoutePort 中移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="30c7c-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="30c7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="30c7c-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30c7c-105">說明</span><span class="sxs-lookup"><span data-stu-id="30c7c-105">DESCRIPTION</span></span>
<span data-ttu-id="30c7c-106">**AzExpressRoutePortIdentity** Cmdlet 會從本機 Azure ExpressRoutePort 物件中移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="30c7c-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="30c7c-107">使用 [ **移除-AzExpressRoutePort** ] 將它從 ExpressRoutePort 中移除。</span><span class="sxs-lookup"><span data-stu-id="30c7c-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="30c7c-108">示例</span><span class="sxs-lookup"><span data-stu-id="30c7c-108">EXAMPLES</span></span>

### <span data-ttu-id="30c7c-109">範例1</span><span class="sxs-lookup"><span data-stu-id="30c7c-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="30c7c-110">參數</span><span class="sxs-lookup"><span data-stu-id="30c7c-110">PARAMETERS</span></span>

### <span data-ttu-id="30c7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c7c-111">-DefaultProfile</span></span>
<span data-ttu-id="30c7c-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30c7c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30c7c-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30c7c-113">-ExpressRoutePort</span></span>
<span data-ttu-id="30c7c-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30c7c-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30c7c-115">-確認</span><span class="sxs-lookup"><span data-stu-id="30c7c-115">-Confirm</span></span>
<span data-ttu-id="30c7c-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30c7c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30c7c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c7c-117">-WhatIf</span></span>
<span data-ttu-id="30c7c-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30c7c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30c7c-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30c7c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30c7c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c7c-120">CommonParameters</span></span>
<span data-ttu-id="30c7c-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30c7c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c7c-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30c7c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="30c7c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="30c7c-123">INPUTS</span></span>

### <span data-ttu-id="30c7c-124">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="30c7c-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="30c7c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="30c7c-125">OUTPUTS</span></span>

### <span data-ttu-id="30c7c-126">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="30c7c-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="30c7c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="30c7c-127">NOTES</span></span>

## <span data-ttu-id="30c7c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="30c7c-128">RELATED LINKS</span></span>
[<span data-ttu-id="30c7c-129">AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="30c7c-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="30c7c-130">新-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="30c7c-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="30c7c-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="30c7c-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)