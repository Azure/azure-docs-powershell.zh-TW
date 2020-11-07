---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: eeab1f5699af5de737bc1e0390c35d387acfdd98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800393"
---
# <span data-ttu-id="e3ceb-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3ceb-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e3ceb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ceb-103">從 Azure 應用程式閘道移除 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="e3ceb-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3ceb-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3ceb-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3ceb-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3ceb-105">DESCRIPTION</span></span>
<span data-ttu-id="e3ceb-106">**AzureRmApplicationGatewaySslCertificate** Cmdlet 會從 Azure 應用程式閘道 (SSL) 憑證中移除安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="e3ceb-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="e3ceb-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3ceb-107">EXAMPLES</span></span>

### <span data-ttu-id="e3ceb-108">範例1：從應用程式閘道移除 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="e3ceb-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="e3ceb-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e3ceb-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="e3ceb-110">第二個命令會從 $AppGW 變數中儲存的應用程式閘道，移除名為 Cert02 的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="e3ceb-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="e3ceb-111">參數</span><span class="sxs-lookup"><span data-stu-id="e3ceb-111">PARAMETERS</span></span>

### <span data-ttu-id="e3ceb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3ceb-112">-ApplicationGateway</span></span>
<span data-ttu-id="e3ceb-113">指定此 Cmdlet 移除 SSL 憑證的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e3ceb-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="e3ceb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ceb-114">-DefaultProfile</span></span>
<span data-ttu-id="e3ceb-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3ceb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ceb-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3ceb-116">-Name</span></span>
<span data-ttu-id="e3ceb-117">指定此 Cmdlet 移除之 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3ceb-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e3ceb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ceb-118">CommonParameters</span></span>
<span data-ttu-id="e3ceb-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3ceb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ceb-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3ceb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ceb-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e3ceb-121">INPUTS</span></span>

### <span data-ttu-id="e3ceb-122">System.object</span><span class="sxs-lookup"><span data-stu-id="e3ceb-122">System.String</span></span>

## <span data-ttu-id="e3ceb-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e3ceb-123">OUTPUTS</span></span>

### <span data-ttu-id="e3ceb-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3ceb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3ceb-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e3ceb-125">NOTES</span></span>

## <span data-ttu-id="e3ceb-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3ceb-126">RELATED LINKS</span></span>

[<span data-ttu-id="e3ceb-127">附加 AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3ceb-127">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e3ceb-128">AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3ceb-128">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e3ceb-129">新-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3ceb-129">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e3ceb-130">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3ceb-130">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


