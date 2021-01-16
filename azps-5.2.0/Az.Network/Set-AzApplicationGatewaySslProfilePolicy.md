---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 344be8b71bc74f3620ca90dd60b61f9a59026ea0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276527"
---
# <span data-ttu-id="0e7f4-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="0e7f4-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="0e7f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="0e7f4-103">修改應用程式閘道 SSL 設定檔的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="0e7f4-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="0e7f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e7f4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e7f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="0e7f4-105">DESCRIPTION</span></span>
<span data-ttu-id="0e7f4-106">**AzApplicationGatewaySslProfilePolicy** Cmdlet 會修改應用程式閘道 SSL 設定檔的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="0e7f4-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="0e7f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="0e7f4-107">EXAMPLES</span></span>

### <span data-ttu-id="0e7f4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0e7f4-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="0e7f4-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="0e7f4-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="0e7f4-110">第二個命令會針對 $AppGw 取得名為 SslProfile01 的 ssl 設定檔，並將設定儲存在 $profile 變數中。</span><span class="sxs-lookup"><span data-stu-id="0e7f4-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="0e7f4-111">最後一個命令會修改儲存在 $profile 之 ssl 設定檔物件的 ssl 原則。</span><span class="sxs-lookup"><span data-stu-id="0e7f4-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="0e7f4-112">參數</span><span class="sxs-lookup"><span data-stu-id="0e7f4-112">PARAMETERS</span></span>

### <span data-ttu-id="0e7f4-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="0e7f4-113">-CipherSuite</span></span>
<span data-ttu-id="0e7f4-114">要在應用程式閘道的指定順序啟用 Ssl 密碼套件</span><span class="sxs-lookup"><span data-stu-id="0e7f4-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="0e7f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e7f4-115">-DefaultProfile</span></span>
<span data-ttu-id="0e7f4-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e7f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e7f4-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="0e7f4-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="0e7f4-118">要停用的 SSL 通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="0e7f4-118">List of SSL protocols to be disabled</span></span>

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

### <span data-ttu-id="0e7f4-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="0e7f4-119">-MinProtocolVersion</span></span>
<span data-ttu-id="0e7f4-120">應用程式閘道支援的最小 Ssl 通訊協定版本</span><span class="sxs-lookup"><span data-stu-id="0e7f4-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="0e7f4-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="0e7f4-121">-PolicyName</span></span>
<span data-ttu-id="0e7f4-122">Ssl 預先定義原則的名稱</span><span class="sxs-lookup"><span data-stu-id="0e7f4-122">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="0e7f4-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="0e7f4-123">-PolicyType</span></span>
<span data-ttu-id="0e7f4-124">Ssl 原則類型</span><span class="sxs-lookup"><span data-stu-id="0e7f4-124">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="0e7f4-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="0e7f4-125">-SslProfile</span></span>
<span data-ttu-id="0e7f4-126">應用程式閘道 SSL 設定檔</span><span class="sxs-lookup"><span data-stu-id="0e7f4-126">The application gateway SSL profile</span></span>

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

### <span data-ttu-id="0e7f4-127">-確認</span><span class="sxs-lookup"><span data-stu-id="0e7f4-127">-Confirm</span></span>
<span data-ttu-id="0e7f4-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0e7f4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e7f4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e7f4-129">-WhatIf</span></span>
<span data-ttu-id="0e7f4-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e7f4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e7f4-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e7f4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e7f4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e7f4-132">CommonParameters</span></span>
<span data-ttu-id="0e7f4-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e7f4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e7f4-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0e7f4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e7f4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0e7f4-135">INPUTS</span></span>

### <span data-ttu-id="0e7f4-136">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0e7f4-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="0e7f4-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0e7f4-137">OUTPUTS</span></span>

### <span data-ttu-id="0e7f4-138">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0e7f4-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="0e7f4-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0e7f4-139">NOTES</span></span>

## <span data-ttu-id="0e7f4-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e7f4-140">RELATED LINKS</span></span>

[<span data-ttu-id="0e7f4-141">附加 AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="0e7f4-141">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="0e7f4-142">新-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="0e7f4-142">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="0e7f4-143">AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="0e7f4-143">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="0e7f4-144">移除-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="0e7f4-144">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)