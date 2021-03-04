---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 7c338f49191071bfa48214e65f79e196a75650eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907342"
---
# <span data-ttu-id="b2a81-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2a81-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="b2a81-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b2a81-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a81-103">為應用程式閘道建立私人連結組</span><span class="sxs-lookup"><span data-stu-id="b2a81-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="b2a81-104">語法</span><span class="sxs-lookup"><span data-stu-id="b2a81-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2a81-105">描述</span><span class="sxs-lookup"><span data-stu-id="b2a81-105">DESCRIPTION</span></span>
<span data-ttu-id="b2a81-106">**New-AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會為 Azure 應用程式閘道建立 PrivateLink 組式。</span><span class="sxs-lookup"><span data-stu-id="b2a81-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="b2a81-107">私人連結組配置必須與前端 IP 組配置相關聯，才能啟用私人連結功能。</span><span class="sxs-lookup"><span data-stu-id="b2a81-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="b2a81-108">一個私人連結組組最可能只與應用程式閘道上的一個前端 ip 組定相關聯。</span><span class="sxs-lookup"><span data-stu-id="b2a81-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="b2a81-109">例子</span><span class="sxs-lookup"><span data-stu-id="b2a81-109">EXAMPLES</span></span>

### <span data-ttu-id="b2a81-110">範例 1：使用單一 Ip 組配置建立私人連結組</span><span class="sxs-lookup"><span data-stu-id="b2a81-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="b2a81-111">此命令會建立名為 'privateLinkConfig01' 的 PrivateLink 組$PrivateLinkConfiguration。</span><span class="sxs-lookup"><span data-stu-id="b2a81-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="b2a81-112">範例 2：使用多個 Ip 組配置的建立私人連結組</span><span class="sxs-lookup"><span data-stu-id="b2a81-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="b2a81-113">此命令會使用兩個 ipConfiguration 建立名為 'privateLinkConfig01' 的 PrivateLink 組$PrivateLinkConfiguration。</span><span class="sxs-lookup"><span data-stu-id="b2a81-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="b2a81-114">參數</span><span class="sxs-lookup"><span data-stu-id="b2a81-114">PARAMETERS</span></span>

### <span data-ttu-id="b2a81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a81-115">-DefaultProfile</span></span>
<span data-ttu-id="b2a81-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2a81-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2a81-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2a81-117">-IpConfiguration</span></span>
<span data-ttu-id="b2a81-118">ipConfiguration 清單</span><span class="sxs-lookup"><span data-stu-id="b2a81-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2a81-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2a81-119">-Name</span></span>
<span data-ttu-id="b2a81-120">privateLink 組組的名稱</span><span class="sxs-lookup"><span data-stu-id="b2a81-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="b2a81-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b2a81-121">-Confirm</span></span>
<span data-ttu-id="b2a81-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b2a81-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2a81-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2a81-123">-WhatIf</span></span>
<span data-ttu-id="b2a81-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2a81-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2a81-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2a81-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2a81-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a81-126">CommonParameters</span></span>
<span data-ttu-id="b2a81-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b2a81-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a81-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2a81-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a81-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b2a81-129">INPUTS</span></span>

### <span data-ttu-id="b2a81-130">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="b2a81-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="b2a81-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b2a81-131">OUTPUTS</span></span>

### <span data-ttu-id="b2a81-132">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2a81-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="b2a81-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b2a81-133">NOTES</span></span>

## <span data-ttu-id="b2a81-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2a81-134">RELATED LINKS</span></span>

[<span data-ttu-id="b2a81-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2a81-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b2a81-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2a81-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b2a81-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2a81-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b2a81-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2a81-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
