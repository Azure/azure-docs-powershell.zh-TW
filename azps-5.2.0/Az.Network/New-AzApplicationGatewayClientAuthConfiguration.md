---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 6e8c3cdbfa1242cba19d3aa3250c4bf4e381ae92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279767"
---
# <span data-ttu-id="f5077-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5077-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="f5077-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5077-102">SYNOPSIS</span></span>
<span data-ttu-id="f5077-103">為 SSL 設定檔建立新的用戶端驗證設定。</span><span class="sxs-lookup"><span data-stu-id="f5077-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="f5077-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5077-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5077-105">說明</span><span class="sxs-lookup"><span data-stu-id="f5077-105">DESCRIPTION</span></span>
<span data-ttu-id="f5077-106">**新的-AzApplicationGatewayClientAuthConfiguration** Cmdlet 會為 SSL 設定檔建立新的用戶端驗證設定。</span><span class="sxs-lookup"><span data-stu-id="f5077-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="f5077-107">示例</span><span class="sxs-lookup"><span data-stu-id="f5077-107">EXAMPLES</span></span>

### <span data-ttu-id="f5077-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f5077-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="f5077-109">此命令會建立新的用戶端驗證設定，並將其儲存在 SSL 設定檔中要使用 $clientAuthConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="f5077-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="f5077-110">參數</span><span class="sxs-lookup"><span data-stu-id="f5077-110">PARAMETERS</span></span>

### <span data-ttu-id="f5077-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5077-111">-DefaultProfile</span></span>
<span data-ttu-id="f5077-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5077-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5077-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="f5077-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="f5077-114">驗證用戶端憑證頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="f5077-114">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="f5077-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5077-115">CommonParameters</span></span>
<span data-ttu-id="f5077-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5077-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5077-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f5077-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5077-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f5077-118">INPUTS</span></span>

### <span data-ttu-id="f5077-119">所有</span><span class="sxs-lookup"><span data-stu-id="f5077-119">None</span></span>

## <span data-ttu-id="f5077-120">輸出</span><span class="sxs-lookup"><span data-stu-id="f5077-120">OUTPUTS</span></span>

### <span data-ttu-id="f5077-121">PSApplicationGatewayClientAuthConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f5077-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="f5077-122">筆記</span><span class="sxs-lookup"><span data-stu-id="f5077-122">NOTES</span></span>

## <span data-ttu-id="f5077-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5077-123">RELATED LINKS</span></span>

[<span data-ttu-id="f5077-124">附加 AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5077-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="f5077-125">AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5077-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="f5077-126">移除-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5077-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="f5077-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5077-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)