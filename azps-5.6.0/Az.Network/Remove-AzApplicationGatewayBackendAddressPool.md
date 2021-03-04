---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 202801e39e62b265b39036793ed4369a5d98bf2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916515"
---
# <span data-ttu-id="f06d4-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f06d4-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f06d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f06d4-102">SYNOPSIS</span></span>
<span data-ttu-id="f06d4-103">從應用程式閘道移除後端位址庫。</span><span class="sxs-lookup"><span data-stu-id="f06d4-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="f06d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="f06d4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f06d4-105">描述</span><span class="sxs-lookup"><span data-stu-id="f06d4-105">DESCRIPTION</span></span>
<span data-ttu-id="f06d4-106">**Remove-AzApplicationGatewayBackendAddressPool** Cmdlet 會從 Azure 應用程式閘道移除後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="f06d4-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="f06d4-107">例子</span><span class="sxs-lookup"><span data-stu-id="f06d4-107">EXAMPLES</span></span>

### <span data-ttu-id="f06d4-108">範例 1：從應用程式閘道移除後端位址庫</span><span class="sxs-lookup"><span data-stu-id="f06d4-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="f06d4-109">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並會將它$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="f06d4-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="f06d4-110">第二個命令會從應用程式閘道移除名為 BackEndPool02 的後端位址庫。</span><span class="sxs-lookup"><span data-stu-id="f06d4-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="f06d4-111">參數</span><span class="sxs-lookup"><span data-stu-id="f06d4-111">PARAMETERS</span></span>

### <span data-ttu-id="f06d4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f06d4-112">-ApplicationGateway</span></span>
<span data-ttu-id="f06d4-113">指定此 Cmdlet 會移除後端位址區的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="f06d4-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="f06d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f06d4-114">-DefaultProfile</span></span>
<span data-ttu-id="f06d4-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f06d4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f06d4-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f06d4-116">-Name</span></span>
<span data-ttu-id="f06d4-117">指定此 Cmdlet 移除的後端位址組名。</span><span class="sxs-lookup"><span data-stu-id="f06d4-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f06d4-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f06d4-118">-Confirm</span></span>
<span data-ttu-id="f06d4-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f06d4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f06d4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f06d4-120">-WhatIf</span></span>
<span data-ttu-id="f06d4-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f06d4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f06d4-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f06d4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f06d4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f06d4-123">CommonParameters</span></span>
<span data-ttu-id="f06d4-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f06d4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f06d4-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f06d4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f06d4-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f06d4-126">INPUTS</span></span>

### <span data-ttu-id="f06d4-127">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f06d4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f06d4-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f06d4-128">OUTPUTS</span></span>

### <span data-ttu-id="f06d4-129">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f06d4-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f06d4-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f06d4-130">NOTES</span></span>

## <span data-ttu-id="f06d4-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f06d4-131">RELATED LINKS</span></span>

[<span data-ttu-id="f06d4-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f06d4-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f06d4-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f06d4-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f06d4-134">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f06d4-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f06d4-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f06d4-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


