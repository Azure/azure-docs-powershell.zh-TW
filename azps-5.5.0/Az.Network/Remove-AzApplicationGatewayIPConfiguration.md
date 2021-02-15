---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142137"
---
# <span data-ttu-id="1bef5-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bef5-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="1bef5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1bef5-102">SYNOPSIS</span></span>
<span data-ttu-id="1bef5-103">從應用程式閘道移除 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="1bef5-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="1bef5-104">句法</span><span class="sxs-lookup"><span data-stu-id="1bef5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bef5-105">說明</span><span class="sxs-lookup"><span data-stu-id="1bef5-105">DESCRIPTION</span></span>
<span data-ttu-id="1bef5-106">**AzApplicationGatewayIPConfiguration** Cmdlet 會從 Azure 應用程式閘道中移除 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="1bef5-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="1bef5-107">示例</span><span class="sxs-lookup"><span data-stu-id="1bef5-107">EXAMPLES</span></span>

### <span data-ttu-id="1bef5-108">範例1：從 Azure 應用程式閘道移除 IP 設定</span><span class="sxs-lookup"><span data-stu-id="1bef5-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="1bef5-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="1bef5-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1bef5-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 Subnet02 的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="1bef5-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1bef5-111">參數</span><span class="sxs-lookup"><span data-stu-id="1bef5-111">PARAMETERS</span></span>

### <span data-ttu-id="1bef5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bef5-112">-ApplicationGateway</span></span>
<span data-ttu-id="1bef5-113">指定要從中移除 IP 配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1bef5-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="1bef5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bef5-114">-DefaultProfile</span></span>
<span data-ttu-id="1bef5-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bef5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bef5-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="1bef5-116">-Name</span></span>
<span data-ttu-id="1bef5-117">指定要移除的 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="1bef5-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="1bef5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bef5-118">CommonParameters</span></span>
<span data-ttu-id="1bef5-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1bef5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bef5-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1bef5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bef5-121">輸入</span><span class="sxs-lookup"><span data-stu-id="1bef5-121">INPUTS</span></span>

### <span data-ttu-id="1bef5-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1bef5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1bef5-123">輸出</span><span class="sxs-lookup"><span data-stu-id="1bef5-123">OUTPUTS</span></span>

### <span data-ttu-id="1bef5-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1bef5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1bef5-125">筆記</span><span class="sxs-lookup"><span data-stu-id="1bef5-125">NOTES</span></span>

## <span data-ttu-id="1bef5-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bef5-126">RELATED LINKS</span></span>

[<span data-ttu-id="1bef5-127">附加 AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bef5-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1bef5-128">AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bef5-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1bef5-129">新-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bef5-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1bef5-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bef5-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


