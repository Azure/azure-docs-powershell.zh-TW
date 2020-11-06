---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 68ba115bb74bf0eae780944037532b0d37424704
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620967"
---
# <span data-ttu-id="7f7fe-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="7f7fe-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="7f7fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7fe-103">取得指定之中繼實體的主要及次要連線字串 (Namespace/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="7f7fe-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="7f7fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f7fe-104">SYNTAX</span></span>

### <span data-ttu-id="7f7fe-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7f7fe-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f7fe-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f7fe-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f7fe-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f7fe-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f7fe-108">說明</span><span class="sxs-lookup"><span data-stu-id="7f7fe-108">DESCRIPTION</span></span>
<span data-ttu-id="7f7fe-109">**AzRelayKey** Cmdlet 會傳回指定的中繼實體的主要及次要連線字串， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="7f7fe-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="7f7fe-110">示例</span><span class="sxs-lookup"><span data-stu-id="7f7fe-110">EXAMPLES</span></span>

### <span data-ttu-id="7f7fe-111">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="7f7fe-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="7f7fe-112">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7f7fe-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="7f7fe-113">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="7f7fe-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="7f7fe-114">針對指定的中繼實體的主要及次要連線字串 (Namespace/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="7f7fe-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="7f7fe-115">參數</span><span class="sxs-lookup"><span data-stu-id="7f7fe-115">PARAMETERS</span></span>

### <span data-ttu-id="7f7fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7fe-116">-DefaultProfile</span></span>
<span data-ttu-id="7f7fe-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f7fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f7fe-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="7f7fe-118">-HybridConnection</span></span>
<span data-ttu-id="7f7fe-119">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="7f7fe-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="7f7fe-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f7fe-120">-Name</span></span>
<span data-ttu-id="7f7fe-121">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="7f7fe-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7f7fe-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7f7fe-122">-Namespace</span></span>
<span data-ttu-id="7f7fe-123">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="7f7fe-123">Namespace Name.</span></span>

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

### <span data-ttu-id="7f7fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f7fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="7f7fe-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7f7fe-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="7f7fe-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7f7fe-126">-WcfRelay</span></span>
<span data-ttu-id="7f7fe-127">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="7f7fe-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="7f7fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7fe-128">CommonParameters</span></span>
<span data-ttu-id="7f7fe-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f7fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7fe-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f7fe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7fe-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7f7fe-131">INPUTS</span></span>

### <span data-ttu-id="7f7fe-132">System.object</span><span class="sxs-lookup"><span data-stu-id="7f7fe-132">System.String</span></span>

## <span data-ttu-id="7f7fe-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7f7fe-133">OUTPUTS</span></span>

### <span data-ttu-id="7f7fe-134">PSAuthorizationRuleKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7f7fe-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="7f7fe-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7f7fe-135">NOTES</span></span>

## <span data-ttu-id="7f7fe-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f7fe-136">RELATED LINKS</span></span>
