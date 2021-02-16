---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 074ad4103128b9fd3943ebe4f450a04b74c28a75
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403556"
---
# <span data-ttu-id="35cbe-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="35cbe-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="35cbe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="35cbe-102">SYNOPSIS</span></span>
<span data-ttu-id="35cbe-103">獲得 SSL 設定檔物件的用戶端驗證組式。</span><span class="sxs-lookup"><span data-stu-id="35cbe-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="35cbe-104">語法</span><span class="sxs-lookup"><span data-stu-id="35cbe-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35cbe-105">描述</span><span class="sxs-lookup"><span data-stu-id="35cbe-105">DESCRIPTION</span></span>
<span data-ttu-id="35cbe-106">**Get-AzApplicationGatewayClientAuthConfiguration** Cmdlet 會取得 SSL 設定檔物件的用戶端驗證組式。</span><span class="sxs-lookup"><span data-stu-id="35cbe-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="35cbe-107">例子</span><span class="sxs-lookup"><span data-stu-id="35cbe-107">EXAMPLES</span></span>

### <span data-ttu-id="35cbe-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="35cbe-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="35cbe-109">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="35cbe-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="35cbe-110">第二個命令會獲得名稱為 SslProfile01 的 SSL 設定檔，$AppGw儲存為$SslProfile變數。</span><span class="sxs-lookup"><span data-stu-id="35cbe-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="35cbe-111">最後一個命令會從 SSL 設定檔$SslProfile用戶端驗證組$ClientAuthConfig變數。</span><span class="sxs-lookup"><span data-stu-id="35cbe-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="35cbe-112">參數</span><span class="sxs-lookup"><span data-stu-id="35cbe-112">PARAMETERS</span></span>

### <span data-ttu-id="35cbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35cbe-113">-DefaultProfile</span></span>
<span data-ttu-id="35cbe-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="35cbe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35cbe-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="35cbe-115">-SslProfile</span></span>
<span data-ttu-id="35cbe-116">ssl 設定檔</span><span class="sxs-lookup"><span data-stu-id="35cbe-116">The ssl profile</span></span>

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

### <span data-ttu-id="35cbe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35cbe-117">CommonParameters</span></span>
<span data-ttu-id="35cbe-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="35cbe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35cbe-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35cbe-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35cbe-120">輸入</span><span class="sxs-lookup"><span data-stu-id="35cbe-120">INPUTS</span></span>

### <span data-ttu-id="35cbe-121">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="35cbe-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="35cbe-122">輸出</span><span class="sxs-lookup"><span data-stu-id="35cbe-122">OUTPUTS</span></span>

### <span data-ttu-id="35cbe-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="35cbe-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="35cbe-124">筆記</span><span class="sxs-lookup"><span data-stu-id="35cbe-124">NOTES</span></span>

## <span data-ttu-id="35cbe-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="35cbe-125">RELATED LINKS</span></span>

[<span data-ttu-id="35cbe-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="35cbe-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)


[<span data-ttu-id="35cbe-127">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="35cbe-127">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="35cbe-128">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="35cbe-128">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
