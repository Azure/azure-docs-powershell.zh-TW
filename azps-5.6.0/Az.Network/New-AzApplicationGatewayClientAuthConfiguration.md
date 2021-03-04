---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 002fdabfb01a0b12d36c69b0a8a75ddf91880012
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905337"
---
# <span data-ttu-id="83d35-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="83d35-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="83d35-102">簡介</span><span class="sxs-lookup"><span data-stu-id="83d35-102">SYNOPSIS</span></span>
<span data-ttu-id="83d35-103">為 SSL 設定檔建立新的用戶端驗證組。</span><span class="sxs-lookup"><span data-stu-id="83d35-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="83d35-104">語法</span><span class="sxs-lookup"><span data-stu-id="83d35-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83d35-105">描述</span><span class="sxs-lookup"><span data-stu-id="83d35-105">DESCRIPTION</span></span>
<span data-ttu-id="83d35-106">**New-AzApplicationGatewayClientAuthConfiguration** Cmdlet 會為 SSL 設定檔建立新的用戶端驗證組。</span><span class="sxs-lookup"><span data-stu-id="83d35-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="83d35-107">例子</span><span class="sxs-lookup"><span data-stu-id="83d35-107">EXAMPLES</span></span>

### <span data-ttu-id="83d35-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="83d35-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="83d35-109">命令會建立新的用戶端驗證組$clientAuthConfig儲存在 SSL 設定檔中使用的變數。</span><span class="sxs-lookup"><span data-stu-id="83d35-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="83d35-110">參數</span><span class="sxs-lookup"><span data-stu-id="83d35-110">PARAMETERS</span></span>

### <span data-ttu-id="83d35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d35-111">-DefaultProfile</span></span>
<span data-ttu-id="83d35-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="83d35-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83d35-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="83d35-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="83d35-114">驗證用戶端憑證發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="83d35-114">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="83d35-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d35-115">CommonParameters</span></span>
<span data-ttu-id="83d35-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="83d35-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d35-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83d35-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d35-118">輸入</span><span class="sxs-lookup"><span data-stu-id="83d35-118">INPUTS</span></span>

### <span data-ttu-id="83d35-119">沒有</span><span class="sxs-lookup"><span data-stu-id="83d35-119">None</span></span>

## <span data-ttu-id="83d35-120">輸出</span><span class="sxs-lookup"><span data-stu-id="83d35-120">OUTPUTS</span></span>

### <span data-ttu-id="83d35-121">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="83d35-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="83d35-122">筆記</span><span class="sxs-lookup"><span data-stu-id="83d35-122">NOTES</span></span>

## <span data-ttu-id="83d35-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="83d35-123">RELATED LINKS</span></span>

[<span data-ttu-id="83d35-124">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="83d35-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="83d35-125">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="83d35-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="83d35-126">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="83d35-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="83d35-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="83d35-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)