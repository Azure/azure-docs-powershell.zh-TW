---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: cec5a6aa0b61889e7923ebce67d1247f99d215e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625712"
---
# <span data-ttu-id="60e0c-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="60e0c-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="60e0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="60e0c-103">設定 SSL 憑證的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="60e0c-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60e0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="60e0c-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60e0c-105">說明</span><span class="sxs-lookup"><span data-stu-id="60e0c-105">DESCRIPTION</span></span>
<span data-ttu-id="60e0c-106">**AzureRmApplicationGatewaySslCertificate** Cmdlet 會設定 SSL 憑證的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="60e0c-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="60e0c-107">示例</span><span class="sxs-lookup"><span data-stu-id="60e0c-107">EXAMPLES</span></span>

### <span data-ttu-id="60e0c-108">範例1：設定 SSL 憑證的目標狀態</span><span class="sxs-lookup"><span data-stu-id="60e0c-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="60e0c-109">這個命令會從名為 ApplicationGateway01 的應用程式閘道設定 SSL 憑證的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="60e0c-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="60e0c-110">參數</span><span class="sxs-lookup"><span data-stu-id="60e0c-110">PARAMETERS</span></span>

### <span data-ttu-id="60e0c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60e0c-111">-ApplicationGateway</span></span>
<span data-ttu-id="60e0c-112">指定與安全通訊端層 (SSL) 憑證相關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="60e0c-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="60e0c-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="60e0c-113">-CertificateFile</span></span>
<span data-ttu-id="60e0c-114">指定 SSL 憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="60e0c-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="60e0c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="60e0c-115">-Name</span></span>
<span data-ttu-id="60e0c-116">指定 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="60e0c-116">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="60e0c-117">-Password</span><span class="sxs-lookup"><span data-stu-id="60e0c-117">-Password</span></span>
<span data-ttu-id="60e0c-118">指定 SSL 憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="60e0c-118">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="60e0c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e0c-119">-DefaultProfile</span></span>
<span data-ttu-id="60e0c-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60e0c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60e0c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e0c-121">CommonParameters</span></span>
<span data-ttu-id="60e0c-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60e0c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e0c-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60e0c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e0c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="60e0c-124">INPUTS</span></span>

### <span data-ttu-id="60e0c-125">System.object</span><span class="sxs-lookup"><span data-stu-id="60e0c-125">System.String</span></span>

## <span data-ttu-id="60e0c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="60e0c-126">OUTPUTS</span></span>

### <span data-ttu-id="60e0c-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="60e0c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="60e0c-128">筆記</span><span class="sxs-lookup"><span data-stu-id="60e0c-128">NOTES</span></span>

## <span data-ttu-id="60e0c-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="60e0c-129">RELATED LINKS</span></span>

[<span data-ttu-id="60e0c-130">附加 AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="60e0c-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="60e0c-131">AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="60e0c-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="60e0c-132">新-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="60e0c-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="60e0c-133">移除-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="60e0c-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


