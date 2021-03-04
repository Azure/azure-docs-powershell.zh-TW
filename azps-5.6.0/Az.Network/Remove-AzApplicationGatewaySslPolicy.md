---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: e5ac68f10a75dff94313fa17830720466e82da5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911902"
---
# <span data-ttu-id="9f241-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9f241-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="9f241-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9f241-102">SYNOPSIS</span></span>
<span data-ttu-id="9f241-103">從 Azure 應用程式閘道移除 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="9f241-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="9f241-104">語法</span><span class="sxs-lookup"><span data-stu-id="9f241-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f241-105">描述</span><span class="sxs-lookup"><span data-stu-id="9f241-105">DESCRIPTION</span></span>
<span data-ttu-id="9f241-106">此Remove-AzApplicationGatewaySslPolicy Cmdlet 會從 Azure 應用程式閘道移除 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="9f241-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="9f241-107">例子</span><span class="sxs-lookup"><span data-stu-id="9f241-107">EXAMPLES</span></span>

### <span data-ttu-id="9f241-108">範例 1：從應用程式閘道移除 SSL 策略</span><span class="sxs-lookup"><span data-stu-id="9f241-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="9f241-109">此命令會從名為 ApplicationGateway01 的應用程式閘道移除 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="9f241-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="9f241-110">參數</span><span class="sxs-lookup"><span data-stu-id="9f241-110">PARAMETERS</span></span>

### <span data-ttu-id="9f241-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f241-111">-ApplicationGateway</span></span>
<span data-ttu-id="9f241-112">指定此 Cmdlet 會移除 SSL 策略的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="9f241-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="9f241-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f241-113">-DefaultProfile</span></span>
<span data-ttu-id="9f241-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f241-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f241-115">-強制</span><span class="sxs-lookup"><span data-stu-id="9f241-115">-Force</span></span>
<span data-ttu-id="9f241-116">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="9f241-116">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f241-117">-確認</span><span class="sxs-lookup"><span data-stu-id="9f241-117">-Confirm</span></span>
<span data-ttu-id="9f241-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9f241-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f241-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f241-119">-WhatIf</span></span>
<span data-ttu-id="9f241-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9f241-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f241-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f241-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f241-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f241-122">CommonParameters</span></span>
<span data-ttu-id="9f241-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9f241-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f241-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9f241-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f241-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9f241-125">INPUTS</span></span>

### <span data-ttu-id="9f241-126">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f241-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f241-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9f241-127">OUTPUTS</span></span>

### <span data-ttu-id="9f241-128">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f241-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f241-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9f241-129">NOTES</span></span>
<span data-ttu-id="9f241-130">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="9f241-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9f241-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f241-131">RELATED LINKS</span></span>

[<span data-ttu-id="9f241-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9f241-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="9f241-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9f241-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="9f241-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9f241-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

