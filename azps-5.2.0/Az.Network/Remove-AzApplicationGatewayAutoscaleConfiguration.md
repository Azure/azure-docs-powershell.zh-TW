---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275135"
---
# <span data-ttu-id="152bc-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="152bc-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="152bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="152bc-102">SYNOPSIS</span></span>
<span data-ttu-id="152bc-103">從應用程式閘道移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="152bc-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="152bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="152bc-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="152bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="152bc-105">DESCRIPTION</span></span>
<span data-ttu-id="152bc-106">**AzApplicationGatewayAutoscaleConfiguration** Cmdlet 會從現有的應用程式閘道中移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="152bc-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="152bc-107">示例</span><span class="sxs-lookup"><span data-stu-id="152bc-107">EXAMPLES</span></span>

### <span data-ttu-id="152bc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="152bc-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="152bc-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="152bc-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="152bc-110">第二個命令會從應用程式閘道中移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="152bc-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="152bc-111">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="152bc-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="152bc-112">參數</span><span class="sxs-lookup"><span data-stu-id="152bc-112">PARAMETERS</span></span>

### <span data-ttu-id="152bc-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="152bc-113">-ApplicationGateway</span></span>
<span data-ttu-id="152bc-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="152bc-114">The applicationGateway</span></span>

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

### <span data-ttu-id="152bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152bc-115">-DefaultProfile</span></span>
<span data-ttu-id="152bc-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="152bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="152bc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="152bc-117">-Force</span></span>
<span data-ttu-id="152bc-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="152bc-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="152bc-119">-確認</span><span class="sxs-lookup"><span data-stu-id="152bc-119">-Confirm</span></span>
<span data-ttu-id="152bc-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="152bc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="152bc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="152bc-121">-WhatIf</span></span>
<span data-ttu-id="152bc-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="152bc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="152bc-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="152bc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="152bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152bc-124">CommonParameters</span></span>
<span data-ttu-id="152bc-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="152bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152bc-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="152bc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152bc-127">輸入</span><span class="sxs-lookup"><span data-stu-id="152bc-127">INPUTS</span></span>

### <span data-ttu-id="152bc-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="152bc-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="152bc-129">輸出</span><span class="sxs-lookup"><span data-stu-id="152bc-129">OUTPUTS</span></span>

### <span data-ttu-id="152bc-130">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="152bc-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="152bc-131">筆記</span><span class="sxs-lookup"><span data-stu-id="152bc-131">NOTES</span></span>

## <span data-ttu-id="152bc-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="152bc-132">RELATED LINKS</span></span>

[<span data-ttu-id="152bc-133">AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="152bc-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="152bc-134">新-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="152bc-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="152bc-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="152bc-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
