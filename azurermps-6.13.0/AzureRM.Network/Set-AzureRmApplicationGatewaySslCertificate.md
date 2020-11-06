---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: c45a829414fd1009f97c99844705e9affab0ef30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445583"
---
# <span data-ttu-id="5ac38-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ac38-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5ac38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ac38-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac38-103">設定 SSL 憑證的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="5ac38-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ac38-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ac38-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ac38-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ac38-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac38-106">**AzureRmApplicationGatewaySslCertificate** Cmdlet 會設定 SSL 憑證的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="5ac38-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="5ac38-107">示例</span><span class="sxs-lookup"><span data-stu-id="5ac38-107">EXAMPLES</span></span>

### <span data-ttu-id="5ac38-108">範例1：設定 SSL 憑證的目標狀態</span><span class="sxs-lookup"><span data-stu-id="5ac38-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="5ac38-109">這個命令會從名為 ApplicationGateway01 的應用程式閘道設定 SSL 憑證的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="5ac38-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="5ac38-110">參數</span><span class="sxs-lookup"><span data-stu-id="5ac38-110">PARAMETERS</span></span>

### <span data-ttu-id="5ac38-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ac38-111">-ApplicationGateway</span></span>
<span data-ttu-id="5ac38-112">指定與安全通訊端層 (SSL) 憑證相關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5ac38-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="5ac38-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5ac38-113">-CertificateFile</span></span>
<span data-ttu-id="5ac38-114">指定 SSL 憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="5ac38-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="5ac38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac38-115">-DefaultProfile</span></span>
<span data-ttu-id="5ac38-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ac38-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac38-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ac38-117">-Name</span></span>
<span data-ttu-id="5ac38-118">指定 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ac38-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="5ac38-119">-Password</span><span class="sxs-lookup"><span data-stu-id="5ac38-119">-Password</span></span>
<span data-ttu-id="5ac38-120">指定 SSL 憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="5ac38-120">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac38-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac38-121">CommonParameters</span></span>
<span data-ttu-id="5ac38-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ac38-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac38-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ac38-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac38-124">輸入</span><span class="sxs-lookup"><span data-stu-id="5ac38-124">INPUTS</span></span>

### <span data-ttu-id="5ac38-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5ac38-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="5ac38-126">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5ac38-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="5ac38-127">輸出</span><span class="sxs-lookup"><span data-stu-id="5ac38-127">OUTPUTS</span></span>

### <span data-ttu-id="5ac38-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5ac38-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ac38-129">筆記</span><span class="sxs-lookup"><span data-stu-id="5ac38-129">NOTES</span></span>

## <span data-ttu-id="5ac38-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ac38-130">RELATED LINKS</span></span>

[<span data-ttu-id="5ac38-131">附加 AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ac38-131">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5ac38-132">AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ac38-132">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5ac38-133">新-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ac38-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5ac38-134">移除-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ac38-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


