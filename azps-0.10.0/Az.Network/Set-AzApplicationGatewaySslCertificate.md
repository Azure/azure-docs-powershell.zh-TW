---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b68f0bf3b0112587256fddc3dbb6c31605f811b7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795435"
---
# <span data-ttu-id="b9dfa-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dfa-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b9dfa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="b9dfa-103">設定 SSL 憑證的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="b9dfa-103">Sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="b9dfa-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9dfa-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9dfa-105">說明</span><span class="sxs-lookup"><span data-stu-id="b9dfa-105">DESCRIPTION</span></span>
<span data-ttu-id="b9dfa-106">**AzApplicationGatewaySslCertificate** Cmdlet 會設定 SSL 憑證的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="b9dfa-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="b9dfa-107">示例</span><span class="sxs-lookup"><span data-stu-id="b9dfa-107">EXAMPLES</span></span>

### <span data-ttu-id="b9dfa-108">範例1：設定 SSL 憑證的目標狀態</span><span class="sxs-lookup"><span data-stu-id="b9dfa-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="b9dfa-109">這個命令會從名為 ApplicationGateway01 的應用程式閘道設定 SSL 憑證的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="b9dfa-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="b9dfa-110">參數</span><span class="sxs-lookup"><span data-stu-id="b9dfa-110">PARAMETERS</span></span>

### <span data-ttu-id="b9dfa-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9dfa-111">-ApplicationGateway</span></span>
<span data-ttu-id="b9dfa-112">指定與安全通訊端層 (SSL) 憑證相關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b9dfa-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="b9dfa-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b9dfa-113">-CertificateFile</span></span>
<span data-ttu-id="b9dfa-114">指定 SSL 憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="b9dfa-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="b9dfa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9dfa-115">-DefaultProfile</span></span>
<span data-ttu-id="b9dfa-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9dfa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9dfa-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9dfa-117">-Name</span></span>
<span data-ttu-id="b9dfa-118">指定 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9dfa-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="b9dfa-119">-Password</span><span class="sxs-lookup"><span data-stu-id="b9dfa-119">-Password</span></span>
<span data-ttu-id="b9dfa-120">指定 SSL 憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="b9dfa-120">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9dfa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9dfa-121">CommonParameters</span></span>
<span data-ttu-id="b9dfa-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9dfa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9dfa-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b9dfa-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9dfa-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b9dfa-124">INPUTS</span></span>

### <span data-ttu-id="b9dfa-125">System.object</span><span class="sxs-lookup"><span data-stu-id="b9dfa-125">System.String</span></span>

## <span data-ttu-id="b9dfa-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b9dfa-126">OUTPUTS</span></span>

### <span data-ttu-id="b9dfa-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b9dfa-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9dfa-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b9dfa-128">NOTES</span></span>

## <span data-ttu-id="b9dfa-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9dfa-129">RELATED LINKS</span></span>

[<span data-ttu-id="b9dfa-130">附加 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dfa-130">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b9dfa-131">AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dfa-131">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b9dfa-132">新-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dfa-132">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b9dfa-133">移除-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9dfa-133">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


