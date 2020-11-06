---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 884ff52132af34dad7c4498653233f0b122555ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455192"
---
# <span data-ttu-id="87307-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="87307-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="87307-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87307-102">SYNOPSIS</span></span>
<span data-ttu-id="87307-103">從應用程式閘道移除 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="87307-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87307-104">句法</span><span class="sxs-lookup"><span data-stu-id="87307-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87307-105">說明</span><span class="sxs-lookup"><span data-stu-id="87307-105">DESCRIPTION</span></span>
<span data-ttu-id="87307-106">**AzureRmApplicationGatewayIPConfiguration** Cmdlet 會從 Azure 應用程式閘道中移除 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="87307-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="87307-107">示例</span><span class="sxs-lookup"><span data-stu-id="87307-107">EXAMPLES</span></span>

### <span data-ttu-id="87307-108">範例1：從 Azure 應用程式閘道移除 IP 設定</span><span class="sxs-lookup"><span data-stu-id="87307-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="87307-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="87307-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="87307-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 Subnet02 的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="87307-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="87307-111">參數</span><span class="sxs-lookup"><span data-stu-id="87307-111">PARAMETERS</span></span>

### <span data-ttu-id="87307-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="87307-112">-ApplicationGateway</span></span>
<span data-ttu-id="87307-113">指定要從中移除 IP 配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="87307-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="87307-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87307-114">-DefaultProfile</span></span>
<span data-ttu-id="87307-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87307-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87307-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="87307-116">-Name</span></span>
<span data-ttu-id="87307-117">指定要移除的 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="87307-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="87307-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87307-118">CommonParameters</span></span>
<span data-ttu-id="87307-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87307-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87307-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87307-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87307-121">輸入</span><span class="sxs-lookup"><span data-stu-id="87307-121">INPUTS</span></span>

### <span data-ttu-id="87307-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="87307-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="87307-123">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="87307-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="87307-124">輸出</span><span class="sxs-lookup"><span data-stu-id="87307-124">OUTPUTS</span></span>

### <span data-ttu-id="87307-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="87307-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="87307-126">筆記</span><span class="sxs-lookup"><span data-stu-id="87307-126">NOTES</span></span>

## <span data-ttu-id="87307-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="87307-127">RELATED LINKS</span></span>

[<span data-ttu-id="87307-128">附加 AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="87307-128">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="87307-129">AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="87307-129">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="87307-130">新-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="87307-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="87307-131">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="87307-131">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


