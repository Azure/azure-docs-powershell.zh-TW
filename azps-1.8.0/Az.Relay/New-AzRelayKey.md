---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: b768b7838629ce25e4202ca309de8741cfa7f0de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620951"
---
# <span data-ttu-id="6b6a4-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="6b6a4-101">New-AzRelayKey</span></span>

## <span data-ttu-id="6b6a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b6a4-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6a4-103">針對指定的中繼實體， (Namespace/WcfRelay/HybridConnection 重新產生主要或次要連接字串) </span><span class="sxs-lookup"><span data-stu-id="6b6a4-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="6b6a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b6a4-104">SYNTAX</span></span>

### <span data-ttu-id="6b6a4-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6b6a4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b6a4-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b6a4-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b6a4-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b6a4-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b6a4-108">說明</span><span class="sxs-lookup"><span data-stu-id="6b6a4-108">DESCRIPTION</span></span>
<span data-ttu-id="6b6a4-109">**AzRelayKey** Cmdlet 會針對給定的中繼實體產生主要及次要連接字串， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="6b6a4-110">示例</span><span class="sxs-lookup"><span data-stu-id="6b6a4-110">EXAMPLES</span></span>

### <span data-ttu-id="6b6a4-111">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="6b6a4-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b6a4-112">針對指定的 Relay-Namespace 實體重新產生主要或次要的連接字串。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="6b6a4-113">範例 1.1-提供的命名空間 KeyValue</span><span class="sxs-lookup"><span data-stu-id="6b6a4-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b6a4-114">使用提供的索引鍵值來產生給定 Relay-Namespace 實體的主要或次要連接字串</span><span class="sxs-lookup"><span data-stu-id="6b6a4-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="6b6a4-115">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6b6a4-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b6a4-116">針對指定的 Relay-WcfRelay 實體重新產生主要或次要的連接字串。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="6b6a4-117">範例 2.1-提供 WcfRelay KeyValue</span><span class="sxs-lookup"><span data-stu-id="6b6a4-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b6a4-118">使用提供的索引鍵值來產生給定 Relay-WcfRelay 實體的主要或次要連接字串</span><span class="sxs-lookup"><span data-stu-id="6b6a4-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="6b6a4-119">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6b6a4-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b6a4-120">針對指定的中繼實體， (Namespace/WcfRelay/HybridConnection) 重新產生主要或次要的連線字串。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="6b6a4-121">範例 3.1-提供 HybridConnection KeyValue</span><span class="sxs-lookup"><span data-stu-id="6b6a4-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b6a4-122">使用提供的索引鍵值來產生給定 Relay-HybridConnection 實體的主要或次要連接字串</span><span class="sxs-lookup"><span data-stu-id="6b6a4-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="6b6a4-123">參數</span><span class="sxs-lookup"><span data-stu-id="6b6a4-123">PARAMETERS</span></span>

### <span data-ttu-id="6b6a4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6a4-124">-DefaultProfile</span></span>
<span data-ttu-id="6b6a4-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b6a4-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6b6a4-126">-HybridConnection</span></span>
<span data-ttu-id="6b6a4-127">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="6b6a4-128">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="6b6a4-128">-KeyValue</span></span>
<span data-ttu-id="6b6a4-129">用於簽署及驗證 SAS 權杖的 base64 編碼256位金鑰。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="6b6a4-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b6a4-130">-Name</span></span>
<span data-ttu-id="6b6a4-131">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6b6a4-132">-命名空間</span><span class="sxs-lookup"><span data-stu-id="6b6a4-132">-Namespace</span></span>
<span data-ttu-id="6b6a4-133">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-133">Namespace Name.</span></span>

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

### <span data-ttu-id="6b6a4-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="6b6a4-134">-RegenerateKey</span></span>
<span data-ttu-id="6b6a4-135">重新產生按鍵-"PrimaryKey"/"SecondaryKey"。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="6b6a4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b6a4-136">-ResourceGroupName</span></span>
<span data-ttu-id="6b6a4-137">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="6b6a4-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6b6a4-138">-WcfRelay</span></span>
<span data-ttu-id="6b6a4-139">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="6b6a4-140">-確認</span><span class="sxs-lookup"><span data-stu-id="6b6a4-140">-Confirm</span></span>
<span data-ttu-id="6b6a4-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b6a4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b6a4-142">-WhatIf</span></span>
<span data-ttu-id="6b6a4-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b6a4-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b6a4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6a4-145">CommonParameters</span></span>
<span data-ttu-id="6b6a4-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6a4-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6b6a4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6a4-148">輸入</span><span class="sxs-lookup"><span data-stu-id="6b6a4-148">INPUTS</span></span>

### <span data-ttu-id="6b6a4-149">System.object</span><span class="sxs-lookup"><span data-stu-id="6b6a4-149">System.String</span></span>

## <span data-ttu-id="6b6a4-150">輸出</span><span class="sxs-lookup"><span data-stu-id="6b6a4-150">OUTPUTS</span></span>

### <span data-ttu-id="6b6a4-151">PSAuthorizationRuleKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6b6a4-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="6b6a4-152">筆記</span><span class="sxs-lookup"><span data-stu-id="6b6a4-152">NOTES</span></span>

## <span data-ttu-id="6b6a4-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b6a4-153">RELATED LINKS</span></span>
