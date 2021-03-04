---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 367e54036d7665cf59ebcc6f1a10b3060b97580d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911914"
---
# <span data-ttu-id="ae0e8-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae0e8-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="ae0e8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ae0e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ae0e8-103">從應用程式閘道移除 privateLink 組配置。</span><span class="sxs-lookup"><span data-stu-id="ae0e8-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="ae0e8-104">語法</span><span class="sxs-lookup"><span data-stu-id="ae0e8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae0e8-105">描述</span><span class="sxs-lookup"><span data-stu-id="ae0e8-105">DESCRIPTION</span></span>
<span data-ttu-id="ae0e8-106">**Remove-AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會從 Azure 應用程式閘道移除 privateLink 組式。</span><span class="sxs-lookup"><span data-stu-id="ae0e8-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="ae0e8-107">例子</span><span class="sxs-lookup"><span data-stu-id="ae0e8-107">EXAMPLES</span></span>

### <span data-ttu-id="ae0e8-108">範例 1：移除應用程式閘道 PrivateLink Configuration</span><span class="sxs-lookup"><span data-stu-id="ae0e8-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="ae0e8-109">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="ae0e8-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ae0e8-110">第二個命令會從儲存在 $AppGw 的應用程式閘道移除名為 privateLinkConfig01 的 privateLink $AppGw。</span><span class="sxs-lookup"><span data-stu-id="ae0e8-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ae0e8-111">參數</span><span class="sxs-lookup"><span data-stu-id="ae0e8-111">PARAMETERS</span></span>

### <span data-ttu-id="ae0e8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae0e8-112">-ApplicationGateway</span></span>
<span data-ttu-id="ae0e8-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="ae0e8-113">The applicationGateway</span></span>

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

### <span data-ttu-id="ae0e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae0e8-114">-DefaultProfile</span></span>
<span data-ttu-id="ae0e8-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae0e8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae0e8-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae0e8-116">-Name</span></span>
<span data-ttu-id="ae0e8-117">應用程式閘道 privateLink 組組的名稱</span><span class="sxs-lookup"><span data-stu-id="ae0e8-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="ae0e8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae0e8-118">CommonParameters</span></span>
<span data-ttu-id="ae0e8-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ae0e8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae0e8-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae0e8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae0e8-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ae0e8-121">INPUTS</span></span>

### <span data-ttu-id="ae0e8-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae0e8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae0e8-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ae0e8-123">OUTPUTS</span></span>

### <span data-ttu-id="ae0e8-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae0e8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae0e8-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ae0e8-125">NOTES</span></span>

## <span data-ttu-id="ae0e8-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae0e8-126">RELATED LINKS</span></span>

[<span data-ttu-id="ae0e8-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae0e8-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ae0e8-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae0e8-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ae0e8-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae0e8-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ae0e8-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae0e8-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)