---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 51eb0b5f08da2591ff4398ac9572b17a16cfbc93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449317"
---
# <span data-ttu-id="e7cb5-101">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7cb5-101">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e7cb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="e7cb5-103">將後端位址集區新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-103">Adds a back-end address pool to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7cb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7cb5-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7cb5-105">說明</span><span class="sxs-lookup"><span data-stu-id="e7cb5-105">DESCRIPTION</span></span>
<span data-ttu-id="e7cb5-106">**AzureRmApplicationGatewayBackendAddressPool** Cmdlet 會將後端位址集區新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-106">The **Add-AzureRmApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="e7cb5-107">可使用 IP 位址指定後端位址、完全合格的功能變數名稱 (FQDN) 或 IP 配置 Id。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="e7cb5-108">示例</span><span class="sxs-lookup"><span data-stu-id="e7cb5-108">EXAMPLES</span></span>

### <span data-ttu-id="e7cb5-109">範例1：使用後端伺服器 FQDN 新增後端位址集區</span><span class="sxs-lookup"><span data-stu-id="e7cb5-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="e7cb5-110">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會使用 Fqdn，新增儲存在 $AppGw 中之應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="e7cb5-111">範例2：使用後端伺服器 IP 位址新增後端位址集區</span><span class="sxs-lookup"><span data-stu-id="e7cb5-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="e7cb5-112">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會使用 IP 位址，新增儲存在 $AppGw 中之應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="e7cb5-113">範例3：使用後端伺服器 IP 位址的識別碼 Seta 後端位址集區</span><span class="sxs-lookup"><span data-stu-id="e7cb5-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="e7cb5-114">第一個命令會取得一個名為 Nic01 的網路介面物件，該物件屬於名為 ResourceGroup01 的資源群組，並儲存在 $Nic 01 變數中。第二個命令會取得一個名為 Nic02 的網路介面物件，該物件屬於名為 ResourceGroup02 的資源群組，並儲存在 $Nic 02 變數中。第三個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第四個命令使用 $Nic 01 和 $Nic 02 的後端 IP 配置識別碼來新增儲存在 $AppGw 中之應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="e7cb5-115">參數</span><span class="sxs-lookup"><span data-stu-id="e7cb5-115">PARAMETERS</span></span>

### <span data-ttu-id="e7cb5-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7cb5-116">-ApplicationGateway</span></span>
<span data-ttu-id="e7cb5-117">指定此 Cmdlet 新增後端位址集區的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="e7cb5-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="e7cb5-118">-BackendFqdns</span></span>
<span data-ttu-id="e7cb5-119">指定這個 Cmdlet 作為後端伺服器池加入的後端 Fqdn 清單。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7cb5-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="e7cb5-120">-BackendIPAddresses</span></span>
<span data-ttu-id="e7cb5-121">指定此 Cmdlet 新增為後端伺服器池的後端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7cb5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7cb5-122">-DefaultProfile</span></span>
<span data-ttu-id="e7cb5-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7cb5-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7cb5-124">-Name</span></span>
<span data-ttu-id="e7cb5-125">指定此 Cmdlet 所新增之後端伺服器池的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e7cb5-126">-確認</span><span class="sxs-lookup"><span data-stu-id="e7cb5-126">-Confirm</span></span>
<span data-ttu-id="e7cb5-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7cb5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7cb5-128">-WhatIf</span></span>
<span data-ttu-id="e7cb5-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7cb5-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7cb5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7cb5-131">CommonParameters</span></span>
<span data-ttu-id="e7cb5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7cb5-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e7cb5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7cb5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e7cb5-134">INPUTS</span></span>

###  
<span data-ttu-id="e7cb5-135">System.object</span><span class="sxs-lookup"><span data-stu-id="e7cb5-135">System.String</span></span>

## <span data-ttu-id="e7cb5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e7cb5-136">OUTPUTS</span></span>

### <span data-ttu-id="e7cb5-137">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e7cb5-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e7cb5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e7cb5-138">NOTES</span></span>

## <span data-ttu-id="e7cb5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7cb5-139">RELATED LINKS</span></span>

[<span data-ttu-id="e7cb5-140">AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7cb5-140">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e7cb5-141">AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7cb5-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e7cb5-142">新-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7cb5-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e7cb5-143">移除-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7cb5-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e7cb5-144">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7cb5-144">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


