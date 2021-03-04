---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 79a602047327ef7723da360f0b89743a316d2ec3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904937"
---
# <span data-ttu-id="52ffe-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="52ffe-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="52ffe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="52ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="52ffe-103">修改 Ssl 設定檔物件的用戶端驗證組式。</span><span class="sxs-lookup"><span data-stu-id="52ffe-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="52ffe-104">語法</span><span class="sxs-lookup"><span data-stu-id="52ffe-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52ffe-105">描述</span><span class="sxs-lookup"><span data-stu-id="52ffe-105">DESCRIPTION</span></span>
<span data-ttu-id="52ffe-106">**Set-AzApplicationGatewayClientAuthConfiguration** Cmdlet 會修改 ssl 設定檔物件的用戶端驗證設定。</span><span class="sxs-lookup"><span data-stu-id="52ffe-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="52ffe-107">例子</span><span class="sxs-lookup"><span data-stu-id="52ffe-107">EXAMPLES</span></span>

### <span data-ttu-id="52ffe-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="52ffe-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="52ffe-109">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="52ffe-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="52ffe-110">第二個命令會獲得名稱為 SslProfile01 的 ssl 設定檔$AppGw將設定儲存在$profile變數中。</span><span class="sxs-lookup"><span data-stu-id="52ffe-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="52ffe-111">最後一個命令會修改儲存在 $profile 中的 ssl 設定檔物件的用戶端驗證$profile。</span><span class="sxs-lookup"><span data-stu-id="52ffe-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="52ffe-112">參數</span><span class="sxs-lookup"><span data-stu-id="52ffe-112">PARAMETERS</span></span>

### <span data-ttu-id="52ffe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ffe-113">-DefaultProfile</span></span>
<span data-ttu-id="52ffe-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="52ffe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52ffe-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="52ffe-115">-SslProfile</span></span>
<span data-ttu-id="52ffe-116">ssl 設定檔</span><span class="sxs-lookup"><span data-stu-id="52ffe-116">The ssl profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52ffe-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="52ffe-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="52ffe-118">驗證用戶端憑證發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="52ffe-118">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ffe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ffe-119">CommonParameters</span></span>
<span data-ttu-id="52ffe-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="52ffe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ffe-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52ffe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ffe-122">輸入</span><span class="sxs-lookup"><span data-stu-id="52ffe-122">INPUTS</span></span>

### <span data-ttu-id="52ffe-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="52ffe-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="52ffe-124">輸出</span><span class="sxs-lookup"><span data-stu-id="52ffe-124">OUTPUTS</span></span>

### <span data-ttu-id="52ffe-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="52ffe-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="52ffe-126">筆記</span><span class="sxs-lookup"><span data-stu-id="52ffe-126">NOTES</span></span>

## <span data-ttu-id="52ffe-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="52ffe-127">RELATED LINKS</span></span>

[<span data-ttu-id="52ffe-128">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="52ffe-128">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="52ffe-129">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="52ffe-129">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="52ffe-130">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="52ffe-130">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="52ffe-131">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="52ffe-131">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)