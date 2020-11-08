---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1ce5989516286d366e6363cbeeee8ebddc93edfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126434"
---
# <span data-ttu-id="545bb-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="545bb-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="545bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="545bb-102">SYNOPSIS</span></span>
<span data-ttu-id="545bb-103">從應用程式閘道移除後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="545bb-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="545bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="545bb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="545bb-105">說明</span><span class="sxs-lookup"><span data-stu-id="545bb-105">DESCRIPTION</span></span>
<span data-ttu-id="545bb-106">**AzApplicationGatewayBackendAddressPool** Cmdlet 會從 Azure 應用程式閘道中移除後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="545bb-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="545bb-107">示例</span><span class="sxs-lookup"><span data-stu-id="545bb-107">EXAMPLES</span></span>

### <span data-ttu-id="545bb-108">範例1：從應用程式閘道移除後端位址集區</span><span class="sxs-lookup"><span data-stu-id="545bb-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="545bb-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將其儲存于名為 ResourceGroup01 的資源群組，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="545bb-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="545bb-110">第二個命令會從應用程式閘道移除名為 BackEndPool02 的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="545bb-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="545bb-111">參數</span><span class="sxs-lookup"><span data-stu-id="545bb-111">PARAMETERS</span></span>

### <span data-ttu-id="545bb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="545bb-112">-ApplicationGateway</span></span>
<span data-ttu-id="545bb-113">指定此 Cmdlet 從中移除後端位址集區的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="545bb-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="545bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545bb-114">-DefaultProfile</span></span>
<span data-ttu-id="545bb-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="545bb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="545bb-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="545bb-116">-Name</span></span>
<span data-ttu-id="545bb-117">指定此 Cmdlet 移除之後端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="545bb-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="545bb-118">-確認</span><span class="sxs-lookup"><span data-stu-id="545bb-118">-Confirm</span></span>
<span data-ttu-id="545bb-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="545bb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="545bb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="545bb-120">-WhatIf</span></span>
<span data-ttu-id="545bb-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="545bb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="545bb-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="545bb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="545bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545bb-123">CommonParameters</span></span>
<span data-ttu-id="545bb-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="545bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545bb-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="545bb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545bb-126">輸入</span><span class="sxs-lookup"><span data-stu-id="545bb-126">INPUTS</span></span>

### <span data-ttu-id="545bb-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="545bb-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="545bb-128">輸出</span><span class="sxs-lookup"><span data-stu-id="545bb-128">OUTPUTS</span></span>

### <span data-ttu-id="545bb-129">PSApplicationGatewayBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="545bb-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="545bb-130">筆記</span><span class="sxs-lookup"><span data-stu-id="545bb-130">NOTES</span></span>

## <span data-ttu-id="545bb-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="545bb-131">RELATED LINKS</span></span>

[<span data-ttu-id="545bb-132">附加 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="545bb-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="545bb-133">AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="545bb-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="545bb-134">新-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="545bb-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="545bb-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="545bb-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


