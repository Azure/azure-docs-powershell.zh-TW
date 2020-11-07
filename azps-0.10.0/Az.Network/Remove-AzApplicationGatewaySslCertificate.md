---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 9b90dc354a62c6f6d69e1e6dbd8bf18ecc0fa4f7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794198"
---
# <span data-ttu-id="d7860-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d7860-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="d7860-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d7860-102">SYNOPSIS</span></span>
<span data-ttu-id="d7860-103">從 Azure 應用程式閘道移除 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="d7860-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="d7860-104">句法</span><span class="sxs-lookup"><span data-stu-id="d7860-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7860-105">說明</span><span class="sxs-lookup"><span data-stu-id="d7860-105">DESCRIPTION</span></span>
<span data-ttu-id="d7860-106">**AzApplicationGatewaySslCertificate** Cmdlet 會從 Azure 應用程式閘道 (SSL) 憑證中移除安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="d7860-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="d7860-107">示例</span><span class="sxs-lookup"><span data-stu-id="d7860-107">EXAMPLES</span></span>

### <span data-ttu-id="d7860-108">範例1：從應用程式閘道移除 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="d7860-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="d7860-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="d7860-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="d7860-110">第二個命令會從 $AppGW 變數中儲存的應用程式閘道，移除名為 Cert02 的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="d7860-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="d7860-111">參數</span><span class="sxs-lookup"><span data-stu-id="d7860-111">PARAMETERS</span></span>

### <span data-ttu-id="d7860-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7860-112">-ApplicationGateway</span></span>
<span data-ttu-id="d7860-113">指定此 Cmdlet 移除 SSL 憑證的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d7860-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="d7860-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7860-114">-DefaultProfile</span></span>
<span data-ttu-id="d7860-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7860-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7860-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7860-116">-Name</span></span>
<span data-ttu-id="d7860-117">指定此 Cmdlet 移除之 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7860-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d7860-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7860-118">CommonParameters</span></span>
<span data-ttu-id="d7860-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d7860-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7860-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d7860-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7860-121">輸入</span><span class="sxs-lookup"><span data-stu-id="d7860-121">INPUTS</span></span>

### <span data-ttu-id="d7860-122">System.object</span><span class="sxs-lookup"><span data-stu-id="d7860-122">System.String</span></span>

## <span data-ttu-id="d7860-123">輸出</span><span class="sxs-lookup"><span data-stu-id="d7860-123">OUTPUTS</span></span>

### <span data-ttu-id="d7860-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d7860-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d7860-125">筆記</span><span class="sxs-lookup"><span data-stu-id="d7860-125">NOTES</span></span>

## <span data-ttu-id="d7860-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7860-126">RELATED LINKS</span></span>

[<span data-ttu-id="d7860-127">附加 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d7860-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="d7860-128">AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d7860-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="d7860-129">新-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d7860-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="d7860-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d7860-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


