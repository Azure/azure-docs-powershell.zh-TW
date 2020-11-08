---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a5b0fa1054136354725ec404960bcf680a104d06
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139743"
---
# <span data-ttu-id="852f5-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="852f5-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="852f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="852f5-102">SYNOPSIS</span></span>
<span data-ttu-id="852f5-103">更新應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="852f5-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="852f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="852f5-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="852f5-105">說明</span><span class="sxs-lookup"><span data-stu-id="852f5-105">DESCRIPTION</span></span>
<span data-ttu-id="852f5-106">**AzApplicationGatewayBackendAddressPool** Cmdlet 會更新 Azure 應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="852f5-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="852f5-107">後端位址可以指定為 IP 位址、完全限定的功能變數名稱 (FQDN) 或 IP 配置 Id。</span><span class="sxs-lookup"><span data-stu-id="852f5-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="852f5-108">示例</span><span class="sxs-lookup"><span data-stu-id="852f5-108">EXAMPLES</span></span>

### <span data-ttu-id="852f5-109">範例1：使用 Fqdn 設定後端位址集區</span><span class="sxs-lookup"><span data-stu-id="852f5-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="852f5-110">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="852f5-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="852f5-111">第二個命令會使用 Fqdn，在 $AppGw 中更新應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="852f5-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="852f5-112">範例2：使用後端伺服器 IP 位址設定後端位址集區</span><span class="sxs-lookup"><span data-stu-id="852f5-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="852f5-113">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="852f5-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="852f5-114">第二個命令會在 $AppGw 中使用 IP 位址來更新應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="852f5-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="852f5-115">參數</span><span class="sxs-lookup"><span data-stu-id="852f5-115">PARAMETERS</span></span>

### <span data-ttu-id="852f5-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="852f5-116">-ApplicationGateway</span></span>
<span data-ttu-id="852f5-117">指定此 Cmdlet 與後端位址集區關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="852f5-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="852f5-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="852f5-118">-BackendFqdns</span></span>
<span data-ttu-id="852f5-119">指定要用來做為後端伺服器池的後端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="852f5-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="852f5-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="852f5-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="852f5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="852f5-121">-DefaultProfile</span></span>
<span data-ttu-id="852f5-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="852f5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="852f5-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="852f5-123">-Name</span></span>
<span data-ttu-id="852f5-124">指定後端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="852f5-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="852f5-125">此後端位址集區必須存在於應用程式閘道中。</span><span class="sxs-lookup"><span data-stu-id="852f5-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="852f5-126">-確認</span><span class="sxs-lookup"><span data-stu-id="852f5-126">-Confirm</span></span>
<span data-ttu-id="852f5-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="852f5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="852f5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="852f5-128">-WhatIf</span></span>
<span data-ttu-id="852f5-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="852f5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="852f5-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="852f5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="852f5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="852f5-131">CommonParameters</span></span>
<span data-ttu-id="852f5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="852f5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="852f5-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="852f5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="852f5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="852f5-134">INPUTS</span></span>

### <span data-ttu-id="852f5-135">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="852f5-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="852f5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="852f5-136">OUTPUTS</span></span>

### <span data-ttu-id="852f5-137">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="852f5-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="852f5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="852f5-138">NOTES</span></span>

## <span data-ttu-id="852f5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="852f5-139">RELATED LINKS</span></span>

[<span data-ttu-id="852f5-140">附加 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="852f5-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="852f5-141">AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="852f5-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="852f5-142">新-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="852f5-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="852f5-143">移除-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="852f5-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


