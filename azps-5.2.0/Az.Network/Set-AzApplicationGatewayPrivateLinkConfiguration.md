---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284244"
---
# <span data-ttu-id="2ad9c-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ad9c-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="2ad9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ad9c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad9c-103">修改應用程式閘道的 PrivateLink 配置。</span><span class="sxs-lookup"><span data-stu-id="2ad9c-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="2ad9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ad9c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ad9c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ad9c-105">DESCRIPTION</span></span>
<span data-ttu-id="2ad9c-106">**AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會修改 Azure 應用程式閘道的 privateLink 設定。</span><span class="sxs-lookup"><span data-stu-id="2ad9c-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="2ad9c-107">示例</span><span class="sxs-lookup"><span data-stu-id="2ad9c-107">EXAMPLES</span></span>

### <span data-ttu-id="2ad9c-108">範例1：設定 PrivateLink 設定</span><span class="sxs-lookup"><span data-stu-id="2ad9c-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="2ad9c-109">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="2ad9c-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2ad9c-110">第二個命令會將名稱為 privateLinkConfig01 的 privateLink 設定設定為使用 $privateLinkIpConfiguration 01 中儲存的 ip 配置</span><span class="sxs-lookup"><span data-stu-id="2ad9c-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="2ad9c-111">參數</span><span class="sxs-lookup"><span data-stu-id="2ad9c-111">PARAMETERS</span></span>

### <span data-ttu-id="2ad9c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ad9c-112">-ApplicationGateway</span></span>
<span data-ttu-id="2ad9c-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ad9c-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2ad9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad9c-114">-DefaultProfile</span></span>
<span data-ttu-id="2ad9c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ad9c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ad9c-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ad9c-116">-IpConfiguration</span></span>
<span data-ttu-id="2ad9c-117">IpConfiguration 清單</span><span class="sxs-lookup"><span data-stu-id="2ad9c-117">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="2ad9c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ad9c-118">-Name</span></span>
<span data-ttu-id="2ad9c-119">PrivateLink 配置的名稱</span><span class="sxs-lookup"><span data-stu-id="2ad9c-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="2ad9c-120">-確認</span><span class="sxs-lookup"><span data-stu-id="2ad9c-120">-Confirm</span></span>
<span data-ttu-id="2ad9c-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2ad9c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ad9c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ad9c-122">-WhatIf</span></span>
<span data-ttu-id="2ad9c-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ad9c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ad9c-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ad9c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ad9c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad9c-125">CommonParameters</span></span>
<span data-ttu-id="2ad9c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ad9c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad9c-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2ad9c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad9c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2ad9c-128">INPUTS</span></span>

### <span data-ttu-id="2ad9c-129">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2ad9c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="2ad9c-130">PSApplicationGatewayPrivateLinkIpConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="2ad9c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="2ad9c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2ad9c-131">OUTPUTS</span></span>

### <span data-ttu-id="2ad9c-132">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2ad9c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2ad9c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2ad9c-133">NOTES</span></span>

## <span data-ttu-id="2ad9c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ad9c-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ad9c-135">新-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ad9c-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2ad9c-136">附加 AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ad9c-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2ad9c-137">AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ad9c-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2ad9c-138">移除-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ad9c-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)