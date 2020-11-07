---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 44e1571dbd6da015e163a69716f06d3ed3cebde5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623861"
---
# <span data-ttu-id="286b5-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="286b5-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="286b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="286b5-102">SYNOPSIS</span></span>
<span data-ttu-id="286b5-103">取得指定之中繼實體的主要及次要連線字串 (Namespace/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="286b5-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="286b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="286b5-104">SYNTAX</span></span>

### <span data-ttu-id="286b5-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="286b5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="286b5-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="286b5-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="286b5-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="286b5-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="286b5-108">說明</span><span class="sxs-lookup"><span data-stu-id="286b5-108">DESCRIPTION</span></span>
<span data-ttu-id="286b5-109">**AzureRmRelayKey** Cmdlet 會傳回指定的中繼實體的主要及次要連線字串， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="286b5-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="286b5-110">示例</span><span class="sxs-lookup"><span data-stu-id="286b5-110">EXAMPLES</span></span>

### <span data-ttu-id="286b5-111">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="286b5-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### <span data-ttu-id="286b5-112">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="286b5-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### <span data-ttu-id="286b5-113">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="286b5-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="286b5-114">針對指定的中繼實體的主要及次要連線字串 (Namespace/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="286b5-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="286b5-115">參數</span><span class="sxs-lookup"><span data-stu-id="286b5-115">PARAMETERS</span></span>

### <span data-ttu-id="286b5-116">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="286b5-116">-HybridConnection</span></span>
<span data-ttu-id="286b5-117">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="286b5-117">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="286b5-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="286b5-118">-Name</span></span>
<span data-ttu-id="286b5-119">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="286b5-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="286b5-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="286b5-120">-Namespace</span></span>
<span data-ttu-id="286b5-121">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="286b5-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="286b5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286b5-122">-ResourceGroupName</span></span>
<span data-ttu-id="286b5-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="286b5-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="286b5-124">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="286b5-124">-WcfRelay</span></span>
<span data-ttu-id="286b5-125">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="286b5-125">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="286b5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286b5-126">-DefaultProfile</span></span>
<span data-ttu-id="286b5-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="286b5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286b5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286b5-128">CommonParameters</span></span>
<span data-ttu-id="286b5-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="286b5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286b5-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="286b5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286b5-131">輸入</span><span class="sxs-lookup"><span data-stu-id="286b5-131">INPUTS</span></span>

### <span data-ttu-id="286b5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286b5-132">-ResourceGroupName</span></span>
 <span data-ttu-id="286b5-133">System.object</span><span class="sxs-lookup"><span data-stu-id="286b5-133">System.String</span></span> 

### <span data-ttu-id="286b5-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="286b5-134">-NamespaceName</span></span>
 <span data-ttu-id="286b5-135">System.object</span><span class="sxs-lookup"><span data-stu-id="286b5-135">System.String</span></span> 
 

### <span data-ttu-id="286b5-136">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="286b5-136">-HybridConnectionsName</span></span>
 <span data-ttu-id="286b5-137">System.object</span><span class="sxs-lookup"><span data-stu-id="286b5-137">System.String</span></span> 

### <span data-ttu-id="286b5-138">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="286b5-138">-WcfRelayName</span></span>
 <span data-ttu-id="286b5-139">System.object</span><span class="sxs-lookup"><span data-stu-id="286b5-139">System.String</span></span> 

### <span data-ttu-id="286b5-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="286b5-140">-Name</span></span>
 <span data-ttu-id="286b5-141">System.object</span><span class="sxs-lookup"><span data-stu-id="286b5-141">System.String</span></span>

## <span data-ttu-id="286b5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="286b5-142">OUTPUTS</span></span>

### <span data-ttu-id="286b5-143">AuthorizationRuleKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="286b5-143">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="286b5-144">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="286b5-144">Example 1 - Namespace</span></span>
<span data-ttu-id="286b5-145">PrimaryConnectionString： Endpoint = sb：//testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #： AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="286b5-145">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="286b5-146">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="286b5-146">Example 2 - WcfRelay</span></span>
<span data-ttu-id="286b5-147">PrimaryConnectionString： Endpoint = sb：//testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #EntityPath = TestWCFRelay1 SecondaryConnectionString： Endpoint = sb：//testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #EntityPath = TestWCFRelay1 PrimaryKey： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # 的 SecondaryKey： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #： AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="286b5-147">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="286b5-148">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="286b5-148">Example 3 - HybridConnection</span></span>
<span data-ttu-id="286b5-149">PrimaryConnectionString： Endpoint = sb：//testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #EntityPath = TestHybridConnection SecondaryConnectionString： Endpoint = sb：//testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #EntityPath = TestHybridConnection PrimaryKey： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # 的 SecondaryKey： # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #： AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="286b5-149">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="286b5-150">筆記</span><span class="sxs-lookup"><span data-stu-id="286b5-150">NOTES</span></span>

## <span data-ttu-id="286b5-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="286b5-151">RELATED LINKS</span></span>

