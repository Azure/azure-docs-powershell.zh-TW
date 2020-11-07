---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 517327ab3af1665d70f3d2f8eff4594d708a2f85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789178"
---
# <span data-ttu-id="55611-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="55611-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="55611-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55611-102">SYNOPSIS</span></span>
<span data-ttu-id="55611-103">從 Azure 應用程式閘道移除 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="55611-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="55611-104">句法</span><span class="sxs-lookup"><span data-stu-id="55611-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55611-105">說明</span><span class="sxs-lookup"><span data-stu-id="55611-105">DESCRIPTION</span></span>
<span data-ttu-id="55611-106">Remove-AzApplicationGatewaySslPolicy Cmdlet 會從 Azure 應用程式閘道移除 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="55611-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="55611-107">示例</span><span class="sxs-lookup"><span data-stu-id="55611-107">EXAMPLES</span></span>

### <span data-ttu-id="55611-108">範例1：從應用程式閘道移除 SSL 原則</span><span class="sxs-lookup"><span data-stu-id="55611-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="55611-109">這個命令會從名為 ApplicationGateway01 的應用程式閘道中移除 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="55611-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="55611-110">參數</span><span class="sxs-lookup"><span data-stu-id="55611-110">PARAMETERS</span></span>

### <span data-ttu-id="55611-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="55611-111">-ApplicationGateway</span></span>
<span data-ttu-id="55611-112">指定此 Cmdlet 移除 SSL 原則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="55611-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="55611-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55611-113">-DefaultProfile</span></span>
<span data-ttu-id="55611-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55611-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55611-115">-Force</span><span class="sxs-lookup"><span data-stu-id="55611-115">-Force</span></span>
<span data-ttu-id="55611-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="55611-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="55611-117">-確認</span><span class="sxs-lookup"><span data-stu-id="55611-117">-Confirm</span></span>
<span data-ttu-id="55611-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55611-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55611-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55611-119">-WhatIf</span></span>
<span data-ttu-id="55611-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55611-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55611-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55611-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55611-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55611-122">CommonParameters</span></span>
<span data-ttu-id="55611-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55611-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55611-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55611-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55611-125">輸入</span><span class="sxs-lookup"><span data-stu-id="55611-125">INPUTS</span></span>

### <span data-ttu-id="55611-126">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55611-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="55611-127">輸出</span><span class="sxs-lookup"><span data-stu-id="55611-127">OUTPUTS</span></span>

### <span data-ttu-id="55611-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55611-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="55611-129">筆記</span><span class="sxs-lookup"><span data-stu-id="55611-129">NOTES</span></span>
<span data-ttu-id="55611-130">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="55611-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="55611-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="55611-131">RELATED LINKS</span></span>

[<span data-ttu-id="55611-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="55611-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="55611-133">新-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="55611-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="55611-134">AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="55611-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

