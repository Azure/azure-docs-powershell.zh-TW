---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 88a89a17adc7a05e75865121d2133f723e534fcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903997"
---
# <span data-ttu-id="f0ef0-101">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f0ef0-101">Remove-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="f0ef0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ef0-103">從 Azure 應用程式閘道 SSL 設定檔移除 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="f0ef0-103">Removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="f0ef0-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0ef0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0ef0-105">描述</span><span class="sxs-lookup"><span data-stu-id="f0ef0-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ef0-106">Cmdlet Remove-AzApplicationGatewaySslProfilePolicy Azure 應用程式閘道 SSL 設定檔移除 SSL 策略。</span><span class="sxs-lookup"><span data-stu-id="f0ef0-106">The Remove-AzApplicationGatewaySslProfilePolicy cmdlet removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="f0ef0-107">例子</span><span class="sxs-lookup"><span data-stu-id="f0ef0-107">EXAMPLES</span></span>

### <span data-ttu-id="f0ef0-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f0ef0-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> $profile = Remove-AzApplicationGatewaySslProfilePolicy -SslProfile $profile
```

<span data-ttu-id="f0ef0-109">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="f0ef0-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="f0ef0-110">第二個命令會獲得名稱為 Profile01 的 SSL 設定檔$AppGw並儲存在$profile變數中。</span><span class="sxs-lookup"><span data-stu-id="f0ef0-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="f0ef0-111">最後一個命令會移除儲存在 $profile 中的 ssl 設定檔$profile。</span><span class="sxs-lookup"><span data-stu-id="f0ef0-111">The last command removes the ssl policy of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="f0ef0-112">參數</span><span class="sxs-lookup"><span data-stu-id="f0ef0-112">PARAMETERS</span></span>

### <span data-ttu-id="f0ef0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ef0-113">-DefaultProfile</span></span>
<span data-ttu-id="f0ef0-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0ef0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ef0-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="f0ef0-115">-SslProfile</span></span>
<span data-ttu-id="f0ef0-116">ApplicationGateway SSL 設定檔</span><span class="sxs-lookup"><span data-stu-id="f0ef0-116">The applicationGateway SSL profile</span></span>

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

### <span data-ttu-id="f0ef0-117">-確認</span><span class="sxs-lookup"><span data-stu-id="f0ef0-117">-Confirm</span></span>
<span data-ttu-id="f0ef0-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f0ef0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0ef0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ef0-119">-WhatIf</span></span>
<span data-ttu-id="f0ef0-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0ef0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0ef0-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0ef0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0ef0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ef0-122">CommonParameters</span></span>
<span data-ttu-id="f0ef0-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0ef0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ef0-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0ef0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ef0-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f0ef0-125">INPUTS</span></span>

### <span data-ttu-id="f0ef0-126">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f0ef0-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f0ef0-127">輸出</span><span class="sxs-lookup"><span data-stu-id="f0ef0-127">OUTPUTS</span></span>

### <span data-ttu-id="f0ef0-128">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f0ef0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f0ef0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f0ef0-129">NOTES</span></span>

## <span data-ttu-id="f0ef0-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0ef0-130">RELATED LINKS</span></span>

[<span data-ttu-id="f0ef0-131">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f0ef0-131">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="f0ef0-132">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f0ef0-132">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="f0ef0-133">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f0ef0-133">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="f0ef0-134">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f0ef0-134">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)