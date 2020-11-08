---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135535"
---
# <span data-ttu-id="4dfa1-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4dfa1-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="4dfa1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4dfa1-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfa1-103">從 ExpressRoutePort 中移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="4dfa1-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="4dfa1-104">句法</span><span class="sxs-lookup"><span data-stu-id="4dfa1-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dfa1-105">說明</span><span class="sxs-lookup"><span data-stu-id="4dfa1-105">DESCRIPTION</span></span>
<span data-ttu-id="4dfa1-106">**AzExpressRoutePortIdentity** Cmdlet 會從本機 Azure ExpressRoutePort 物件中移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="4dfa1-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="4dfa1-107">使用 [ **移除-AzExpressRoutePort** ] 將它從 ExpressRoutePort 中移除。</span><span class="sxs-lookup"><span data-stu-id="4dfa1-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="4dfa1-108">示例</span><span class="sxs-lookup"><span data-stu-id="4dfa1-108">EXAMPLES</span></span>

### <span data-ttu-id="4dfa1-109">範例1</span><span class="sxs-lookup"><span data-stu-id="4dfa1-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="4dfa1-110">參數</span><span class="sxs-lookup"><span data-stu-id="4dfa1-110">PARAMETERS</span></span>

### <span data-ttu-id="4dfa1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfa1-111">-DefaultProfile</span></span>
<span data-ttu-id="4dfa1-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4dfa1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dfa1-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4dfa1-113">-ExpressRoutePort</span></span>
<span data-ttu-id="4dfa1-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4dfa1-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="4dfa1-115">-確認</span><span class="sxs-lookup"><span data-stu-id="4dfa1-115">-Confirm</span></span>
<span data-ttu-id="4dfa1-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4dfa1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dfa1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dfa1-117">-WhatIf</span></span>
<span data-ttu-id="4dfa1-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4dfa1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dfa1-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4dfa1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dfa1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfa1-120">CommonParameters</span></span>
<span data-ttu-id="4dfa1-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4dfa1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfa1-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4dfa1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="4dfa1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="4dfa1-123">INPUTS</span></span>

### <span data-ttu-id="4dfa1-124">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4dfa1-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="4dfa1-125">輸出</span><span class="sxs-lookup"><span data-stu-id="4dfa1-125">OUTPUTS</span></span>

### <span data-ttu-id="4dfa1-126">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4dfa1-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="4dfa1-127">筆記</span><span class="sxs-lookup"><span data-stu-id="4dfa1-127">NOTES</span></span>

## <span data-ttu-id="4dfa1-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="4dfa1-128">RELATED LINKS</span></span>
[<span data-ttu-id="4dfa1-129">AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4dfa1-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="4dfa1-130">新-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4dfa1-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="4dfa1-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4dfa1-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
