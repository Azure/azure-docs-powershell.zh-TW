---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 22644dca713ef234aec8be17c324faaf90eebf20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913441"
---
# <span data-ttu-id="7d1c0-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7d1c0-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="7d1c0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7d1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1c0-103">從 ExpressRoutePort 移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="7d1c0-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="7d1c0-104">語法</span><span class="sxs-lookup"><span data-stu-id="7d1c0-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d1c0-105">描述</span><span class="sxs-lookup"><span data-stu-id="7d1c0-105">DESCRIPTION</span></span>
<span data-ttu-id="7d1c0-106">**Remove-AzExpressRoutePortIdentity Cmdlet** 會移除本地 Azure ExpressRoutePort 物件的身分識別。</span><span class="sxs-lookup"><span data-stu-id="7d1c0-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="7d1c0-107">使用 **Remove-AzExpressRoutePort** 將其從 ExpressRoutePort 移除。</span><span class="sxs-lookup"><span data-stu-id="7d1c0-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="7d1c0-108">例子</span><span class="sxs-lookup"><span data-stu-id="7d1c0-108">EXAMPLES</span></span>

### <span data-ttu-id="7d1c0-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="7d1c0-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="7d1c0-110">參數</span><span class="sxs-lookup"><span data-stu-id="7d1c0-110">PARAMETERS</span></span>

### <span data-ttu-id="7d1c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1c0-111">-DefaultProfile</span></span>
<span data-ttu-id="7d1c0-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d1c0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d1c0-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7d1c0-113">-ExpressRoutePort</span></span>
<span data-ttu-id="7d1c0-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7d1c0-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="7d1c0-115">-確認</span><span class="sxs-lookup"><span data-stu-id="7d1c0-115">-Confirm</span></span>
<span data-ttu-id="7d1c0-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7d1c0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d1c0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1c0-117">-WhatIf</span></span>
<span data-ttu-id="7d1c0-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d1c0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d1c0-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d1c0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d1c0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1c0-120">CommonParameters</span></span>
<span data-ttu-id="7d1c0-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7d1c0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1c0-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7d1c0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="7d1c0-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7d1c0-123">INPUTS</span></span>

### <span data-ttu-id="7d1c0-124">Microsoft.Azure.Commands.Network.models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7d1c0-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7d1c0-125">輸出</span><span class="sxs-lookup"><span data-stu-id="7d1c0-125">OUTPUTS</span></span>

### <span data-ttu-id="7d1c0-126">Microsoft.Azure.Commands.Network.models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7d1c0-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7d1c0-127">筆記</span><span class="sxs-lookup"><span data-stu-id="7d1c0-127">NOTES</span></span>

## <span data-ttu-id="7d1c0-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d1c0-128">RELATED LINKS</span></span>
[<span data-ttu-id="7d1c0-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7d1c0-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7d1c0-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7d1c0-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7d1c0-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7d1c0-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
