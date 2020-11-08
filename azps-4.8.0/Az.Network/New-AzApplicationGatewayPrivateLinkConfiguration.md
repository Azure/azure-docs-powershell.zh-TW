---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136320"
---
# <span data-ttu-id="8d1eb-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d1eb-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="8d1eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1eb-103">建立應用程式閘道的私人連結設定</span><span class="sxs-lookup"><span data-stu-id="8d1eb-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="8d1eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d1eb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d1eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d1eb-105">DESCRIPTION</span></span>
<span data-ttu-id="8d1eb-106">**新的-AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會建立 Azure 應用程式閘道的 PrivateLink 設定。</span><span class="sxs-lookup"><span data-stu-id="8d1eb-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="8d1eb-107">私人連結設定必須與前端 ip 配置相關聯，才能啟用私人連結功能。</span><span class="sxs-lookup"><span data-stu-id="8d1eb-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="8d1eb-108">您可以 atmost 單一的私人連結設定，只會與應用程式閘道上的一個前端 ip 配置相關聯。</span><span class="sxs-lookup"><span data-stu-id="8d1eb-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="8d1eb-109">示例</span><span class="sxs-lookup"><span data-stu-id="8d1eb-109">EXAMPLES</span></span>

### <span data-ttu-id="8d1eb-110">範例1：使用單一 Ip 配置建立私人連結設定</span><span class="sxs-lookup"><span data-stu-id="8d1eb-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="8d1eb-111">這個命令會建立名為 "privateLinkConfig01" 的 PrivateLink 配置，並將結果儲存在名為 $PrivateLinkConfiguration 的變數中。</span><span class="sxs-lookup"><span data-stu-id="8d1eb-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="8d1eb-112">範例2：建立具有多個 Ip 配置的私人連結設定</span><span class="sxs-lookup"><span data-stu-id="8d1eb-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="8d1eb-113">這個命令會建立一個名為「privateLinkConfig01」的 PrivateLink 配置，並將結果儲存在名為 $PrivateLinkConfiguration 的變數中。</span><span class="sxs-lookup"><span data-stu-id="8d1eb-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="8d1eb-114">參數</span><span class="sxs-lookup"><span data-stu-id="8d1eb-114">PARAMETERS</span></span>

### <span data-ttu-id="8d1eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1eb-115">-DefaultProfile</span></span>
<span data-ttu-id="8d1eb-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d1eb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d1eb-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d1eb-117">-IpConfiguration</span></span>
<span data-ttu-id="8d1eb-118">IpConfiguration 清單</span><span class="sxs-lookup"><span data-stu-id="8d1eb-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="8d1eb-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d1eb-119">-Name</span></span>
<span data-ttu-id="8d1eb-120">PrivateLink 配置的名稱</span><span class="sxs-lookup"><span data-stu-id="8d1eb-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="8d1eb-121">-確認</span><span class="sxs-lookup"><span data-stu-id="8d1eb-121">-Confirm</span></span>
<span data-ttu-id="8d1eb-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d1eb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d1eb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d1eb-123">-WhatIf</span></span>
<span data-ttu-id="8d1eb-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d1eb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d1eb-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d1eb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d1eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1eb-126">CommonParameters</span></span>
<span data-ttu-id="8d1eb-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d1eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1eb-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d1eb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1eb-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8d1eb-129">INPUTS</span></span>

### <span data-ttu-id="8d1eb-130">PSApplicationGatewayPrivateLinkIpConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8d1eb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="8d1eb-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8d1eb-131">OUTPUTS</span></span>

### <span data-ttu-id="8d1eb-132">PSApplicationGatewayPrivateLinkConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8d1eb-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="8d1eb-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8d1eb-133">NOTES</span></span>

## <span data-ttu-id="8d1eb-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d1eb-134">RELATED LINKS</span></span>

[<span data-ttu-id="8d1eb-135">AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d1eb-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="8d1eb-136">附加 AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d1eb-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="8d1eb-137">移除-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d1eb-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="8d1eb-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d1eb-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
