---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7b5f37cb42d128cbf44294520419c8f4d09124fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621643"
---
# <span data-ttu-id="55989-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="55989-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="55989-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55989-102">SYNOPSIS</span></span>
<span data-ttu-id="55989-103">從 Azure 應用程式閘道移除 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="55989-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="55989-104">句法</span><span class="sxs-lookup"><span data-stu-id="55989-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55989-105">說明</span><span class="sxs-lookup"><span data-stu-id="55989-105">DESCRIPTION</span></span>
<span data-ttu-id="55989-106">**AzApplicationGatewaySslCertificate** Cmdlet 會從 Azure 應用程式閘道 (SSL) 憑證中移除安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="55989-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="55989-107">示例</span><span class="sxs-lookup"><span data-stu-id="55989-107">EXAMPLES</span></span>

### <span data-ttu-id="55989-108">範例1：從應用程式閘道移除 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="55989-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="55989-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="55989-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="55989-110">第二個命令會從 $AppGW 變數中儲存的應用程式閘道，移除名為 Cert02 的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="55989-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="55989-111">參數</span><span class="sxs-lookup"><span data-stu-id="55989-111">PARAMETERS</span></span>

### <span data-ttu-id="55989-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="55989-112">-ApplicationGateway</span></span>
<span data-ttu-id="55989-113">指定此 Cmdlet 移除 SSL 憑證的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="55989-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="55989-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55989-114">-DefaultProfile</span></span>
<span data-ttu-id="55989-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55989-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55989-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="55989-116">-Name</span></span>
<span data-ttu-id="55989-117">指定此 Cmdlet 移除之 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="55989-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="55989-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55989-118">CommonParameters</span></span>
<span data-ttu-id="55989-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55989-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55989-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55989-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55989-121">輸入</span><span class="sxs-lookup"><span data-stu-id="55989-121">INPUTS</span></span>

### <span data-ttu-id="55989-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55989-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="55989-123">輸出</span><span class="sxs-lookup"><span data-stu-id="55989-123">OUTPUTS</span></span>

### <span data-ttu-id="55989-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55989-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="55989-125">筆記</span><span class="sxs-lookup"><span data-stu-id="55989-125">NOTES</span></span>

## <span data-ttu-id="55989-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="55989-126">RELATED LINKS</span></span>

[<span data-ttu-id="55989-127">附加 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="55989-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="55989-128">AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="55989-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="55989-129">新-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="55989-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="55989-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="55989-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


