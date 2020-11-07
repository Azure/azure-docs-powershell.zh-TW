---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: bafc55d3e630b936d2d30efa168f60919cc6c69d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626549"
---
# <span data-ttu-id="96473-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="96473-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="96473-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96473-102">SYNOPSIS</span></span>
<span data-ttu-id="96473-103">更新應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="96473-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96473-104">句法</span><span class="sxs-lookup"><span data-stu-id="96473-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96473-105">說明</span><span class="sxs-lookup"><span data-stu-id="96473-105">DESCRIPTION</span></span>
<span data-ttu-id="96473-106">**AzureRmApplicationGatewayBackendAddressPool** Cmdlet 會更新 Azure 應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="96473-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="96473-107">後端位址可以指定為 IP 位址、完全限定的功能變數名稱 (FQDN) 或 IP 配置 Id。</span><span class="sxs-lookup"><span data-stu-id="96473-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="96473-108">示例</span><span class="sxs-lookup"><span data-stu-id="96473-108">EXAMPLES</span></span>

### <span data-ttu-id="96473-109">範例1：使用 Fqdn 設定後端位址集區</span><span class="sxs-lookup"><span data-stu-id="96473-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="96473-110">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="96473-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="96473-111">第二個命令會使用 Fqdn，在 $AppGw 中更新應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="96473-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="96473-112">範例2：使用後端伺服器 IP 位址設定後端位址集區</span><span class="sxs-lookup"><span data-stu-id="96473-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="96473-113">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="96473-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="96473-114">第二個命令會在 $AppGw 中使用 IP 位址來更新應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="96473-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="96473-115">參數</span><span class="sxs-lookup"><span data-stu-id="96473-115">PARAMETERS</span></span>

### <span data-ttu-id="96473-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96473-116">-ApplicationGateway</span></span>
<span data-ttu-id="96473-117">指定此 Cmdlet 與後端位址集區關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="96473-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="96473-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="96473-118">-BackendFqdns</span></span>
<span data-ttu-id="96473-119">指定要用來做為後端伺服器池的後端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="96473-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="96473-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="96473-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="96473-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96473-121">-DefaultProfile</span></span>
<span data-ttu-id="96473-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96473-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96473-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="96473-123">-Name</span></span>
<span data-ttu-id="96473-124">指定後端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="96473-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="96473-125">此後端位址集區必須存在於應用程式閘道中。</span><span class="sxs-lookup"><span data-stu-id="96473-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="96473-126">-確認</span><span class="sxs-lookup"><span data-stu-id="96473-126">-Confirm</span></span>
<span data-ttu-id="96473-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="96473-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96473-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96473-128">-WhatIf</span></span>
<span data-ttu-id="96473-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96473-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96473-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96473-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96473-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96473-131">CommonParameters</span></span>
<span data-ttu-id="96473-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96473-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96473-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96473-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96473-134">輸入</span><span class="sxs-lookup"><span data-stu-id="96473-134">INPUTS</span></span>

### <span data-ttu-id="96473-135">System.object</span><span class="sxs-lookup"><span data-stu-id="96473-135">System.String</span></span>

## <span data-ttu-id="96473-136">輸出</span><span class="sxs-lookup"><span data-stu-id="96473-136">OUTPUTS</span></span>

### <span data-ttu-id="96473-137">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="96473-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96473-138">筆記</span><span class="sxs-lookup"><span data-stu-id="96473-138">NOTES</span></span>

## <span data-ttu-id="96473-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="96473-139">RELATED LINKS</span></span>

[<span data-ttu-id="96473-140">附加 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="96473-140">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="96473-141">AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="96473-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="96473-142">新-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="96473-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="96473-143">移除-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="96473-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


