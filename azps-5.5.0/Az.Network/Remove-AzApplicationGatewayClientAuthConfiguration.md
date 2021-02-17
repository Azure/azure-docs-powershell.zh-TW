---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 64dc67a59b739ac7cab51c9c4a02fd7a73f8b4cc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407585"
---
# <span data-ttu-id="9316f-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="9316f-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="9316f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9316f-102">SYNOPSIS</span></span>
<span data-ttu-id="9316f-103">移除 SSL 設定檔物件的用戶端驗證組式。</span><span class="sxs-lookup"><span data-stu-id="9316f-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="9316f-104">語法</span><span class="sxs-lookup"><span data-stu-id="9316f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9316f-105">描述</span><span class="sxs-lookup"><span data-stu-id="9316f-105">DESCRIPTION</span></span>
<span data-ttu-id="9316f-106">**Remove-AzApplicationGatewayClientAuthConfiguration** Cmdlet 會移除 SSL 設定檔物件的用戶端驗證組式。</span><span class="sxs-lookup"><span data-stu-id="9316f-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="9316f-107">例子</span><span class="sxs-lookup"><span data-stu-id="9316f-107">EXAMPLES</span></span>

### <span data-ttu-id="9316f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9316f-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="9316f-109">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="9316f-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="9316f-110">第二個命令會獲得名稱為 Profile01 的 SSL 設定檔$AppGw並儲存在$profile變數中。</span><span class="sxs-lookup"><span data-stu-id="9316f-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="9316f-111">最後一個命令會移除儲存在 $profile 中的 ssl 設定檔的用戶端驗證$profile。</span><span class="sxs-lookup"><span data-stu-id="9316f-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="9316f-112">參數</span><span class="sxs-lookup"><span data-stu-id="9316f-112">PARAMETERS</span></span>

### <span data-ttu-id="9316f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9316f-113">-DefaultProfile</span></span>
<span data-ttu-id="9316f-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9316f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9316f-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="9316f-115">-SslProfile</span></span>
<span data-ttu-id="9316f-116">ssl 設定檔</span><span class="sxs-lookup"><span data-stu-id="9316f-116">The ssl profile</span></span>

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

### <span data-ttu-id="9316f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9316f-117">CommonParameters</span></span>
<span data-ttu-id="9316f-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9316f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9316f-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9316f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9316f-120">輸入</span><span class="sxs-lookup"><span data-stu-id="9316f-120">INPUTS</span></span>

### <span data-ttu-id="9316f-121">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="9316f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="9316f-122">輸出</span><span class="sxs-lookup"><span data-stu-id="9316f-122">OUTPUTS</span></span>

### <span data-ttu-id="9316f-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="9316f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="9316f-124">筆記</span><span class="sxs-lookup"><span data-stu-id="9316f-124">NOTES</span></span>

## <span data-ttu-id="9316f-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="9316f-125">RELATED LINKS</span></span>

[<span data-ttu-id="9316f-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="9316f-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)


[<span data-ttu-id="9316f-127">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="9316f-127">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="9316f-128">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="9316f-128">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
