---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 80248749772bdcfc26bbbc633bbb4919531462be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789201"
---
# <span data-ttu-id="acbeb-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="acbeb-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="acbeb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acbeb-102">SYNOPSIS</span></span>
<span data-ttu-id="acbeb-103">從應用程式閘道移除 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="acbeb-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="acbeb-104">句法</span><span class="sxs-lookup"><span data-stu-id="acbeb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acbeb-105">說明</span><span class="sxs-lookup"><span data-stu-id="acbeb-105">DESCRIPTION</span></span>
<span data-ttu-id="acbeb-106">**AzApplicationGatewayIPConfiguration** Cmdlet 會從 Azure 應用程式閘道中移除 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="acbeb-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="acbeb-107">示例</span><span class="sxs-lookup"><span data-stu-id="acbeb-107">EXAMPLES</span></span>

### <span data-ttu-id="acbeb-108">範例1：從 Azure 應用程式閘道移除 IP 設定</span><span class="sxs-lookup"><span data-stu-id="acbeb-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="acbeb-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="acbeb-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="acbeb-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 Subnet02 的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="acbeb-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="acbeb-111">參數</span><span class="sxs-lookup"><span data-stu-id="acbeb-111">PARAMETERS</span></span>

### <span data-ttu-id="acbeb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="acbeb-112">-ApplicationGateway</span></span>
<span data-ttu-id="acbeb-113">指定要從中移除 IP 配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="acbeb-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="acbeb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbeb-114">-DefaultProfile</span></span>
<span data-ttu-id="acbeb-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acbeb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acbeb-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="acbeb-116">-Name</span></span>
<span data-ttu-id="acbeb-117">指定要移除的 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="acbeb-117">Specifies the name of the IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbeb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbeb-118">CommonParameters</span></span>
<span data-ttu-id="acbeb-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acbeb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbeb-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="acbeb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbeb-121">輸入</span><span class="sxs-lookup"><span data-stu-id="acbeb-121">INPUTS</span></span>

### <span data-ttu-id="acbeb-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="acbeb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="acbeb-123">輸出</span><span class="sxs-lookup"><span data-stu-id="acbeb-123">OUTPUTS</span></span>

### <span data-ttu-id="acbeb-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="acbeb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="acbeb-125">筆記</span><span class="sxs-lookup"><span data-stu-id="acbeb-125">NOTES</span></span>

## <span data-ttu-id="acbeb-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="acbeb-126">RELATED LINKS</span></span>

[<span data-ttu-id="acbeb-127">附加 AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="acbeb-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="acbeb-128">AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="acbeb-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="acbeb-129">新-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="acbeb-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="acbeb-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="acbeb-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


