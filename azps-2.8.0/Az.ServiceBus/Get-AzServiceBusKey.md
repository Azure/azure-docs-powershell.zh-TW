---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: c9d6e262acd20616cf070ab061b48a61ccfbba48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792128"
---
# <span data-ttu-id="f75a0-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="f75a0-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="f75a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f75a0-102">SYNOPSIS</span></span>
<span data-ttu-id="f75a0-103">針對指定的命名空間或佇列或主題或 (GeoDR 設定的別名，取得) 的主要及次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="f75a0-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="f75a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="f75a0-104">SYNTAX</span></span>

### <span data-ttu-id="f75a0-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f75a0-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f75a0-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f75a0-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f75a0-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f75a0-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f75a0-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="f75a0-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f75a0-109">說明</span><span class="sxs-lookup"><span data-stu-id="f75a0-109">DESCRIPTION</span></span>
<span data-ttu-id="f75a0-110">**AzServiceBusKey** Cmdlet 會針對給定的命名空間或佇列或主題或主題或別名，傳回) 的主要和次要連線字串， (GeoDR 設定。</span><span class="sxs-lookup"><span data-stu-id="f75a0-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="f75a0-111">示例</span><span class="sxs-lookup"><span data-stu-id="f75a0-111">EXAMPLES</span></span>

### <span data-ttu-id="f75a0-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f75a0-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="f75a0-113">在指定命名空間中的主要和次要連線字串。</span><span class="sxs-lookup"><span data-stu-id="f75a0-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="f75a0-114">範例2</span><span class="sxs-lookup"><span data-stu-id="f75a0-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="f75a0-115">主要和次要連接字串到指定的佇列。</span><span class="sxs-lookup"><span data-stu-id="f75a0-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="f75a0-116">範例3</span><span class="sxs-lookup"><span data-stu-id="f75a0-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="f75a0-117">指定主題的主要和次要連線字串。</span><span class="sxs-lookup"><span data-stu-id="f75a0-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="f75a0-118">範例4</span><span class="sxs-lookup"><span data-stu-id="f75a0-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="f75a0-119">將主要及次要連線字串連至指定的命名空間和別名。</span><span class="sxs-lookup"><span data-stu-id="f75a0-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="f75a0-120">參數</span><span class="sxs-lookup"><span data-stu-id="f75a0-120">PARAMETERS</span></span>

### <span data-ttu-id="f75a0-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="f75a0-121">-AliasName</span></span>
<span data-ttu-id="f75a0-122">別名名稱</span><span class="sxs-lookup"><span data-stu-id="f75a0-122">Alias Name</span></span>

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

### <span data-ttu-id="f75a0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75a0-123">-DefaultProfile</span></span>
<span data-ttu-id="f75a0-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f75a0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f75a0-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f75a0-125">-Name</span></span>
<span data-ttu-id="f75a0-126">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="f75a0-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f75a0-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f75a0-127">-Namespace</span></span>
<span data-ttu-id="f75a0-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f75a0-128">Namespace Name</span></span>

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

### <span data-ttu-id="f75a0-129">-佇列</span><span class="sxs-lookup"><span data-stu-id="f75a0-129">-Queue</span></span>
<span data-ttu-id="f75a0-130">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="f75a0-130">Queue Name</span></span>

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

### <span data-ttu-id="f75a0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f75a0-131">-ResourceGroupName</span></span>
<span data-ttu-id="f75a0-132">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f75a0-132">Resource Group Name</span></span>

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

### <span data-ttu-id="f75a0-133">-主題</span><span class="sxs-lookup"><span data-stu-id="f75a0-133">-Topic</span></span>
<span data-ttu-id="f75a0-134">主題名稱</span><span class="sxs-lookup"><span data-stu-id="f75a0-134">Topic Name</span></span>

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

### <span data-ttu-id="f75a0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75a0-135">CommonParameters</span></span>
<span data-ttu-id="f75a0-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f75a0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75a0-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f75a0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75a0-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f75a0-138">INPUTS</span></span>

### <span data-ttu-id="f75a0-139">System.object</span><span class="sxs-lookup"><span data-stu-id="f75a0-139">System.String</span></span>

## <span data-ttu-id="f75a0-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f75a0-140">OUTPUTS</span></span>

### <span data-ttu-id="f75a0-141">PSListKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f75a0-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="f75a0-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f75a0-142">NOTES</span></span>

## <span data-ttu-id="f75a0-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f75a0-143">RELATED LINKS</span></span>
