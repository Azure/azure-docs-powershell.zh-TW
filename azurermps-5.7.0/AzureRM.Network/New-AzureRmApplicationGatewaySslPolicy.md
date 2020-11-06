---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3887f8cdbc4256d39e76fc6b86ff9e9113385519
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93457672"
---
# <span data-ttu-id="43b6a-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="43b6a-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="43b6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="43b6a-103">建立應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="43b6a-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43b6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="43b6a-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43b6a-105">說明</span><span class="sxs-lookup"><span data-stu-id="43b6a-105">DESCRIPTION</span></span>
<span data-ttu-id="43b6a-106">**新的-AzureRmApplicationGatewaySslPolicy** Cmdlet 會為應用程式閘道建立 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="43b6a-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="43b6a-107">示例</span><span class="sxs-lookup"><span data-stu-id="43b6a-107">EXAMPLES</span></span>

### <span data-ttu-id="43b6a-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="43b6a-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="43b6a-109">這個命令會建立自訂原則。</span><span class="sxs-lookup"><span data-stu-id="43b6a-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="43b6a-110">參數</span><span class="sxs-lookup"><span data-stu-id="43b6a-110">PARAMETERS</span></span>

### <span data-ttu-id="43b6a-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="43b6a-111">-CipherSuite</span></span>
<span data-ttu-id="43b6a-112">要在應用程式閘道的指定順序啟用 Ssl 密碼套件</span><span class="sxs-lookup"><span data-stu-id="43b6a-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="43b6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b6a-113">-DefaultProfile</span></span>
<span data-ttu-id="43b6a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43b6a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43b6a-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="43b6a-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="43b6a-116">指定停用哪些通訊協定。</span><span class="sxs-lookup"><span data-stu-id="43b6a-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="43b6a-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="43b6a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43b6a-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="43b6a-118">TLSv1_0</span></span> 
- <span data-ttu-id="43b6a-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="43b6a-119">TLSv1_1</span></span> 
- <span data-ttu-id="43b6a-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="43b6a-120">TLSv1_2</span></span>

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

### <span data-ttu-id="43b6a-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="43b6a-121">-MinProtocolVersion</span></span>
<span data-ttu-id="43b6a-122">應用程式閘道支援的最小 Ssl 通訊協定版本</span><span class="sxs-lookup"><span data-stu-id="43b6a-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43b6a-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="43b6a-123">-PolicyName</span></span>
<span data-ttu-id="43b6a-124">Ssl 預先定義原則的名稱</span><span class="sxs-lookup"><span data-stu-id="43b6a-124">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43b6a-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="43b6a-125">-PolicyType</span></span>
<span data-ttu-id="43b6a-126">Ssl 原則類型</span><span class="sxs-lookup"><span data-stu-id="43b6a-126">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43b6a-127">-確認</span><span class="sxs-lookup"><span data-stu-id="43b6a-127">-Confirm</span></span>
<span data-ttu-id="43b6a-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43b6a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43b6a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43b6a-129">-WhatIf</span></span>
<span data-ttu-id="43b6a-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43b6a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43b6a-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43b6a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43b6a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b6a-132">CommonParameters</span></span>
<span data-ttu-id="43b6a-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43b6a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b6a-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43b6a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b6a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="43b6a-135">INPUTS</span></span>

### <span data-ttu-id="43b6a-136">System.object</span><span class="sxs-lookup"><span data-stu-id="43b6a-136">System.String</span></span>

## <span data-ttu-id="43b6a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="43b6a-137">OUTPUTS</span></span>

### <span data-ttu-id="43b6a-138">PSApplicationGatewaySslPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="43b6a-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="43b6a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="43b6a-139">NOTES</span></span>
* <span data-ttu-id="43b6a-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="43b6a-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="43b6a-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="43b6a-141">RELATED LINKS</span></span>

[<span data-ttu-id="43b6a-142">AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="43b6a-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="43b6a-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="43b6a-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


