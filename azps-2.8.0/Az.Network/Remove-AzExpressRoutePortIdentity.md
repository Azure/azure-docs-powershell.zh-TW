---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c7ffb86fa56a09fb0c5bbdd41e62bf8d47bee140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789134"
---
# <span data-ttu-id="15d95-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="15d95-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="15d95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15d95-102">SYNOPSIS</span></span>
<span data-ttu-id="15d95-103">從 ExpressRoutePort 中移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="15d95-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="15d95-104">句法</span><span class="sxs-lookup"><span data-stu-id="15d95-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15d95-105">說明</span><span class="sxs-lookup"><span data-stu-id="15d95-105">DESCRIPTION</span></span>
<span data-ttu-id="15d95-106">**AzExpressRoutePortIdentity** Cmdlet 會從本機 Azure ExpressRoutePort 物件中移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="15d95-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="15d95-107">使用 [ **移除-AzExpressRoutePort** ] 將它從 ExpressRoutePort 中移除。</span><span class="sxs-lookup"><span data-stu-id="15d95-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="15d95-108">示例</span><span class="sxs-lookup"><span data-stu-id="15d95-108">EXAMPLES</span></span>

### <span data-ttu-id="15d95-109">範例1</span><span class="sxs-lookup"><span data-stu-id="15d95-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="15d95-110">參數</span><span class="sxs-lookup"><span data-stu-id="15d95-110">PARAMETERS</span></span>

### <span data-ttu-id="15d95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d95-111">-DefaultProfile</span></span>
<span data-ttu-id="15d95-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="15d95-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15d95-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="15d95-113">-ExpressRoutePort</span></span>
<span data-ttu-id="15d95-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="15d95-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="15d95-115">-確認</span><span class="sxs-lookup"><span data-stu-id="15d95-115">-Confirm</span></span>
<span data-ttu-id="15d95-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="15d95-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15d95-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15d95-117">-WhatIf</span></span>
<span data-ttu-id="15d95-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="15d95-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15d95-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15d95-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15d95-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d95-120">CommonParameters</span></span>
<span data-ttu-id="15d95-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15d95-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d95-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="15d95-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="15d95-123">輸入</span><span class="sxs-lookup"><span data-stu-id="15d95-123">INPUTS</span></span>

### <span data-ttu-id="15d95-124">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="15d95-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="15d95-125">輸出</span><span class="sxs-lookup"><span data-stu-id="15d95-125">OUTPUTS</span></span>

### <span data-ttu-id="15d95-126">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="15d95-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="15d95-127">筆記</span><span class="sxs-lookup"><span data-stu-id="15d95-127">NOTES</span></span>

## <span data-ttu-id="15d95-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="15d95-128">RELATED LINKS</span></span>
[<span data-ttu-id="15d95-129">AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="15d95-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="15d95-130">新-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="15d95-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="15d95-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="15d95-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
