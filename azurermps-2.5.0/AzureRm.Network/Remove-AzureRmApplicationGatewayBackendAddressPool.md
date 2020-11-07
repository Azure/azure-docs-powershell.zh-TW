---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 7b82cf189d912d000c143b20cca76c4f2683b7d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801218"
---
# <span data-ttu-id="ae36e-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae36e-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ae36e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae36e-102">SYNOPSIS</span></span>
<span data-ttu-id="ae36e-103">從應用程式閘道移除後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="ae36e-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae36e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae36e-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae36e-105">說明</span><span class="sxs-lookup"><span data-stu-id="ae36e-105">DESCRIPTION</span></span>
<span data-ttu-id="ae36e-106">**AzureRmApplicationGatewayBackendAddressPool** Cmdlet 會從 Azure 應用程式閘道中移除後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="ae36e-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="ae36e-107">示例</span><span class="sxs-lookup"><span data-stu-id="ae36e-107">EXAMPLES</span></span>

### <span data-ttu-id="ae36e-108">範例1：從應用程式閘道移除後端位址集區</span><span class="sxs-lookup"><span data-stu-id="ae36e-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="ae36e-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將其儲存于名為 ResourceGroup01 的資源群組，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="ae36e-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="ae36e-110">第二個命令會從應用程式閘道移除名為 BackEndPool02 的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="ae36e-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="ae36e-111">參數</span><span class="sxs-lookup"><span data-stu-id="ae36e-111">PARAMETERS</span></span>

### <span data-ttu-id="ae36e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae36e-112">-ApplicationGateway</span></span>
<span data-ttu-id="ae36e-113">指定此 Cmdlet 從中移除後端位址集區的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ae36e-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="ae36e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae36e-114">-DefaultProfile</span></span>
<span data-ttu-id="ae36e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae36e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae36e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae36e-116">-Name</span></span>
<span data-ttu-id="ae36e-117">指定此 Cmdlet 移除之後端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae36e-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae36e-118">-確認</span><span class="sxs-lookup"><span data-stu-id="ae36e-118">-Confirm</span></span>
<span data-ttu-id="ae36e-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae36e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae36e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae36e-120">-WhatIf</span></span>
<span data-ttu-id="ae36e-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae36e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae36e-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae36e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae36e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae36e-123">CommonParameters</span></span>
<span data-ttu-id="ae36e-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae36e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae36e-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae36e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae36e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="ae36e-126">INPUTS</span></span>

### <span data-ttu-id="ae36e-127">System.object</span><span class="sxs-lookup"><span data-stu-id="ae36e-127">System.String</span></span>

## <span data-ttu-id="ae36e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ae36e-128">OUTPUTS</span></span>

### <span data-ttu-id="ae36e-129">PSApplicationGatewayBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ae36e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ae36e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ae36e-130">NOTES</span></span>

## <span data-ttu-id="ae36e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae36e-131">RELATED LINKS</span></span>

[<span data-ttu-id="ae36e-132">附加 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae36e-132">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ae36e-133">AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae36e-133">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ae36e-134">新-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae36e-134">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ae36e-135">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae36e-135">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


