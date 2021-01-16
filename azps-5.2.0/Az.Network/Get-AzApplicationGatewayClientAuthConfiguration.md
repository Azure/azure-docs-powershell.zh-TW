---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: eee7040dab93a4f73bacdf440c6450a525fab9a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274168"
---
# <span data-ttu-id="4e7a4-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e7a4-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="4e7a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="4e7a4-103">取得 SSL 設定檔物件的用戶端驗證設定。</span><span class="sxs-lookup"><span data-stu-id="4e7a4-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="4e7a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e7a4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e7a4-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e7a4-105">DESCRIPTION</span></span>
<span data-ttu-id="4e7a4-106">**AzApplicationGatewayClientAuthConfiguration** Cmdlet 會取得 SSL 設定檔物件的用戶端驗證設定。</span><span class="sxs-lookup"><span data-stu-id="4e7a4-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="4e7a4-107">示例</span><span class="sxs-lookup"><span data-stu-id="4e7a4-107">EXAMPLES</span></span>

### <span data-ttu-id="4e7a4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4e7a4-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="4e7a4-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4e7a4-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="4e7a4-110">第二個命令會針對 $AppGw 取得名為 SslProfile01 的 SSL 設定檔，並將它儲存 $SslProfile 變數。</span><span class="sxs-lookup"><span data-stu-id="4e7a4-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="4e7a4-111">最後一個命令會從 SSL 設定檔中取得用戶端驗證設定，$SslProfile 並將它儲存在 $ClientAuthConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="4e7a4-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="4e7a4-112">參數</span><span class="sxs-lookup"><span data-stu-id="4e7a4-112">PARAMETERS</span></span>

### <span data-ttu-id="4e7a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e7a4-113">-DefaultProfile</span></span>
<span data-ttu-id="4e7a4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e7a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e7a4-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="4e7a4-115">-SslProfile</span></span>
<span data-ttu-id="4e7a4-116">Ssl 設定檔</span><span class="sxs-lookup"><span data-stu-id="4e7a4-116">The ssl profile</span></span>

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

### <span data-ttu-id="4e7a4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e7a4-117">CommonParameters</span></span>
<span data-ttu-id="4e7a4-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e7a4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e7a4-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e7a4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e7a4-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4e7a4-120">INPUTS</span></span>

### <span data-ttu-id="4e7a4-121">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e7a4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="4e7a4-122">輸出</span><span class="sxs-lookup"><span data-stu-id="4e7a4-122">OUTPUTS</span></span>

### <span data-ttu-id="4e7a4-123">PSApplicationGatewayClientAuthConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e7a4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="4e7a4-124">筆記</span><span class="sxs-lookup"><span data-stu-id="4e7a4-124">NOTES</span></span>

## <span data-ttu-id="4e7a4-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e7a4-125">RELATED LINKS</span></span>

[<span data-ttu-id="4e7a4-126">新-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e7a4-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="4e7a4-127">附加 AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e7a4-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="4e7a4-128">移除-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e7a4-128">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="4e7a4-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e7a4-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)