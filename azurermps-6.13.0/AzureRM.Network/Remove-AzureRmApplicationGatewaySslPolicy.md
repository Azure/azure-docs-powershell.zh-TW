---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3504e4fbdb74fffc41e3f6424540dec71bb209e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448330"
---
# <span data-ttu-id="e2085-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e2085-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e2085-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2085-102">SYNOPSIS</span></span>
<span data-ttu-id="e2085-103">從 Azure 應用程式閘道移除 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="e2085-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2085-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2085-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2085-105">說明</span><span class="sxs-lookup"><span data-stu-id="e2085-105">DESCRIPTION</span></span>
<span data-ttu-id="e2085-106">Remove-AzureRmApplicationGatewaySslPolicy Cmdlet 會從 Azure 應用程式閘道移除 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="e2085-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="e2085-107">示例</span><span class="sxs-lookup"><span data-stu-id="e2085-107">EXAMPLES</span></span>

### <span data-ttu-id="e2085-108">範例1：從應用程式閘道移除 SSL 原則</span><span class="sxs-lookup"><span data-stu-id="e2085-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="e2085-109">這個命令會從名為 ApplicationGateway01 的應用程式閘道中移除 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="e2085-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="e2085-110">參數</span><span class="sxs-lookup"><span data-stu-id="e2085-110">PARAMETERS</span></span>

### <span data-ttu-id="e2085-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2085-111">-ApplicationGateway</span></span>
<span data-ttu-id="e2085-112">指定此 Cmdlet 移除 SSL 原則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e2085-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="e2085-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2085-113">-DefaultProfile</span></span>
<span data-ttu-id="e2085-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2085-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2085-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e2085-115">-Force</span></span>
<span data-ttu-id="e2085-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="e2085-116">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2085-117">-確認</span><span class="sxs-lookup"><span data-stu-id="e2085-117">-Confirm</span></span>
<span data-ttu-id="e2085-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e2085-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2085-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2085-119">-WhatIf</span></span>
<span data-ttu-id="e2085-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2085-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2085-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2085-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2085-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2085-122">CommonParameters</span></span>
<span data-ttu-id="e2085-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2085-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2085-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2085-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2085-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e2085-125">INPUTS</span></span>

### <span data-ttu-id="e2085-126">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e2085-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="e2085-127">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e2085-127">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="e2085-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e2085-128">OUTPUTS</span></span>

### <span data-ttu-id="e2085-129">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e2085-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2085-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e2085-130">NOTES</span></span>
<span data-ttu-id="e2085-131">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="e2085-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e2085-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2085-132">RELATED LINKS</span></span>

[<span data-ttu-id="e2085-133">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e2085-133">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e2085-134">新-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e2085-134">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e2085-135">AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e2085-135">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

