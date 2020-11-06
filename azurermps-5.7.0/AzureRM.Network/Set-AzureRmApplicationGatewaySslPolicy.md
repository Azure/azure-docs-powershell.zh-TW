---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 7ab968539cb57568540a0e1c60f59b36d6de79ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447029"
---
# <span data-ttu-id="4f648-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4f648-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="4f648-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f648-102">SYNOPSIS</span></span>
<span data-ttu-id="4f648-103">修改應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="4f648-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f648-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f648-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f648-105">說明</span><span class="sxs-lookup"><span data-stu-id="4f648-105">DESCRIPTION</span></span>
<span data-ttu-id="4f648-106">**AzureRmApplicationGatewaySslPolicy** Cmdlet 會修改應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="4f648-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="4f648-107">示例</span><span class="sxs-lookup"><span data-stu-id="4f648-107">EXAMPLES</span></span>

### <span data-ttu-id="4f648-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="4f648-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="4f648-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4f648-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4f648-110">這個第二個命令會將 ssl 原則修改為預先定義的原則，以及策略名稱 AppGwSslPolicy20170401。</span><span class="sxs-lookup"><span data-stu-id="4f648-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="4f648-111">參數</span><span class="sxs-lookup"><span data-stu-id="4f648-111">PARAMETERS</span></span>

### <span data-ttu-id="4f648-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4f648-112">-ApplicationGateway</span></span>
<span data-ttu-id="4f648-113">指定此 Cmdlet 所修改之 SSL 原則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4f648-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4f648-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="4f648-114">-CipherSuite</span></span>
<span data-ttu-id="4f648-115">要在應用程式閘道的指定順序啟用 Ssl 密碼套件</span><span class="sxs-lookup"><span data-stu-id="4f648-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="4f648-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f648-116">-DefaultProfile</span></span>
<span data-ttu-id="4f648-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f648-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f648-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="4f648-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="4f648-119">指定停用哪些通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4f648-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="4f648-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4f648-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f648-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="4f648-121">TLSv1_0</span></span> 
- <span data-ttu-id="4f648-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="4f648-122">TLSv1_1</span></span> 
- <span data-ttu-id="4f648-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="4f648-123">TLSv1_2</span></span>

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

### <span data-ttu-id="4f648-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="4f648-124">-MinProtocolVersion</span></span>
<span data-ttu-id="4f648-125">應用程式閘道支援的最小 Ssl 通訊協定版本</span><span class="sxs-lookup"><span data-stu-id="4f648-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="4f648-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="4f648-126">-PolicyName</span></span>
<span data-ttu-id="4f648-127">Ssl 預先定義原則的名稱</span><span class="sxs-lookup"><span data-stu-id="4f648-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="4f648-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="4f648-128">-PolicyType</span></span>
<span data-ttu-id="4f648-129">Ssl 原則類型</span><span class="sxs-lookup"><span data-stu-id="4f648-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="4f648-130">-確認</span><span class="sxs-lookup"><span data-stu-id="4f648-130">-Confirm</span></span>
<span data-ttu-id="4f648-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f648-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f648-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f648-132">-WhatIf</span></span>
<span data-ttu-id="4f648-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f648-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f648-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f648-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f648-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f648-135">CommonParameters</span></span>
<span data-ttu-id="4f648-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f648-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f648-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f648-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f648-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4f648-138">INPUTS</span></span>

### <span data-ttu-id="4f648-139">System.object</span><span class="sxs-lookup"><span data-stu-id="4f648-139">System.String</span></span>

## <span data-ttu-id="4f648-140">輸出</span><span class="sxs-lookup"><span data-stu-id="4f648-140">OUTPUTS</span></span>

### <span data-ttu-id="4f648-141">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4f648-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4f648-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4f648-142">NOTES</span></span>
* <span data-ttu-id="4f648-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="4f648-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4f648-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f648-144">RELATED LINKS</span></span>

[<span data-ttu-id="4f648-145">AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4f648-145">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="4f648-146">新-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4f648-146">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)


