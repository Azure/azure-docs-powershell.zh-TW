---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 92d3945e92dc4996fbbe3fc0abbcc296ab141621
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286816"
---
# <span data-ttu-id="46ba4-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46ba4-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="46ba4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="46ba4-103">移除 SSL 設定檔物件的用戶端驗證設定。</span><span class="sxs-lookup"><span data-stu-id="46ba4-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="46ba4-104">句法</span><span class="sxs-lookup"><span data-stu-id="46ba4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46ba4-105">說明</span><span class="sxs-lookup"><span data-stu-id="46ba4-105">DESCRIPTION</span></span>
<span data-ttu-id="46ba4-106">**AzApplicationGatewayClientAuthConfiguration** Cmdlet 會移除 SSL 設定檔物件的用戶端驗證設定。</span><span class="sxs-lookup"><span data-stu-id="46ba4-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="46ba4-107">示例</span><span class="sxs-lookup"><span data-stu-id="46ba4-107">EXAMPLES</span></span>

### <span data-ttu-id="46ba4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="46ba4-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="46ba4-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="46ba4-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="46ba4-110">第二個命令會針對 $AppGw 取得名為 Profile01 的 SSL 設定檔，並將它儲存在 $profile 變數中。</span><span class="sxs-lookup"><span data-stu-id="46ba4-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="46ba4-111">最後一個命令會移除儲存在 $profile 中之 ssl 設定檔的用戶端驗證設定。</span><span class="sxs-lookup"><span data-stu-id="46ba4-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="46ba4-112">參數</span><span class="sxs-lookup"><span data-stu-id="46ba4-112">PARAMETERS</span></span>

### <span data-ttu-id="46ba4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ba4-113">-DefaultProfile</span></span>
<span data-ttu-id="46ba4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46ba4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46ba4-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="46ba4-115">-SslProfile</span></span>
<span data-ttu-id="46ba4-116">Ssl 設定檔</span><span class="sxs-lookup"><span data-stu-id="46ba4-116">The ssl profile</span></span>

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

### <span data-ttu-id="46ba4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ba4-117">CommonParameters</span></span>
<span data-ttu-id="46ba4-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46ba4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ba4-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="46ba4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ba4-120">輸入</span><span class="sxs-lookup"><span data-stu-id="46ba4-120">INPUTS</span></span>

### <span data-ttu-id="46ba4-121">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="46ba4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="46ba4-122">輸出</span><span class="sxs-lookup"><span data-stu-id="46ba4-122">OUTPUTS</span></span>

### <span data-ttu-id="46ba4-123">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="46ba4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="46ba4-124">筆記</span><span class="sxs-lookup"><span data-stu-id="46ba4-124">NOTES</span></span>

## <span data-ttu-id="46ba4-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="46ba4-125">RELATED LINKS</span></span>

[<span data-ttu-id="46ba4-126">新-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46ba4-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="46ba4-127">附加 AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46ba4-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="46ba4-128">AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46ba4-128">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="46ba4-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46ba4-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)