---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: 078f8ec492e5cda6aea5c059f3b8493197ad358c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914585"
---
# <span data-ttu-id="3d4eb-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="3d4eb-101">New-AzRelayKey</span></span>

## <span data-ttu-id="3d4eb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3d4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4eb-103">重新產生命名空間/WcfRelay/HybridConnection (之給定轉場實體的主要或次要) </span><span class="sxs-lookup"><span data-stu-id="3d4eb-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="3d4eb-104">語法</span><span class="sxs-lookup"><span data-stu-id="3d4eb-104">SYNTAX</span></span>

### <span data-ttu-id="3d4eb-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3d4eb-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d4eb-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d4eb-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d4eb-108">描述</span><span class="sxs-lookup"><span data-stu-id="3d4eb-108">DESCRIPTION</span></span>
<span data-ttu-id="3d4eb-109">**New-AzRelayKey** Cmdlet 會為給定轉場實體產生主要和次要連接字串 (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3d4eb-110">例子</span><span class="sxs-lookup"><span data-stu-id="3d4eb-110">EXAMPLES</span></span>

### <span data-ttu-id="3d4eb-111">範例 1 - 命名空間</span><span class="sxs-lookup"><span data-stu-id="3d4eb-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="3d4eb-112">為給定實體重新產生主要或次要Relay-Namespace字串。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="3d4eb-113">範例 1.1 - 提供的命名空間 KeyValue</span><span class="sxs-lookup"><span data-stu-id="3d4eb-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="3d4eb-114">產生提供 Key Value 之Relay-Namespace實體的主要或次要連接字串</span><span class="sxs-lookup"><span data-stu-id="3d4eb-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="3d4eb-115">範例 2 - WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3d4eb-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="3d4eb-116">為給定實體重新產生主要或次要Relay-WcfRelay字串。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="3d4eb-117">範例 2.1 - 提供 WcfRelay KeyValue</span><span class="sxs-lookup"><span data-stu-id="3d4eb-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="3d4eb-118">產生提供 Key Value 之Relay-WcfRelay實體的主要或次要連接字串</span><span class="sxs-lookup"><span data-stu-id="3d4eb-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="3d4eb-119">範例 3 - HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3d4eb-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="3d4eb-120">重新產生命名空間/WcfRelay/HybridConnection (之給定轉場實體的主要或次要) 。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="3d4eb-121">範例 3.1 - 提供 HybridConnection KeyValue</span><span class="sxs-lookup"><span data-stu-id="3d4eb-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="3d4eb-122">產生提供 Key Value 之Relay-HybridConnection實體的主要或次要連接字串</span><span class="sxs-lookup"><span data-stu-id="3d4eb-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="3d4eb-123">參數</span><span class="sxs-lookup"><span data-stu-id="3d4eb-123">PARAMETERS</span></span>

### <span data-ttu-id="3d4eb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4eb-124">-DefaultProfile</span></span>
<span data-ttu-id="3d4eb-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d4eb-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3d4eb-126">-HybridConnection</span></span>
<span data-ttu-id="3d4eb-127">HybridConnection 名稱。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="3d4eb-128">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="3d4eb-128">-KeyValue</span></span>
<span data-ttu-id="3d4eb-129">用於簽署及驗證 SAS 權杖的 256 位基本編碼金鑰。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d4eb-130">-Name</span></span>
<span data-ttu-id="3d4eb-131">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="3d4eb-132">-命名空間</span><span class="sxs-lookup"><span data-stu-id="3d4eb-132">-Namespace</span></span>
<span data-ttu-id="3d4eb-133">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-133">Namespace Name.</span></span>

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

### <span data-ttu-id="3d4eb-134">-重新產生金鑰</span><span class="sxs-lookup"><span data-stu-id="3d4eb-134">-RegenerateKey</span></span>
<span data-ttu-id="3d4eb-135">重新產生金鑰 - 'PrimaryKey'/'SecondaryKey'。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d4eb-136">-ResourceGroupName</span></span>
<span data-ttu-id="3d4eb-137">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d4eb-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3d4eb-138">-WcfRelay</span></span>
<span data-ttu-id="3d4eb-139">WcfRelay 名稱。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="3d4eb-140">-確認</span><span class="sxs-lookup"><span data-stu-id="3d4eb-140">-Confirm</span></span>
<span data-ttu-id="3d4eb-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d4eb-142">-WhatIf</span></span>
<span data-ttu-id="3d4eb-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d4eb-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4eb-145">CommonParameters</span></span>
<span data-ttu-id="3d4eb-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4eb-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3d4eb-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4eb-148">輸入</span><span class="sxs-lookup"><span data-stu-id="3d4eb-148">INPUTS</span></span>

### <span data-ttu-id="3d4eb-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3d4eb-149">System.String</span></span>

## <span data-ttu-id="3d4eb-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3d4eb-150">OUTPUTS</span></span>

### <span data-ttu-id="3d4eb-151">Microsoft.Azure.Commands.Relay.models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="3d4eb-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="3d4eb-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3d4eb-152">NOTES</span></span>

## <span data-ttu-id="3d4eb-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d4eb-153">RELATED LINKS</span></span>
