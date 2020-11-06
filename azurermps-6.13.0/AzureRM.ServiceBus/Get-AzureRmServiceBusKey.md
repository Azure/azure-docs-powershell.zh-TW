---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 96b95a4a6641e3bcfc2c1a18653da4231bee5c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445455"
---
# <span data-ttu-id="a243a-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="a243a-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="a243a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a243a-102">SYNOPSIS</span></span>
<span data-ttu-id="a243a-103">針對指定的命名空間或佇列或主題或 (GeoDR 設定的別名，取得) 的主要及次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="a243a-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a243a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a243a-104">SYNTAX</span></span>

### <span data-ttu-id="a243a-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a243a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a243a-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a243a-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a243a-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a243a-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a243a-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="a243a-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a243a-109">說明</span><span class="sxs-lookup"><span data-stu-id="a243a-109">DESCRIPTION</span></span>
<span data-ttu-id="a243a-110">**AzureRmServiceBusKey** Cmdlet 會針對給定的命名空間或佇列或主題或主題或別名，傳回) 的主要和次要連線字串， (GeoDR 設定。</span><span class="sxs-lookup"><span data-stu-id="a243a-110">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="a243a-111">示例</span><span class="sxs-lookup"><span data-stu-id="a243a-111">EXAMPLES</span></span>

### <span data-ttu-id="a243a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a243a-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="a243a-113">在指定命名空間中的主要和次要連線字串。</span><span class="sxs-lookup"><span data-stu-id="a243a-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="a243a-114">範例2</span><span class="sxs-lookup"><span data-stu-id="a243a-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="a243a-115">主要和次要連接字串到指定的佇列。</span><span class="sxs-lookup"><span data-stu-id="a243a-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="a243a-116">範例3</span><span class="sxs-lookup"><span data-stu-id="a243a-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="a243a-117">指定主題的主要和次要連線字串。</span><span class="sxs-lookup"><span data-stu-id="a243a-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="a243a-118">範例4</span><span class="sxs-lookup"><span data-stu-id="a243a-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="a243a-119">將主要及次要連線字串連至指定的命名空間和別名。</span><span class="sxs-lookup"><span data-stu-id="a243a-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="a243a-120">參數</span><span class="sxs-lookup"><span data-stu-id="a243a-120">PARAMETERS</span></span>

### <span data-ttu-id="a243a-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="a243a-121">-AliasName</span></span>
<span data-ttu-id="a243a-122">別名名稱</span><span class="sxs-lookup"><span data-stu-id="a243a-122">Alias Name</span></span>

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

### <span data-ttu-id="a243a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a243a-123">-DefaultProfile</span></span>
<span data-ttu-id="a243a-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a243a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a243a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a243a-125">-Name</span></span>
<span data-ttu-id="a243a-126">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="a243a-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="a243a-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a243a-127">-Namespace</span></span>
<span data-ttu-id="a243a-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="a243a-128">Namespace Name</span></span>

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

### <span data-ttu-id="a243a-129">-佇列</span><span class="sxs-lookup"><span data-stu-id="a243a-129">-Queue</span></span>
<span data-ttu-id="a243a-130">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="a243a-130">Queue Name</span></span>

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

### <span data-ttu-id="a243a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a243a-131">-ResourceGroupName</span></span>
<span data-ttu-id="a243a-132">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a243a-132">Resource Group Name</span></span>

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

### <span data-ttu-id="a243a-133">-主題</span><span class="sxs-lookup"><span data-stu-id="a243a-133">-Topic</span></span>
<span data-ttu-id="a243a-134">主題名稱</span><span class="sxs-lookup"><span data-stu-id="a243a-134">Topic Name</span></span>

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

### <span data-ttu-id="a243a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a243a-135">CommonParameters</span></span>
<span data-ttu-id="a243a-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a243a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a243a-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a243a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a243a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a243a-138">INPUTS</span></span>

### <span data-ttu-id="a243a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="a243a-139">System.String</span></span>

## <span data-ttu-id="a243a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a243a-140">OUTPUTS</span></span>

### <span data-ttu-id="a243a-141">PSListKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a243a-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="a243a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a243a-142">NOTES</span></span>

## <span data-ttu-id="a243a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a243a-143">RELATED LINKS</span></span>