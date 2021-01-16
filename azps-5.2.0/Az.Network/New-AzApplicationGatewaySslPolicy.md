---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: cf2f2ef91fa217b1710eeb100f4e3e6c2ce6fb9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280499"
---
# <span data-ttu-id="c2a13-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c2a13-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c2a13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2a13-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a13-103">建立應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="c2a13-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="c2a13-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2a13-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2a13-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2a13-105">DESCRIPTION</span></span>
<span data-ttu-id="c2a13-106">**新的-AzApplicationGatewaySslPolicy** Cmdlet 會為應用程式閘道建立 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="c2a13-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="c2a13-107">示例</span><span class="sxs-lookup"><span data-stu-id="c2a13-107">EXAMPLES</span></span>

### <span data-ttu-id="c2a13-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c2a13-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="c2a13-109">這個命令會建立自訂原則。</span><span class="sxs-lookup"><span data-stu-id="c2a13-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="c2a13-110">參數</span><span class="sxs-lookup"><span data-stu-id="c2a13-110">PARAMETERS</span></span>

### <span data-ttu-id="c2a13-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="c2a13-111">-CipherSuite</span></span>
<span data-ttu-id="c2a13-112">要在應用程式閘道的指定順序啟用 Ssl 密碼套件</span><span class="sxs-lookup"><span data-stu-id="c2a13-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a13-113">-DefaultProfile</span></span>
<span data-ttu-id="c2a13-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2a13-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2a13-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="c2a13-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="c2a13-116">指定停用哪些通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c2a13-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="c2a13-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c2a13-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2a13-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="c2a13-118">TLSv1_0</span></span> 
- <span data-ttu-id="c2a13-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="c2a13-119">TLSv1_1</span></span> 
- <span data-ttu-id="c2a13-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="c2a13-120">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a13-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="c2a13-121">-MinProtocolVersion</span></span>
<span data-ttu-id="c2a13-122">應用程式閘道支援的最小 Ssl 通訊協定版本</span><span class="sxs-lookup"><span data-stu-id="c2a13-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="c2a13-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="c2a13-123">-PolicyName</span></span>
<span data-ttu-id="c2a13-124">Ssl 預先定義原則的名稱</span><span class="sxs-lookup"><span data-stu-id="c2a13-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="c2a13-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="c2a13-125">-PolicyType</span></span>
<span data-ttu-id="c2a13-126">Ssl 原則類型</span><span class="sxs-lookup"><span data-stu-id="c2a13-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="c2a13-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c2a13-127">-Confirm</span></span>
<span data-ttu-id="c2a13-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2a13-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2a13-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2a13-129">-WhatIf</span></span>
<span data-ttu-id="c2a13-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2a13-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2a13-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2a13-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2a13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a13-132">CommonParameters</span></span>
<span data-ttu-id="c2a13-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2a13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a13-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2a13-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a13-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c2a13-135">INPUTS</span></span>

### <span data-ttu-id="c2a13-136">所有</span><span class="sxs-lookup"><span data-stu-id="c2a13-136">None</span></span>

## <span data-ttu-id="c2a13-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c2a13-137">OUTPUTS</span></span>

### <span data-ttu-id="c2a13-138">PSApplicationGatewaySslPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2a13-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c2a13-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c2a13-139">NOTES</span></span>
* <span data-ttu-id="c2a13-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="c2a13-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c2a13-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2a13-141">RELATED LINKS</span></span>

[<span data-ttu-id="c2a13-142">AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c2a13-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="c2a13-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c2a13-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


