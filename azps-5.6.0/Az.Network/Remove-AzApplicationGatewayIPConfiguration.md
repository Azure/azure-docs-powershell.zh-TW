---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 610fe3f2ba4867dc1145488dfe789dba051b23bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910981"
---
# <span data-ttu-id="c3e25-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3e25-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="c3e25-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c3e25-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e25-103">從應用程式閘道移除 IP 組。</span><span class="sxs-lookup"><span data-stu-id="c3e25-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="c3e25-104">語法</span><span class="sxs-lookup"><span data-stu-id="c3e25-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e25-105">描述</span><span class="sxs-lookup"><span data-stu-id="c3e25-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e25-106">**Remove-AzApplicationGatewayIPConfiguration** Cmdlet 會從 Azure 應用程式閘道移除 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="c3e25-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="c3e25-107">例子</span><span class="sxs-lookup"><span data-stu-id="c3e25-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e25-108">範例 1：從 Azure 應用程式閘道移除 IP 組</span><span class="sxs-lookup"><span data-stu-id="c3e25-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="c3e25-109">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="c3e25-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c3e25-110">第二個命令會從儲存在 $AppGw 的應用程式閘道移除名為子網02 的 IP $AppGw。</span><span class="sxs-lookup"><span data-stu-id="c3e25-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c3e25-111">參數</span><span class="sxs-lookup"><span data-stu-id="c3e25-111">PARAMETERS</span></span>

### <span data-ttu-id="c3e25-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3e25-112">-ApplicationGateway</span></span>
<span data-ttu-id="c3e25-113">指定要從中移除 IP 群組原則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c3e25-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="c3e25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e25-114">-DefaultProfile</span></span>
<span data-ttu-id="c3e25-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3e25-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3e25-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3e25-116">-Name</span></span>
<span data-ttu-id="c3e25-117">指定要移除的 IP 組名。</span><span class="sxs-lookup"><span data-stu-id="c3e25-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="c3e25-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e25-118">CommonParameters</span></span>
<span data-ttu-id="c3e25-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c3e25-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e25-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c3e25-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e25-121">輸入</span><span class="sxs-lookup"><span data-stu-id="c3e25-121">INPUTS</span></span>

### <span data-ttu-id="c3e25-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3e25-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3e25-123">輸出</span><span class="sxs-lookup"><span data-stu-id="c3e25-123">OUTPUTS</span></span>

### <span data-ttu-id="c3e25-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3e25-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3e25-125">筆記</span><span class="sxs-lookup"><span data-stu-id="c3e25-125">NOTES</span></span>

## <span data-ttu-id="c3e25-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3e25-126">RELATED LINKS</span></span>

[<span data-ttu-id="c3e25-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3e25-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c3e25-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3e25-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c3e25-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3e25-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c3e25-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3e25-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


