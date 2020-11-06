---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 7b92f090a4866dabeb064e828dbf3386e26fcb53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449284"
---
# <span data-ttu-id="2a7cd-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a7cd-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="2a7cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="2a7cd-103">建立應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a7cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a7cd-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a7cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="2a7cd-105">DESCRIPTION</span></span>
<span data-ttu-id="2a7cd-106">**新的 AzureRmApplicationGatewayBackendAddressPool** Cmdlet 會建立 Azure 應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="2a7cd-107">後端位址可以指定為 IP 位址、完全合格的功能變數名稱 (FQDN) 或 IP 配置 ID。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="2a7cd-108">示例</span><span class="sxs-lookup"><span data-stu-id="2a7cd-108">EXAMPLES</span></span>

### <span data-ttu-id="2a7cd-109">範例1：使用後端伺服器的 FQDN 建立後端位址集區</span><span class="sxs-lookup"><span data-stu-id="2a7cd-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="2a7cd-110">這個命令會使用後端伺服器的 Fqdn 建立名為 Pool01 的後端位址集區，並將它儲存在 $Pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="2a7cd-111">範例2：使用後端伺服器的 IP 位址來建立後端位址集區</span><span class="sxs-lookup"><span data-stu-id="2a7cd-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="2a7cd-112">這個命令會使用後端伺服器的 IP 位址，建立名為 Pool02 的後端位址集區，並將它儲存在 $Pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="2a7cd-113">參數</span><span class="sxs-lookup"><span data-stu-id="2a7cd-113">PARAMETERS</span></span>

### <span data-ttu-id="2a7cd-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="2a7cd-114">-BackendFqdns</span></span>
<span data-ttu-id="2a7cd-115">指定此 Cmdlet 與後端伺服器池相關聯的後端 Fqdn 清單。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="2a7cd-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="2a7cd-116">-BackendIPAddresses</span></span>
<span data-ttu-id="2a7cd-117">指定此 Cmdlet 與後端伺服器池相關聯的後端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="2a7cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a7cd-118">-DefaultProfile</span></span>
<span data-ttu-id="2a7cd-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a7cd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a7cd-120">-Name</span></span>
<span data-ttu-id="2a7cd-121">指定此 Cmdlet 建立的後端伺服器池的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2a7cd-122">-確認</span><span class="sxs-lookup"><span data-stu-id="2a7cd-122">-Confirm</span></span>
<span data-ttu-id="2a7cd-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a7cd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a7cd-124">-WhatIf</span></span>
<span data-ttu-id="2a7cd-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a7cd-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a7cd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a7cd-127">CommonParameters</span></span>
<span data-ttu-id="2a7cd-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a7cd-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a7cd-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2a7cd-130">INPUTS</span></span>

### <span data-ttu-id="2a7cd-131">System.object</span><span class="sxs-lookup"><span data-stu-id="2a7cd-131">System.String</span></span>

## <span data-ttu-id="2a7cd-132">輸出</span><span class="sxs-lookup"><span data-stu-id="2a7cd-132">OUTPUTS</span></span>

### <span data-ttu-id="2a7cd-133">PSApplicationGatewayBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2a7cd-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="2a7cd-134">筆記</span><span class="sxs-lookup"><span data-stu-id="2a7cd-134">NOTES</span></span>

## <span data-ttu-id="2a7cd-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a7cd-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a7cd-136">附加 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a7cd-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="2a7cd-137">AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a7cd-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="2a7cd-138">移除-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a7cd-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="2a7cd-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a7cd-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


