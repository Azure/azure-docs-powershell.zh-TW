---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e6321125958b872d15f60bbe433819c4c6f1d7ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917677"
---
# <span data-ttu-id="ae84c-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae84c-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ae84c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ae84c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae84c-103">移除應用程式閘道的自動縮放組配置。</span><span class="sxs-lookup"><span data-stu-id="ae84c-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="ae84c-104">語法</span><span class="sxs-lookup"><span data-stu-id="ae84c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae84c-105">描述</span><span class="sxs-lookup"><span data-stu-id="ae84c-105">DESCRIPTION</span></span>
<span data-ttu-id="ae84c-106">**Remove-AzApplicationGatewayAutoscaleConfiguration** Cmdlet 會從現有的應用程式閘道移除自動縮放組式。</span><span class="sxs-lookup"><span data-stu-id="ae84c-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="ae84c-107">例子</span><span class="sxs-lookup"><span data-stu-id="ae84c-107">EXAMPLES</span></span>

### <span data-ttu-id="ae84c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ae84c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="ae84c-109">第一個命令會獲得應用程式閘道，並儲存在$gw變數中。</span><span class="sxs-lookup"><span data-stu-id="ae84c-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="ae84c-110">第二個命令會從應用程式閘道移除自動縮放設置。</span><span class="sxs-lookup"><span data-stu-id="ae84c-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="ae84c-111">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ae84c-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="ae84c-112">參數</span><span class="sxs-lookup"><span data-stu-id="ae84c-112">PARAMETERS</span></span>

### <span data-ttu-id="ae84c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae84c-113">-ApplicationGateway</span></span>
<span data-ttu-id="ae84c-114">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="ae84c-114">The applicationGateway</span></span>

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

### <span data-ttu-id="ae84c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae84c-115">-DefaultProfile</span></span>
<span data-ttu-id="ae84c-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae84c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae84c-117">-強制</span><span class="sxs-lookup"><span data-stu-id="ae84c-117">-Force</span></span>
<span data-ttu-id="ae84c-118">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="ae84c-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ae84c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="ae84c-119">-Confirm</span></span>
<span data-ttu-id="ae84c-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ae84c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae84c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae84c-121">-WhatIf</span></span>
<span data-ttu-id="ae84c-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae84c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae84c-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae84c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae84c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae84c-124">CommonParameters</span></span>
<span data-ttu-id="ae84c-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ae84c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae84c-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ae84c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae84c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ae84c-127">INPUTS</span></span>

### <span data-ttu-id="ae84c-128">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae84c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae84c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ae84c-129">OUTPUTS</span></span>

### <span data-ttu-id="ae84c-130">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae84c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae84c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="ae84c-131">NOTES</span></span>

## <span data-ttu-id="ae84c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae84c-132">RELATED LINKS</span></span>

[<span data-ttu-id="ae84c-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae84c-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ae84c-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae84c-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ae84c-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae84c-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
