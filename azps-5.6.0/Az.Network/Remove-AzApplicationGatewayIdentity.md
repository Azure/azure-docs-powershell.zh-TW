---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 7d4cce44aa76628011b35d6723b1ae34a869a2e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910974"
---
# <span data-ttu-id="573f2-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="573f2-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="573f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="573f2-102">SYNOPSIS</span></span>
<span data-ttu-id="573f2-103">從應用程式閘道移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="573f2-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="573f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="573f2-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="573f2-105">描述</span><span class="sxs-lookup"><span data-stu-id="573f2-105">DESCRIPTION</span></span>
<span data-ttu-id="573f2-106">**Remove-AzApplicationGatewayIdentity** Cmdlet 會從應用程式閘道移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="573f2-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="573f2-107">例子</span><span class="sxs-lookup"><span data-stu-id="573f2-107">EXAMPLES</span></span>

### <span data-ttu-id="573f2-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="573f2-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="573f2-109">在此範例中，我們會從現有的應用程式閘道移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="573f2-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="573f2-110">注意：如果閘道是參照 Keyvault 機密，則執行此作業時，也一併移除這些 ssl 憑證參照也非常重要。</span><span class="sxs-lookup"><span data-stu-id="573f2-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="573f2-111">參數</span><span class="sxs-lookup"><span data-stu-id="573f2-111">PARAMETERS</span></span>

### <span data-ttu-id="573f2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="573f2-112">-ApplicationGateway</span></span>
<span data-ttu-id="573f2-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="573f2-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="573f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573f2-114">-DefaultProfile</span></span>
<span data-ttu-id="573f2-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="573f2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="573f2-116">-確認</span><span class="sxs-lookup"><span data-stu-id="573f2-116">-Confirm</span></span>
<span data-ttu-id="573f2-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="573f2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="573f2-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="573f2-118">-WhatIf</span></span>
<span data-ttu-id="573f2-119">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="573f2-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="573f2-120">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="573f2-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="573f2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573f2-121">CommonParameters</span></span>
<span data-ttu-id="573f2-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="573f2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573f2-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="573f2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573f2-124">輸入</span><span class="sxs-lookup"><span data-stu-id="573f2-124">INPUTS</span></span>

### <span data-ttu-id="573f2-125">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="573f2-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="573f2-126">輸出</span><span class="sxs-lookup"><span data-stu-id="573f2-126">OUTPUTS</span></span>

### <span data-ttu-id="573f2-127">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="573f2-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="573f2-128">筆記</span><span class="sxs-lookup"><span data-stu-id="573f2-128">NOTES</span></span>

## <span data-ttu-id="573f2-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="573f2-129">RELATED LINKS</span></span>
