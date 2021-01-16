---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 541293160a1cf9e3d32de5d378c24d1ee4b2705b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274507"
---
# <span data-ttu-id="78bab-101">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="78bab-101">Remove-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="78bab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78bab-102">SYNOPSIS</span></span>
<span data-ttu-id="78bab-103">從 Azure 應用程式閘道 SSL 設定檔移除 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="78bab-103">Removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="78bab-104">句法</span><span class="sxs-lookup"><span data-stu-id="78bab-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78bab-105">說明</span><span class="sxs-lookup"><span data-stu-id="78bab-105">DESCRIPTION</span></span>
<span data-ttu-id="78bab-106">Remove-AzApplicationGatewaySslProfilePolicy Cmdlet 會從 Azure 應用程式閘道 SSL 設定檔中移除 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="78bab-106">The Remove-AzApplicationGatewaySslProfilePolicy cmdlet removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="78bab-107">示例</span><span class="sxs-lookup"><span data-stu-id="78bab-107">EXAMPLES</span></span>

### <span data-ttu-id="78bab-108">範例1</span><span class="sxs-lookup"><span data-stu-id="78bab-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> $profile = Remove-AzApplicationGatewaySslProfilePolicy -SslProfile $profile
```

<span data-ttu-id="78bab-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="78bab-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="78bab-110">第二個命令會針對 $AppGw 取得名為 Profile01 的 SSL 設定檔，並將它儲存在 $profile 變數中。</span><span class="sxs-lookup"><span data-stu-id="78bab-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="78bab-111">最後一個命令會移除 $profile 中儲存的 ssl 設定檔 ssl 原則。</span><span class="sxs-lookup"><span data-stu-id="78bab-111">The last command removes the ssl policy of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="78bab-112">參數</span><span class="sxs-lookup"><span data-stu-id="78bab-112">PARAMETERS</span></span>

### <span data-ttu-id="78bab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78bab-113">-DefaultProfile</span></span>
<span data-ttu-id="78bab-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78bab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78bab-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="78bab-115">-SslProfile</span></span>
<span data-ttu-id="78bab-116">ApplicationGateway SSL 設定檔</span><span class="sxs-lookup"><span data-stu-id="78bab-116">The applicationGateway SSL profile</span></span>

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

### <span data-ttu-id="78bab-117">-確認</span><span class="sxs-lookup"><span data-stu-id="78bab-117">-Confirm</span></span>
<span data-ttu-id="78bab-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78bab-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78bab-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78bab-119">-WhatIf</span></span>
<span data-ttu-id="78bab-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78bab-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78bab-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78bab-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78bab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78bab-122">CommonParameters</span></span>
<span data-ttu-id="78bab-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78bab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78bab-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="78bab-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78bab-125">輸入</span><span class="sxs-lookup"><span data-stu-id="78bab-125">INPUTS</span></span>

### <span data-ttu-id="78bab-126">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="78bab-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="78bab-127">輸出</span><span class="sxs-lookup"><span data-stu-id="78bab-127">OUTPUTS</span></span>

### <span data-ttu-id="78bab-128">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="78bab-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="78bab-129">筆記</span><span class="sxs-lookup"><span data-stu-id="78bab-129">NOTES</span></span>

## <span data-ttu-id="78bab-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="78bab-130">RELATED LINKS</span></span>

[<span data-ttu-id="78bab-131">新-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="78bab-131">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="78bab-132">附加 AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="78bab-132">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="78bab-133">AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="78bab-133">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="78bab-134">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="78bab-134">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)