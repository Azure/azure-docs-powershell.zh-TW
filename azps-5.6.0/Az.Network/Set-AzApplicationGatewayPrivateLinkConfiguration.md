---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: e01404958156967c6881655ab42eb965152ebaaf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902358"
---
# <span data-ttu-id="92fbb-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="92fbb-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="92fbb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="92fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="92fbb-103">修改應用程式閘道的 PrivateLink 群組原則。</span><span class="sxs-lookup"><span data-stu-id="92fbb-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="92fbb-104">語法</span><span class="sxs-lookup"><span data-stu-id="92fbb-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92fbb-105">描述</span><span class="sxs-lookup"><span data-stu-id="92fbb-105">DESCRIPTION</span></span>
<span data-ttu-id="92fbb-106">**Set-AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會修改 Azure 應用程式閘道的 privateLink 設定。</span><span class="sxs-lookup"><span data-stu-id="92fbb-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="92fbb-107">例子</span><span class="sxs-lookup"><span data-stu-id="92fbb-107">EXAMPLES</span></span>

### <span data-ttu-id="92fbb-108">範例 1：設定 PrivateLink 設定</span><span class="sxs-lookup"><span data-stu-id="92fbb-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="92fbb-109">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="92fbb-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="92fbb-110">第二個命令會設定 privateLink 設定與名稱 privateLinkConfig01，以使用儲存在 $privateLinkIpConfiguration 01 中的 ip 設定</span><span class="sxs-lookup"><span data-stu-id="92fbb-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="92fbb-111">參數</span><span class="sxs-lookup"><span data-stu-id="92fbb-111">PARAMETERS</span></span>

### <span data-ttu-id="92fbb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92fbb-112">-ApplicationGateway</span></span>
<span data-ttu-id="92fbb-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="92fbb-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92fbb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92fbb-114">-DefaultProfile</span></span>
<span data-ttu-id="92fbb-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="92fbb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92fbb-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="92fbb-116">-IpConfiguration</span></span>
<span data-ttu-id="92fbb-117">ipConfiguration 清單</span><span class="sxs-lookup"><span data-stu-id="92fbb-117">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92fbb-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="92fbb-118">-Name</span></span>
<span data-ttu-id="92fbb-119">privateLink 組組的名稱</span><span class="sxs-lookup"><span data-stu-id="92fbb-119">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92fbb-120">-確認</span><span class="sxs-lookup"><span data-stu-id="92fbb-120">-Confirm</span></span>
<span data-ttu-id="92fbb-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="92fbb-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92fbb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92fbb-122">-WhatIf</span></span>
<span data-ttu-id="92fbb-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92fbb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92fbb-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92fbb-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92fbb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92fbb-125">CommonParameters</span></span>
<span data-ttu-id="92fbb-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="92fbb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92fbb-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92fbb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92fbb-128">輸入</span><span class="sxs-lookup"><span data-stu-id="92fbb-128">INPUTS</span></span>

### <span data-ttu-id="92fbb-129">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92fbb-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="92fbb-130">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="92fbb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="92fbb-131">輸出</span><span class="sxs-lookup"><span data-stu-id="92fbb-131">OUTPUTS</span></span>

### <span data-ttu-id="92fbb-132">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92fbb-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92fbb-133">筆記</span><span class="sxs-lookup"><span data-stu-id="92fbb-133">NOTES</span></span>

## <span data-ttu-id="92fbb-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="92fbb-134">RELATED LINKS</span></span>

[<span data-ttu-id="92fbb-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="92fbb-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="92fbb-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="92fbb-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="92fbb-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="92fbb-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="92fbb-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="92fbb-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)