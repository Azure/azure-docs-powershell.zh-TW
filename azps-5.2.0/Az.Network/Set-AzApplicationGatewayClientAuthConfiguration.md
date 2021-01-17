---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 9512d2d2a51e70b2a0b5e7aa2e8240a8aeb1be1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275311"
---
# <span data-ttu-id="1c496-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c496-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="1c496-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c496-102">SYNOPSIS</span></span>
<span data-ttu-id="1c496-103">修改 ssl 設定檔物件的用戶端授權設定。</span><span class="sxs-lookup"><span data-stu-id="1c496-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="1c496-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c496-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c496-105">說明</span><span class="sxs-lookup"><span data-stu-id="1c496-105">DESCRIPTION</span></span>
<span data-ttu-id="1c496-106">**AzApplicationGatewayClientAuthConfiguration** Cmdlet 會修改 ssl 設定檔物件的用戶端授權設定。</span><span class="sxs-lookup"><span data-stu-id="1c496-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="1c496-107">示例</span><span class="sxs-lookup"><span data-stu-id="1c496-107">EXAMPLES</span></span>

### <span data-ttu-id="1c496-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1c496-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="1c496-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="1c496-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="1c496-110">第二個命令會針對 $AppGw 取得名為 SslProfile01 的 ssl 設定檔，並將設定儲存在 $profile 變數中。</span><span class="sxs-lookup"><span data-stu-id="1c496-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="1c496-111">最後一個命令會修改儲存在 $profile 之 ssl 設定檔物件的用戶端授權設定。</span><span class="sxs-lookup"><span data-stu-id="1c496-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="1c496-112">參數</span><span class="sxs-lookup"><span data-stu-id="1c496-112">PARAMETERS</span></span>

### <span data-ttu-id="1c496-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c496-113">-DefaultProfile</span></span>
<span data-ttu-id="1c496-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c496-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c496-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="1c496-115">-SslProfile</span></span>
<span data-ttu-id="1c496-116">Ssl 設定檔</span><span class="sxs-lookup"><span data-stu-id="1c496-116">The ssl profile</span></span>

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

### <span data-ttu-id="1c496-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="1c496-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="1c496-118">驗證用戶端憑證頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="1c496-118">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="1c496-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c496-119">CommonParameters</span></span>
<span data-ttu-id="1c496-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c496-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c496-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1c496-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c496-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1c496-122">INPUTS</span></span>

### <span data-ttu-id="1c496-123">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1c496-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1c496-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1c496-124">OUTPUTS</span></span>

### <span data-ttu-id="1c496-125">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1c496-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1c496-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1c496-126">NOTES</span></span>

## <span data-ttu-id="1c496-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c496-127">RELATED LINKS</span></span>

[<span data-ttu-id="1c496-128">附加 AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c496-128">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1c496-129">新-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c496-129">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1c496-130">AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c496-130">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1c496-131">移除-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c496-131">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)