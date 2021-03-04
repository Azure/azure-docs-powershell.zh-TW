---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 672286da502500101846d6fae694af059328c3cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903989"
---
# <span data-ttu-id="c1da3-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1da3-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="c1da3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1da3-102">SYNOPSIS</span></span>
<span data-ttu-id="c1da3-103">更新應用程式閘道的後端位址資料庫。</span><span class="sxs-lookup"><span data-stu-id="c1da3-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="c1da3-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1da3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1da3-105">描述</span><span class="sxs-lookup"><span data-stu-id="c1da3-105">DESCRIPTION</span></span>
<span data-ttu-id="c1da3-106">**Set-AzApplicationGatewayBackendAddressPool** Cmdlet 會更新 Azure 應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="c1da3-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="c1da3-107">後端位址可指定為 IP 位址、FQDN (或 IP) 的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="c1da3-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="c1da3-108">例子</span><span class="sxs-lookup"><span data-stu-id="c1da3-108">EXAMPLES</span></span>

### <span data-ttu-id="c1da3-109">範例 1：使用 FQDNs 設定後端位址區</span><span class="sxs-lookup"><span data-stu-id="c1da3-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="c1da3-110">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="c1da3-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c1da3-111">第二個命令會使用 FQNS 更新 $AppGw 閘道的後端位址資料庫。</span><span class="sxs-lookup"><span data-stu-id="c1da3-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="c1da3-112">範例 2：使用後端伺服器 IP 位址設定後端位址資料庫</span><span class="sxs-lookup"><span data-stu-id="c1da3-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="c1da3-113">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="c1da3-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c1da3-114">第二個命令會使用 IP 位址更新 $AppGw 中應用程式閘道的後端位址資料庫。</span><span class="sxs-lookup"><span data-stu-id="c1da3-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="c1da3-115">參數</span><span class="sxs-lookup"><span data-stu-id="c1da3-115">PARAMETERS</span></span>

### <span data-ttu-id="c1da3-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1da3-116">-ApplicationGateway</span></span>
<span data-ttu-id="c1da3-117">指定此 Cmdlet 與後端位址區關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c1da3-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="c1da3-118">-後端Fqdns</span><span class="sxs-lookup"><span data-stu-id="c1da3-118">-BackendFqdns</span></span>
<span data-ttu-id="c1da3-119">指定要作為後端伺服器資料庫的後端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="c1da3-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="c1da3-120">-後端IPAddresses</span><span class="sxs-lookup"><span data-stu-id="c1da3-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="c1da3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1da3-121">-DefaultProfile</span></span>
<span data-ttu-id="c1da3-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1da3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1da3-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1da3-123">-Name</span></span>
<span data-ttu-id="c1da3-124">指定後端位址區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1da3-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="c1da3-125">這個後端位址區必須存在於應用程式閘道中。</span><span class="sxs-lookup"><span data-stu-id="c1da3-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="c1da3-126">-確認</span><span class="sxs-lookup"><span data-stu-id="c1da3-126">-Confirm</span></span>
<span data-ttu-id="c1da3-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c1da3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1da3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1da3-128">-WhatIf</span></span>
<span data-ttu-id="c1da3-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1da3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1da3-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1da3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1da3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1da3-131">CommonParameters</span></span>
<span data-ttu-id="c1da3-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1da3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1da3-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c1da3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1da3-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c1da3-134">INPUTS</span></span>

### <span data-ttu-id="c1da3-135">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1da3-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1da3-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c1da3-136">OUTPUTS</span></span>

### <span data-ttu-id="c1da3-137">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1da3-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1da3-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c1da3-138">NOTES</span></span>

## <span data-ttu-id="c1da3-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1da3-139">RELATED LINKS</span></span>

[<span data-ttu-id="c1da3-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1da3-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c1da3-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1da3-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c1da3-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1da3-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c1da3-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1da3-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


