---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 140bfd84d2758badc45a902e4ed14e027c5bca3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457004"
---
# <span data-ttu-id="0aca3-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0aca3-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="0aca3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0aca3-102">SYNOPSIS</span></span>
<span data-ttu-id="0aca3-103">建立應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="0aca3-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aca3-104">句法</span><span class="sxs-lookup"><span data-stu-id="0aca3-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0aca3-105">說明</span><span class="sxs-lookup"><span data-stu-id="0aca3-105">DESCRIPTION</span></span>
<span data-ttu-id="0aca3-106">**新的-AzureRmApplicationGatewaySslPolicy** Cmdlet 會為應用程式閘道建立 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="0aca3-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="0aca3-107">示例</span><span class="sxs-lookup"><span data-stu-id="0aca3-107">EXAMPLES</span></span>

### <span data-ttu-id="0aca3-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="0aca3-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="0aca3-109">這個命令會建立自訂原則。</span><span class="sxs-lookup"><span data-stu-id="0aca3-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="0aca3-110">參數</span><span class="sxs-lookup"><span data-stu-id="0aca3-110">PARAMETERS</span></span>

### <span data-ttu-id="0aca3-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="0aca3-111">-CipherSuite</span></span>
<span data-ttu-id="0aca3-112">要在應用程式閘道的指定順序啟用 Ssl 密碼套件</span><span class="sxs-lookup"><span data-stu-id="0aca3-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aca3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aca3-113">-DefaultProfile</span></span>
<span data-ttu-id="0aca3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0aca3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aca3-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="0aca3-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="0aca3-116">指定停用哪些通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0aca3-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="0aca3-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0aca3-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0aca3-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="0aca3-118">TLSv1_0</span></span> 
- <span data-ttu-id="0aca3-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="0aca3-119">TLSv1_1</span></span> 
- <span data-ttu-id="0aca3-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="0aca3-120">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aca3-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="0aca3-121">-MinProtocolVersion</span></span>
<span data-ttu-id="0aca3-122">應用程式閘道支援的最小 Ssl 通訊協定版本</span><span class="sxs-lookup"><span data-stu-id="0aca3-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aca3-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="0aca3-123">-PolicyName</span></span>
<span data-ttu-id="0aca3-124">Ssl 預先定義原則的名稱</span><span class="sxs-lookup"><span data-stu-id="0aca3-124">Name of Ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aca3-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="0aca3-125">-PolicyType</span></span>
<span data-ttu-id="0aca3-126">Ssl 原則類型</span><span class="sxs-lookup"><span data-stu-id="0aca3-126">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aca3-127">-確認</span><span class="sxs-lookup"><span data-stu-id="0aca3-127">-Confirm</span></span>
<span data-ttu-id="0aca3-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0aca3-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aca3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aca3-129">-WhatIf</span></span>
<span data-ttu-id="0aca3-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0aca3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aca3-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0aca3-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aca3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aca3-132">CommonParameters</span></span>
<span data-ttu-id="0aca3-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0aca3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aca3-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0aca3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aca3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0aca3-135">INPUTS</span></span>

### <span data-ttu-id="0aca3-136">所有</span><span class="sxs-lookup"><span data-stu-id="0aca3-136">None</span></span>

## <span data-ttu-id="0aca3-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0aca3-137">OUTPUTS</span></span>

### <span data-ttu-id="0aca3-138">PSApplicationGatewaySslPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0aca3-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="0aca3-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0aca3-139">NOTES</span></span>
* <span data-ttu-id="0aca3-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="0aca3-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0aca3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="0aca3-141">RELATED LINKS</span></span>

[<span data-ttu-id="0aca3-142">AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0aca3-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="0aca3-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0aca3-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


