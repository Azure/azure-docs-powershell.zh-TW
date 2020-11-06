---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 22ace3fb8c2b6b8f620a90cc2f53533ba4a42ff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621655"
---
# <span data-ttu-id="e4c12-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="e4c12-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="e4c12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4c12-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c12-103">從應用程式閘道移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="e4c12-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="e4c12-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4c12-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4c12-105">說明</span><span class="sxs-lookup"><span data-stu-id="e4c12-105">DESCRIPTION</span></span>
<span data-ttu-id="e4c12-106">**AzApplicationGatewayIdentity** Cmdlet 會從應用程式閘道中移除身分識別。</span><span class="sxs-lookup"><span data-stu-id="e4c12-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="e4c12-107">示例</span><span class="sxs-lookup"><span data-stu-id="e4c12-107">EXAMPLES</span></span>

### <span data-ttu-id="e4c12-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e4c12-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="e4c12-109">在這個範例中，我們移除現有應用程式閘道的身分識別。</span><span class="sxs-lookup"><span data-stu-id="e4c12-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="e4c12-110">注意：如果閘道正在參照 keyvault 機密，請務必在此操作中移除那些 ssl 憑證參照。</span><span class="sxs-lookup"><span data-stu-id="e4c12-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="e4c12-111">參數</span><span class="sxs-lookup"><span data-stu-id="e4c12-111">PARAMETERS</span></span>

### <span data-ttu-id="e4c12-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4c12-112">-ApplicationGateway</span></span>
<span data-ttu-id="e4c12-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4c12-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e4c12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c12-114">-DefaultProfile</span></span>
<span data-ttu-id="e4c12-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4c12-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4c12-116">-確認</span><span class="sxs-lookup"><span data-stu-id="e4c12-116">-Confirm</span></span>
<span data-ttu-id="e4c12-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e4c12-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c12-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c12-118">-WhatIf</span></span>
<span data-ttu-id="e4c12-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e4c12-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4c12-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4c12-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c12-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c12-121">CommonParameters</span></span>
<span data-ttu-id="e4c12-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4c12-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c12-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4c12-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c12-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e4c12-124">INPUTS</span></span>

### <span data-ttu-id="e4c12-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e4c12-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4c12-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e4c12-126">OUTPUTS</span></span>

### <span data-ttu-id="e4c12-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e4c12-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4c12-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e4c12-128">NOTES</span></span>

## <span data-ttu-id="e4c12-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4c12-129">RELATED LINKS</span></span>
