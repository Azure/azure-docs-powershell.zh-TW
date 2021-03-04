---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: bfa5cbfdb8ab734a8c6ca8b651808213b9b10f3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903450"
---
# <span data-ttu-id="f9ef4-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ef4-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f9ef4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f9ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ef4-103">更新應用程式閘道的自動縮放組配置。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="f9ef4-104">語法</span><span class="sxs-lookup"><span data-stu-id="f9ef4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9ef4-105">描述</span><span class="sxs-lookup"><span data-stu-id="f9ef4-105">DESCRIPTION</span></span>
<span data-ttu-id="f9ef4-106">**Set-AzApplicationGatewayAutoscaleConfiguration** Cmdlet 會修改應用程式閘道的現有自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="f9ef4-107">例子</span><span class="sxs-lookup"><span data-stu-id="f9ef4-107">EXAMPLES</span></span>

### <span data-ttu-id="f9ef4-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f9ef4-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="f9ef4-109">第一個命令會獲得應用程式閘道，並儲存在$gw變數中。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="f9ef4-110">第二個命令會更新應用程式閘道的自動縮放配置。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="f9ef4-111">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="f9ef4-112">參數</span><span class="sxs-lookup"><span data-stu-id="f9ef4-112">PARAMETERS</span></span>

### <span data-ttu-id="f9ef4-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9ef4-113">-ApplicationGateway</span></span>
<span data-ttu-id="f9ef4-114">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="f9ef4-114">The applicationGateway</span></span>

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

### <span data-ttu-id="f9ef4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ef4-115">-DefaultProfile</span></span>
<span data-ttu-id="f9ef4-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9ef4-117">-Max可</span><span class="sxs-lookup"><span data-stu-id="f9ef4-117">-MaxCapacity</span></span>
<span data-ttu-id="f9ef4-118">應用程式閘道的最大容量。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-118">Maximum capacity for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ef4-119">-Min前小明</span><span class="sxs-lookup"><span data-stu-id="f9ef4-119">-MinCapacity</span></span>
<span data-ttu-id="f9ef4-120">應用程式閘道的最小容量。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-120">Minimum capacity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ef4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="f9ef4-121">-Confirm</span></span>
<span data-ttu-id="f9ef4-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9ef4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ef4-123">-WhatIf</span></span>
<span data-ttu-id="f9ef4-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9ef4-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9ef4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ef4-126">CommonParameters</span></span>
<span data-ttu-id="f9ef4-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ef4-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f9ef4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ef4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f9ef4-129">INPUTS</span></span>

### <span data-ttu-id="f9ef4-130">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9ef4-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f9ef4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f9ef4-131">OUTPUTS</span></span>

### <span data-ttu-id="f9ef4-132">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9ef4-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f9ef4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f9ef4-133">NOTES</span></span>

## <span data-ttu-id="f9ef4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9ef4-134">RELATED LINKS</span></span>

[<span data-ttu-id="f9ef4-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ef4-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="f9ef4-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ef4-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="f9ef4-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ef4-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
