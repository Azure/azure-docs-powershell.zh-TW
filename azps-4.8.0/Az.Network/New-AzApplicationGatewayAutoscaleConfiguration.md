---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136326"
---
# <span data-ttu-id="00a73-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="00a73-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="00a73-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00a73-102">SYNOPSIS</span></span>
<span data-ttu-id="00a73-103">建立應用程式閘道的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="00a73-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="00a73-104">句法</span><span class="sxs-lookup"><span data-stu-id="00a73-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00a73-105">說明</span><span class="sxs-lookup"><span data-stu-id="00a73-105">DESCRIPTION</span></span>
<span data-ttu-id="00a73-106">**新的-AzApplicationGatewayAutoscaleConfiguration** Cmdlet 會針對 Azure 應用程式閘道建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="00a73-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="00a73-107">示例</span><span class="sxs-lookup"><span data-stu-id="00a73-107">EXAMPLES</span></span>

### <span data-ttu-id="00a73-108">範例1</span><span class="sxs-lookup"><span data-stu-id="00a73-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="00a73-109">第一個命令會建立含最小容量3的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="00a73-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="00a73-110">第二個命令會建立具有自動縮放設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="00a73-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="00a73-111">參數</span><span class="sxs-lookup"><span data-stu-id="00a73-111">PARAMETERS</span></span>

### <span data-ttu-id="00a73-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a73-112">-DefaultProfile</span></span>
<span data-ttu-id="00a73-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00a73-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00a73-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="00a73-114">-MaxCapacity</span></span>
<span data-ttu-id="00a73-115">應用程式閘道總可使用的最大容量單位（並收取費用）。</span><span class="sxs-lookup"><span data-stu-id="00a73-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="00a73-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="00a73-116">-MinCapacity</span></span>
<span data-ttu-id="00a73-117">應用程式閘道總可使用的最小容量單位（並收取費用）。</span><span class="sxs-lookup"><span data-stu-id="00a73-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="00a73-118">-確認</span><span class="sxs-lookup"><span data-stu-id="00a73-118">-Confirm</span></span>
<span data-ttu-id="00a73-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="00a73-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00a73-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00a73-120">-WhatIf</span></span>
<span data-ttu-id="00a73-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00a73-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00a73-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00a73-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00a73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a73-123">CommonParameters</span></span>
<span data-ttu-id="00a73-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00a73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a73-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00a73-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a73-126">輸入</span><span class="sxs-lookup"><span data-stu-id="00a73-126">INPUTS</span></span>

### <span data-ttu-id="00a73-127">所有</span><span class="sxs-lookup"><span data-stu-id="00a73-127">None</span></span>

## <span data-ttu-id="00a73-128">輸出</span><span class="sxs-lookup"><span data-stu-id="00a73-128">OUTPUTS</span></span>

### <span data-ttu-id="00a73-129">PSApplicationGatewayAutoscaleConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="00a73-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="00a73-130">筆記</span><span class="sxs-lookup"><span data-stu-id="00a73-130">NOTES</span></span>

## <span data-ttu-id="00a73-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="00a73-131">RELATED LINKS</span></span>

[<span data-ttu-id="00a73-132">AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="00a73-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="00a73-133">移除-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="00a73-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="00a73-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="00a73-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
