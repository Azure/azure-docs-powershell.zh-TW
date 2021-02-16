---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130782"
---
# <span data-ttu-id="530ba-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="530ba-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="530ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="530ba-102">SYNOPSIS</span></span>
<span data-ttu-id="530ba-103">針對指定的命名空間或佇列或主題或 (GeoDR 設定的別名，取得) 的主要及次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="530ba-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="530ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="530ba-104">SYNTAX</span></span>

### <span data-ttu-id="530ba-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="530ba-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="530ba-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="530ba-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="530ba-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="530ba-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="530ba-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="530ba-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="530ba-109">說明</span><span class="sxs-lookup"><span data-stu-id="530ba-109">DESCRIPTION</span></span>
<span data-ttu-id="530ba-110">**AzServiceBusKey** Cmdlet 會針對給定的命名空間或佇列或主題或主題或別名，傳回) 的主要和次要連線字串， (GeoDR 設定。</span><span class="sxs-lookup"><span data-stu-id="530ba-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="530ba-111">示例</span><span class="sxs-lookup"><span data-stu-id="530ba-111">EXAMPLES</span></span>

### <span data-ttu-id="530ba-112">範例1</span><span class="sxs-lookup"><span data-stu-id="530ba-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="530ba-113">在指定命名空間中的主要和次要連線字串。</span><span class="sxs-lookup"><span data-stu-id="530ba-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="530ba-114">範例2</span><span class="sxs-lookup"><span data-stu-id="530ba-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="530ba-115">主要和次要連接字串到指定的佇列。</span><span class="sxs-lookup"><span data-stu-id="530ba-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="530ba-116">範例3</span><span class="sxs-lookup"><span data-stu-id="530ba-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="530ba-117">指定主題的主要和次要連線字串。</span><span class="sxs-lookup"><span data-stu-id="530ba-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="530ba-118">範例4</span><span class="sxs-lookup"><span data-stu-id="530ba-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="530ba-119">將主要及次要連線字串連至指定的命名空間和別名。</span><span class="sxs-lookup"><span data-stu-id="530ba-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="530ba-120">參數</span><span class="sxs-lookup"><span data-stu-id="530ba-120">PARAMETERS</span></span>

### <span data-ttu-id="530ba-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="530ba-121">-AliasName</span></span>
<span data-ttu-id="530ba-122">別名名稱</span><span class="sxs-lookup"><span data-stu-id="530ba-122">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="530ba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="530ba-123">-DefaultProfile</span></span>
<span data-ttu-id="530ba-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="530ba-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="530ba-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="530ba-125">-Name</span></span>
<span data-ttu-id="530ba-126">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="530ba-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="530ba-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="530ba-127">-Namespace</span></span>
<span data-ttu-id="530ba-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="530ba-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="530ba-129">-佇列</span><span class="sxs-lookup"><span data-stu-id="530ba-129">-Queue</span></span>
<span data-ttu-id="530ba-130">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="530ba-130">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="530ba-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="530ba-131">-ResourceGroupName</span></span>
<span data-ttu-id="530ba-132">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="530ba-132">Resource Group Name</span></span>

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

### <span data-ttu-id="530ba-133">-主題</span><span class="sxs-lookup"><span data-stu-id="530ba-133">-Topic</span></span>
<span data-ttu-id="530ba-134">主題名稱</span><span class="sxs-lookup"><span data-stu-id="530ba-134">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="530ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="530ba-135">CommonParameters</span></span>
<span data-ttu-id="530ba-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="530ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="530ba-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="530ba-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="530ba-138">輸入</span><span class="sxs-lookup"><span data-stu-id="530ba-138">INPUTS</span></span>

### <span data-ttu-id="530ba-139">System.object</span><span class="sxs-lookup"><span data-stu-id="530ba-139">System.String</span></span>

## <span data-ttu-id="530ba-140">輸出</span><span class="sxs-lookup"><span data-stu-id="530ba-140">OUTPUTS</span></span>

### <span data-ttu-id="530ba-141">PSListKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="530ba-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="530ba-142">筆記</span><span class="sxs-lookup"><span data-stu-id="530ba-142">NOTES</span></span>

## <span data-ttu-id="530ba-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="530ba-143">RELATED LINKS</span></span>
