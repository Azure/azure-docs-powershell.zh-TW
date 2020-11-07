---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626065"
---
# <span data-ttu-id="d97e5-101">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d97e5-101">Get-AzureRmFirewall</span></span>

## <span data-ttu-id="d97e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d97e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d97e5-103">取得 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="d97e5-103">Gets a Azure Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d97e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d97e5-104">SYNTAX</span></span>

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d97e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="d97e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d97e5-106">**AzureRmFirewall** Cmdlet 會取得資源群組中的一個或多個防火牆。</span><span class="sxs-lookup"><span data-stu-id="d97e5-106">The **Get-AzureRmFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="d97e5-107">示例</span><span class="sxs-lookup"><span data-stu-id="d97e5-107">EXAMPLES</span></span>

### <span data-ttu-id="d97e5-108">1：檢索資源群組中的所有防火牆</span><span class="sxs-lookup"><span data-stu-id="d97e5-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

<span data-ttu-id="d97e5-109">這個範例會檢索資源群組 "rgName" 中的所有防火牆。</span><span class="sxs-lookup"><span data-stu-id="d97e5-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="d97e5-110">2：依名稱檢索防火牆</span><span class="sxs-lookup"><span data-stu-id="d97e5-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

<span data-ttu-id="d97e5-111">這個範例會在資源群組 "rgName" 中，檢索名為 "azFw" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="d97e5-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="d97e5-112">3：檢索防火牆，然後將應用程式規則集合新增到防火牆</span><span class="sxs-lookup"><span data-stu-id="d97e5-112">3:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="d97e5-113">這個範例會檢索防火牆，然後透過呼叫方法 AddApplicationRuleCollection，將應用程式規則集合新增到防火牆。</span><span class="sxs-lookup"><span data-stu-id="d97e5-113">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="d97e5-114">4：檢索防火牆，然後將網路規則集合新增到防火牆</span><span class="sxs-lookup"><span data-stu-id="d97e5-114">4:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="d97e5-115">這個範例會檢索防火牆，然後透過呼叫方法 AddNetworkRuleCollection，將網路規則集合新增到防火牆。</span><span class="sxs-lookup"><span data-stu-id="d97e5-115">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="d97e5-116">5：取回防火牆，然後從防火牆以名稱來檢索應用程式規則集合</span><span class="sxs-lookup"><span data-stu-id="d97e5-116">5:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="d97e5-117">這個範例會檢索防火牆，然後依名稱取得規則集合，並在防火牆物件上呼叫方法 GetApplicationRuleCollectionByName。</span><span class="sxs-lookup"><span data-stu-id="d97e5-117">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="d97e5-118">方法 GetApplicationRuleCollectionByName 的規則集合名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d97e5-118">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="d97e5-119">6：檢索防火牆，然後從防火牆以名稱來檢索網路規則集合</span><span class="sxs-lookup"><span data-stu-id="d97e5-119">6:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="d97e5-120">這個範例會檢索防火牆，然後依名稱取得規則集合，並在防火牆物件上呼叫方法 GetNetworkRuleCollectionByName。</span><span class="sxs-lookup"><span data-stu-id="d97e5-120">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="d97e5-121">方法 GetNetworkRuleCollectionByName 的規則集合名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d97e5-121">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="d97e5-122">7：從防火牆檢索防火牆，然後依名稱移除應用程式規則集合</span><span class="sxs-lookup"><span data-stu-id="d97e5-122">7:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="d97e5-123">這個範例會檢索防火牆，然後依名稱移除規則集合，並在防火牆物件上呼叫方法 RemoveApplicationRuleCollectionByName。</span><span class="sxs-lookup"><span data-stu-id="d97e5-123">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="d97e5-124">方法 RemoveApplicationRuleCollectionByName 的規則集合名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d97e5-124">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="d97e5-125">8：檢索防火牆，然後從防火牆移除網路規則集合（依名稱）</span><span class="sxs-lookup"><span data-stu-id="d97e5-125">8:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="d97e5-126">這個範例會檢索防火牆，然後依名稱移除規則集合，並在防火牆物件上呼叫方法 RemoveNetworkRuleCollectionByName。</span><span class="sxs-lookup"><span data-stu-id="d97e5-126">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="d97e5-127">方法 RemoveNetworkRuleCollectionByName 的規則集合名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d97e5-127">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="d97e5-128">9：取回防火牆，然後再指派防火牆</span><span class="sxs-lookup"><span data-stu-id="d97e5-128">9:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="d97e5-129">這個範例會在防火牆上檢索防火牆，並在防火牆上進行呼叫，以使用與防火牆相關聯的設定 (應用程式和網路規則集合) 來啟動防火牆服務。</span><span class="sxs-lookup"><span data-stu-id="d97e5-129">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="d97e5-130">參數</span><span class="sxs-lookup"><span data-stu-id="d97e5-130">PARAMETERS</span></span>

### <span data-ttu-id="d97e5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97e5-131">-DefaultProfile</span></span>
<span data-ttu-id="d97e5-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d97e5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d97e5-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="d97e5-133">-Name</span></span>
<span data-ttu-id="d97e5-134">指定此 Cmdlet 所取得之防火牆的名稱。</span><span class="sxs-lookup"><span data-stu-id="d97e5-134">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97e5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d97e5-135">-ResourceGroupName</span></span>
<span data-ttu-id="d97e5-136">指定防火牆所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d97e5-136">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97e5-137">CommonParameters</span></span>
<span data-ttu-id="d97e5-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d97e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97e5-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d97e5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97e5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d97e5-140">INPUTS</span></span>

### <span data-ttu-id="d97e5-141">所有</span><span class="sxs-lookup"><span data-stu-id="d97e5-141">None</span></span>
<span data-ttu-id="d97e5-142">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d97e5-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d97e5-143">輸出</span><span class="sxs-lookup"><span data-stu-id="d97e5-143">OUTPUTS</span></span>

### <span data-ttu-id="d97e5-144">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d97e5-144">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="d97e5-145">筆記</span><span class="sxs-lookup"><span data-stu-id="d97e5-145">NOTES</span></span>

## <span data-ttu-id="d97e5-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="d97e5-146">RELATED LINKS</span></span>

[<span data-ttu-id="d97e5-147">新-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d97e5-147">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="d97e5-148">移除-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d97e5-148">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="d97e5-149">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d97e5-149">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
