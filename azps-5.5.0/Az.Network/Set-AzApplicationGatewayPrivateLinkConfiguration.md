---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128706"
---
# <span data-ttu-id="0fc85-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fc85-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="0fc85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0fc85-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc85-103">修改應用程式閘道的 PrivateLink 配置。</span><span class="sxs-lookup"><span data-stu-id="0fc85-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="0fc85-104">句法</span><span class="sxs-lookup"><span data-stu-id="0fc85-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fc85-105">說明</span><span class="sxs-lookup"><span data-stu-id="0fc85-105">DESCRIPTION</span></span>
<span data-ttu-id="0fc85-106">**AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會修改 Azure 應用程式閘道的 privateLink 設定。</span><span class="sxs-lookup"><span data-stu-id="0fc85-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="0fc85-107">示例</span><span class="sxs-lookup"><span data-stu-id="0fc85-107">EXAMPLES</span></span>

### <span data-ttu-id="0fc85-108">範例1：設定 PrivateLink 設定</span><span class="sxs-lookup"><span data-stu-id="0fc85-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="0fc85-109">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="0fc85-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0fc85-110">第二個命令會將名稱為 privateLinkConfig01 的 privateLink 設定設定為使用 $privateLinkIpConfiguration 01 中儲存的 ip 配置</span><span class="sxs-lookup"><span data-stu-id="0fc85-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="0fc85-111">參數</span><span class="sxs-lookup"><span data-stu-id="0fc85-111">PARAMETERS</span></span>

### <span data-ttu-id="0fc85-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fc85-112">-ApplicationGateway</span></span>
<span data-ttu-id="0fc85-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fc85-113">The applicationGateway</span></span>

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

### <span data-ttu-id="0fc85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc85-114">-DefaultProfile</span></span>
<span data-ttu-id="0fc85-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0fc85-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc85-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fc85-116">-IpConfiguration</span></span>
<span data-ttu-id="0fc85-117">IpConfiguration 清單</span><span class="sxs-lookup"><span data-stu-id="0fc85-117">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="0fc85-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="0fc85-118">-Name</span></span>
<span data-ttu-id="0fc85-119">PrivateLink 配置的名稱</span><span class="sxs-lookup"><span data-stu-id="0fc85-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="0fc85-120">-確認</span><span class="sxs-lookup"><span data-stu-id="0fc85-120">-Confirm</span></span>
<span data-ttu-id="0fc85-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0fc85-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fc85-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fc85-122">-WhatIf</span></span>
<span data-ttu-id="0fc85-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0fc85-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fc85-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0fc85-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fc85-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc85-125">CommonParameters</span></span>
<span data-ttu-id="0fc85-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0fc85-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc85-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0fc85-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc85-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0fc85-128">INPUTS</span></span>

### <span data-ttu-id="0fc85-129">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0fc85-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="0fc85-130">PSApplicationGatewayPrivateLinkIpConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="0fc85-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="0fc85-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0fc85-131">OUTPUTS</span></span>

### <span data-ttu-id="0fc85-132">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0fc85-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0fc85-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0fc85-133">NOTES</span></span>

## <span data-ttu-id="0fc85-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0fc85-134">RELATED LINKS</span></span>

[<span data-ttu-id="0fc85-135">新-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fc85-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="0fc85-136">附加 AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fc85-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="0fc85-137">AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fc85-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="0fc85-138">移除-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fc85-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)