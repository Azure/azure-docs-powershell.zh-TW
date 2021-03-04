---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e849b109ba1f1fd43ca960d56581357729f5c344
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916721"
---
# <span data-ttu-id="f8c75-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8c75-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f8c75-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f8c75-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c75-103">為應用程式閘道建立自動縮放組配置。</span><span class="sxs-lookup"><span data-stu-id="f8c75-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="f8c75-104">語法</span><span class="sxs-lookup"><span data-stu-id="f8c75-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8c75-105">描述</span><span class="sxs-lookup"><span data-stu-id="f8c75-105">DESCRIPTION</span></span>
<span data-ttu-id="f8c75-106">**New-AzApplicationGatewayAutoscaleConfiguration** Cmdlet 會為 Azure 應用程式閘道建立自動縮放組配置。</span><span class="sxs-lookup"><span data-stu-id="f8c75-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="f8c75-107">例子</span><span class="sxs-lookup"><span data-stu-id="f8c75-107">EXAMPLES</span></span>

### <span data-ttu-id="f8c75-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f8c75-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="f8c75-109">第一個命令會建立容量最低為 3 的自動縮放配置。</span><span class="sxs-lookup"><span data-stu-id="f8c75-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="f8c75-110">第二個命令會使用自動縮放設置建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="f8c75-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="f8c75-111">參數</span><span class="sxs-lookup"><span data-stu-id="f8c75-111">PARAMETERS</span></span>

### <span data-ttu-id="f8c75-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c75-112">-DefaultProfile</span></span>
<span data-ttu-id="f8c75-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8c75-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8c75-114">-Max可</span><span class="sxs-lookup"><span data-stu-id="f8c75-114">-MaxCapacity</span></span>
<span data-ttu-id="f8c75-115">應用程式閘道永遠可用並收費的最大容量單位。</span><span class="sxs-lookup"><span data-stu-id="f8c75-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="f8c75-116">-Min前小明</span><span class="sxs-lookup"><span data-stu-id="f8c75-116">-MinCapacity</span></span>
<span data-ttu-id="f8c75-117">應用程式閘道永遠可用並收費的最小容量單位。</span><span class="sxs-lookup"><span data-stu-id="f8c75-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="f8c75-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f8c75-118">-Confirm</span></span>
<span data-ttu-id="f8c75-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f8c75-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8c75-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8c75-120">-WhatIf</span></span>
<span data-ttu-id="f8c75-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8c75-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8c75-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8c75-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8c75-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c75-123">CommonParameters</span></span>
<span data-ttu-id="f8c75-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f8c75-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c75-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f8c75-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c75-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f8c75-126">INPUTS</span></span>

### <span data-ttu-id="f8c75-127">沒有</span><span class="sxs-lookup"><span data-stu-id="f8c75-127">None</span></span>

## <span data-ttu-id="f8c75-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f8c75-128">OUTPUTS</span></span>

### <span data-ttu-id="f8c75-129">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8c75-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f8c75-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f8c75-130">NOTES</span></span>

## <span data-ttu-id="f8c75-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8c75-131">RELATED LINKS</span></span>

[<span data-ttu-id="f8c75-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8c75-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="f8c75-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8c75-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="f8c75-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8c75-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
