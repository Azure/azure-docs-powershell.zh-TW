---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 7d04d73905bde7ab008c6910cab708e209125316
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407993"
---
# <span data-ttu-id="5eb90-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5eb90-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="5eb90-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5eb90-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb90-103">修改應用程式閘道 SSL 設定檔的 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="5eb90-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="5eb90-104">語法</span><span class="sxs-lookup"><span data-stu-id="5eb90-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5eb90-105">描述</span><span class="sxs-lookup"><span data-stu-id="5eb90-105">DESCRIPTION</span></span>
<span data-ttu-id="5eb90-106">**Set-AzApplicationGatewaySslProfilePolicy** Cmdlet 會修改應用程式閘道 SSL 設定檔的 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="5eb90-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="5eb90-107">例子</span><span class="sxs-lookup"><span data-stu-id="5eb90-107">EXAMPLES</span></span>

### <span data-ttu-id="5eb90-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="5eb90-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="5eb90-109">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="5eb90-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="5eb90-110">第二個命令會獲得名稱為 SslProfile01 的 ssl 設定檔$AppGw將設定儲存在$profile變數中。</span><span class="sxs-lookup"><span data-stu-id="5eb90-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="5eb90-111">最後一個命令會修改儲存在 $profile 中的 ssl 設定檔物件的 ssl $profile。</span><span class="sxs-lookup"><span data-stu-id="5eb90-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="5eb90-112">參數</span><span class="sxs-lookup"><span data-stu-id="5eb90-112">PARAMETERS</span></span>

### <span data-ttu-id="5eb90-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="5eb90-113">-CipherSuite</span></span>
<span data-ttu-id="5eb90-114">以指定的順序啟用應用程式閘道的 Ssl 密碼套件</span><span class="sxs-lookup"><span data-stu-id="5eb90-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb90-115">-DefaultProfile</span></span>
<span data-ttu-id="5eb90-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5eb90-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb90-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="5eb90-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="5eb90-118">要停用的 SSL 通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="5eb90-118">List of SSL protocols to be disabled</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb90-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="5eb90-119">-MinProtocolVersion</span></span>
<span data-ttu-id="5eb90-120">應用程式閘道支援的最小 Ssl 通訊協定版本</span><span class="sxs-lookup"><span data-stu-id="5eb90-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="5eb90-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="5eb90-121">-PolicyName</span></span>
<span data-ttu-id="5eb90-122">Ssl 預先定義之策略的名稱</span><span class="sxs-lookup"><span data-stu-id="5eb90-122">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="5eb90-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="5eb90-123">-PolicyType</span></span>
<span data-ttu-id="5eb90-124">Ssl 策略類型</span><span class="sxs-lookup"><span data-stu-id="5eb90-124">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="5eb90-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="5eb90-125">-SslProfile</span></span>
<span data-ttu-id="5eb90-126">應用程式閘道 SSL 設定檔</span><span class="sxs-lookup"><span data-stu-id="5eb90-126">The application gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb90-127">-確認</span><span class="sxs-lookup"><span data-stu-id="5eb90-127">-Confirm</span></span>
<span data-ttu-id="5eb90-128">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5eb90-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb90-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eb90-129">-WhatIf</span></span>
<span data-ttu-id="5eb90-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5eb90-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eb90-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5eb90-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb90-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb90-132">CommonParameters</span></span>
<span data-ttu-id="5eb90-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5eb90-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb90-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5eb90-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb90-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5eb90-135">INPUTS</span></span>

### <span data-ttu-id="5eb90-136">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5eb90-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="5eb90-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5eb90-137">OUTPUTS</span></span>

### <span data-ttu-id="5eb90-138">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5eb90-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="5eb90-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5eb90-139">NOTES</span></span>

## <span data-ttu-id="5eb90-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5eb90-140">RELATED LINKS</span></span>



[<span data-ttu-id="5eb90-141">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5eb90-141">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="5eb90-142">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5eb90-142">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)
