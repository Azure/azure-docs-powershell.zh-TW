---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: cf9e847454fc638afc3c25cc3b5d8f0e78ef2fb0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437463"
---
# <span data-ttu-id="8b2c7-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b2c7-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="8b2c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2c7-103">更新應用程式閘道的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="8b2c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b2c7-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b2c7-105">說明</span><span class="sxs-lookup"><span data-stu-id="8b2c7-105">DESCRIPTION</span></span>
<span data-ttu-id="8b2c7-106">**AzApplicationGatewayAutoscaleConfiguration** Cmdlet 會修改應用程式閘道的現有自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="8b2c7-107">示例</span><span class="sxs-lookup"><span data-stu-id="8b2c7-107">EXAMPLES</span></span>

### <span data-ttu-id="8b2c7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8b2c7-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="8b2c7-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="8b2c7-110">第二個命令會從應用程式閘道更新自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="8b2c7-111">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="8b2c7-112">參數</span><span class="sxs-lookup"><span data-stu-id="8b2c7-112">PARAMETERS</span></span>

### <span data-ttu-id="8b2c7-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b2c7-113">-ApplicationGateway</span></span>
<span data-ttu-id="8b2c7-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b2c7-114">The applicationGateway</span></span>

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

### <span data-ttu-id="8b2c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2c7-115">-DefaultProfile</span></span>
<span data-ttu-id="8b2c7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b2c7-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="8b2c7-117">-MaxCapacity</span></span>
<span data-ttu-id="8b2c7-118">應用程式閘道的最大容量。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="8b2c7-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="8b2c7-119">-MinCapacity</span></span>
<span data-ttu-id="8b2c7-120">應用程式閘道的最小容量。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="8b2c7-121">-確認</span><span class="sxs-lookup"><span data-stu-id="8b2c7-121">-Confirm</span></span>
<span data-ttu-id="8b2c7-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b2c7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b2c7-123">-WhatIf</span></span>
<span data-ttu-id="8b2c7-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b2c7-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b2c7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2c7-126">CommonParameters</span></span>
<span data-ttu-id="8b2c7-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2c7-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b2c7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2c7-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8b2c7-129">INPUTS</span></span>

### <span data-ttu-id="8b2c7-130">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8b2c7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b2c7-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8b2c7-131">OUTPUTS</span></span>

### <span data-ttu-id="8b2c7-132">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8b2c7-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b2c7-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8b2c7-133">NOTES</span></span>

## <span data-ttu-id="8b2c7-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b2c7-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b2c7-135">AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b2c7-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="8b2c7-136">新-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b2c7-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="8b2c7-137">移除-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b2c7-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
