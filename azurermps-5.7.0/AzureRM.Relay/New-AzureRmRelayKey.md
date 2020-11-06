---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 050d6477a25922236dc2d9d2e28db1228f4666fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453084"
---
# <span data-ttu-id="1beed-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="1beed-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="1beed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1beed-102">SYNOPSIS</span></span>
<span data-ttu-id="1beed-103">針對指定的中繼實體， (Namespace/WcfRelay/HybridConnection 重新產生主要或次要連接字串) </span><span class="sxs-lookup"><span data-stu-id="1beed-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1beed-104">句法</span><span class="sxs-lookup"><span data-stu-id="1beed-104">SYNTAX</span></span>

### <span data-ttu-id="1beed-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1beed-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1beed-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1beed-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1beed-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1beed-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1beed-108">說明</span><span class="sxs-lookup"><span data-stu-id="1beed-108">DESCRIPTION</span></span>
<span data-ttu-id="1beed-109">**AzureRmRelayKey** Cmdlet 會針對給定的中繼實體產生主要及次要連接字串， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="1beed-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1beed-110">示例</span><span class="sxs-lookup"><span data-stu-id="1beed-110">EXAMPLES</span></span>

### <span data-ttu-id="1beed-111">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="1beed-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="1beed-112">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1beed-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="1beed-113">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1beed-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="1beed-114">針對指定的中繼實體， (Namespace/WcfRelay/HybridConnection) 重新產生主要或次要的連線字串。</span><span class="sxs-lookup"><span data-stu-id="1beed-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1beed-115">參數</span><span class="sxs-lookup"><span data-stu-id="1beed-115">PARAMETERS</span></span>

### <span data-ttu-id="1beed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1beed-116">-DefaultProfile</span></span>
<span data-ttu-id="1beed-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1beed-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1beed-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1beed-118">-HybridConnection</span></span>
<span data-ttu-id="1beed-119">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="1beed-119">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1beed-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1beed-120">-Name</span></span>
<span data-ttu-id="1beed-121">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="1beed-121">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1beed-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="1beed-122">-Namespace</span></span>
<span data-ttu-id="1beed-123">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="1beed-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1beed-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="1beed-124">-RegenerateKey</span></span>
<span data-ttu-id="1beed-125">重新產生按鍵-"PrimaryKey"/"SecondaryKey"。</span><span class="sxs-lookup"><span data-stu-id="1beed-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1beed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1beed-126">-ResourceGroupName</span></span>
<span data-ttu-id="1beed-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1beed-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1beed-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1beed-128">-WcfRelay</span></span>
<span data-ttu-id="1beed-129">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="1beed-129">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1beed-130">-確認</span><span class="sxs-lookup"><span data-stu-id="1beed-130">-Confirm</span></span>
<span data-ttu-id="1beed-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1beed-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1beed-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1beed-132">-WhatIf</span></span>
<span data-ttu-id="1beed-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1beed-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1beed-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1beed-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1beed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1beed-135">CommonParameters</span></span>
<span data-ttu-id="1beed-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1beed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1beed-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1beed-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1beed-138">輸入</span><span class="sxs-lookup"><span data-stu-id="1beed-138">INPUTS</span></span>

### <span data-ttu-id="1beed-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="1beed-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="1beed-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1beed-140">System.String</span></span> 

### <span data-ttu-id="1beed-141">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1beed-141">-NamespaceName</span></span>
 <span data-ttu-id="1beed-142">System.object</span><span class="sxs-lookup"><span data-stu-id="1beed-142">System.String</span></span> 
 

### <span data-ttu-id="1beed-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="1beed-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="1beed-144">System.object</span><span class="sxs-lookup"><span data-stu-id="1beed-144">System.String</span></span> 

### <span data-ttu-id="1beed-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="1beed-145">-WcfRelayName</span></span>
 <span data-ttu-id="1beed-146">System.object</span><span class="sxs-lookup"><span data-stu-id="1beed-146">System.String</span></span> 

### <span data-ttu-id="1beed-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="1beed-147">-Name</span></span>
 <span data-ttu-id="1beed-148">System.object</span><span class="sxs-lookup"><span data-stu-id="1beed-148">System.String</span></span>

### <span data-ttu-id="1beed-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="1beed-149">-RegenerateKeys</span></span>
 <span data-ttu-id="1beed-150">System.object</span><span class="sxs-lookup"><span data-stu-id="1beed-150">System.String</span></span>

## <span data-ttu-id="1beed-151">輸出</span><span class="sxs-lookup"><span data-stu-id="1beed-151">OUTPUTS</span></span>

### <span data-ttu-id="1beed-152">AuthorizationRuleKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1beed-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="1beed-153">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="1beed-153">Example 1 - Namespace</span></span>
<span data-ttu-id="1beed-154">PrimaryConnectionString： Endpoint = sb：//testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #： AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="1beed-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="1beed-155">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1beed-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="1beed-156">PrimaryConnectionString： Endpoint = sb：//testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #EntityPath = TestWCFRelay1 SecondaryConnectionString： Endpoint = sb：//testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #EntityPath = TestWCFRelay1 PrimaryKey： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # 的 SecondaryKey： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #： AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="1beed-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="1beed-157">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1beed-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="1beed-158">PrimaryConnectionString： Endpoint = sb：//testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #EntityPath = TestHybridConnection SecondaryConnectionString： Endpoint = sb：//testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #EntityPath = TestHybridConnection PrimaryKey： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # 的 SecondaryKey： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #： AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="1beed-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="1beed-159">筆記</span><span class="sxs-lookup"><span data-stu-id="1beed-159">NOTES</span></span>

## <span data-ttu-id="1beed-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="1beed-160">RELATED LINKS</span></span>

