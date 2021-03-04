---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 3ce9cb761bb945c777a39e728ac8ebea2c40b885
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916720"
---
# <span data-ttu-id="16987-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="16987-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="16987-102">簡介</span><span class="sxs-lookup"><span data-stu-id="16987-102">SYNOPSIS</span></span>
<span data-ttu-id="16987-103">為應用程式閘道建立後端位址庫。</span><span class="sxs-lookup"><span data-stu-id="16987-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="16987-104">語法</span><span class="sxs-lookup"><span data-stu-id="16987-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16987-105">描述</span><span class="sxs-lookup"><span data-stu-id="16987-105">DESCRIPTION</span></span>
<span data-ttu-id="16987-106">**New-AzApplicationGatewayBackendAddressPool** Cmdlet 會為 Azure 應用程式閘道建立後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="16987-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="16987-107">後端位址可指定為 IP 位址、FQDN (完整功能變數名稱) IP 組組識別碼。</span><span class="sxs-lookup"><span data-stu-id="16987-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="16987-108">例子</span><span class="sxs-lookup"><span data-stu-id="16987-108">EXAMPLES</span></span>

### <span data-ttu-id="16987-109">範例 1：使用後端伺服器的 FQDN 建立後端位址資料庫</span><span class="sxs-lookup"><span data-stu-id="16987-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="16987-110">此命令會使用後端伺服器的 FQDN 建立名為 Pool01 的後端位址資料庫，並儲存在 $Pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="16987-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="16987-111">範例 2：使用後端伺服器的 IP 位址建立後端位址資料庫</span><span class="sxs-lookup"><span data-stu-id="16987-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="16987-112">此命令會使用後端伺服器的 IP 位址建立名為 Pool02 的後端位址資料庫，並儲存在 $Pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="16987-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="16987-113">參數</span><span class="sxs-lookup"><span data-stu-id="16987-113">PARAMETERS</span></span>

### <span data-ttu-id="16987-114">-後端Fqdns</span><span class="sxs-lookup"><span data-stu-id="16987-114">-BackendFqdns</span></span>
<span data-ttu-id="16987-115">指定此 Cmdlet 與後端伺服器資料庫關聯之後端 FQDN 的清單。</span><span class="sxs-lookup"><span data-stu-id="16987-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="16987-116">-後端IPAddresses</span><span class="sxs-lookup"><span data-stu-id="16987-116">-BackendIPAddresses</span></span>
<span data-ttu-id="16987-117">指定此 Cmdlet 與後端伺服器資料庫關聯之後端 IP 位址的清單。</span><span class="sxs-lookup"><span data-stu-id="16987-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="16987-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16987-118">-DefaultProfile</span></span>
<span data-ttu-id="16987-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="16987-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16987-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="16987-120">-Name</span></span>
<span data-ttu-id="16987-121">指定此 Cmdlet 所建立之後端伺服器資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="16987-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="16987-122">-確認</span><span class="sxs-lookup"><span data-stu-id="16987-122">-Confirm</span></span>
<span data-ttu-id="16987-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="16987-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16987-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16987-124">-WhatIf</span></span>
<span data-ttu-id="16987-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16987-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16987-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16987-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16987-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16987-127">CommonParameters</span></span>
<span data-ttu-id="16987-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="16987-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16987-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="16987-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16987-130">輸入</span><span class="sxs-lookup"><span data-stu-id="16987-130">INPUTS</span></span>

### <span data-ttu-id="16987-131">沒有</span><span class="sxs-lookup"><span data-stu-id="16987-131">None</span></span>

## <span data-ttu-id="16987-132">輸出</span><span class="sxs-lookup"><span data-stu-id="16987-132">OUTPUTS</span></span>

### <span data-ttu-id="16987-133">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="16987-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="16987-134">筆記</span><span class="sxs-lookup"><span data-stu-id="16987-134">NOTES</span></span>

## <span data-ttu-id="16987-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="16987-135">RELATED LINKS</span></span>

[<span data-ttu-id="16987-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="16987-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="16987-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="16987-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="16987-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="16987-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="16987-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="16987-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


