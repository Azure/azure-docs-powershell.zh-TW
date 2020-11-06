---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 2d7fa9dd9030f1e5878293276a248c2f6718efe5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451131"
---
# <span data-ttu-id="1b1b3-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b1b3-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="1b1b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1b3-103">更新應用程式閘道的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-103">Updates Autoscale Configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b1b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b1b3-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 -MinCapacity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b1b3-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b1b3-105">DESCRIPTION</span></span>
<span data-ttu-id="1b1b3-106">**AzureRmApplicationGatewayAutoscaleConfiguration** Cmdlet 會修改應用程式閘道的現有自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-106">The **Set-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="1b1b3-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b1b3-107">EXAMPLES</span></span>

### <span data-ttu-id="1b1b3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1b1b3-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="1b1b3-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="1b1b3-110">第二個命令會從 applicationg 閘道更新自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="1b1b3-111">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="1b1b3-112">參數</span><span class="sxs-lookup"><span data-stu-id="1b1b3-112">PARAMETERS</span></span>

### <span data-ttu-id="1b1b3-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b1b3-113">-ApplicationGateway</span></span>
<span data-ttu-id="1b1b3-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b1b3-114">The applicationGateway</span></span>

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

### <span data-ttu-id="1b1b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1b3-115">-DefaultProfile</span></span>
<span data-ttu-id="1b1b3-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1b3-117">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="1b1b3-117">-MinCapacity</span></span>
<span data-ttu-id="1b1b3-118">應用程式閘道的最小 capcity。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-118">Minimum capcity for application gateway.</span></span>

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

### <span data-ttu-id="1b1b3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="1b1b3-119">-Confirm</span></span>
<span data-ttu-id="1b1b3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b1b3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b1b3-121">-WhatIf</span></span>
<span data-ttu-id="1b1b3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b1b3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b1b3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1b3-124">CommonParameters</span></span>
<span data-ttu-id="1b1b3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1b3-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b1b3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1b3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1b1b3-127">INPUTS</span></span>

### <span data-ttu-id="1b1b3-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1b1b3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1b1b3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1b1b3-129">OUTPUTS</span></span>

### <span data-ttu-id="1b1b3-130">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1b1b3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1b1b3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1b1b3-131">NOTES</span></span>

## <span data-ttu-id="1b1b3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b1b3-132">RELATED LINKS</span></span>
