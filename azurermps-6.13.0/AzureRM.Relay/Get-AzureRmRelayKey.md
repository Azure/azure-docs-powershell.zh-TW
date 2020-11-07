---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 69f6b1bc50681bafe7a860dcebaa7616c8f14e90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626361"
---
# <span data-ttu-id="c53f6-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="c53f6-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="c53f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c53f6-102">SYNOPSIS</span></span>
<span data-ttu-id="c53f6-103">取得指定之中繼實體的主要及次要連線字串 (Namespace/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="c53f6-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c53f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c53f6-104">SYNTAX</span></span>

### <span data-ttu-id="c53f6-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c53f6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c53f6-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c53f6-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c53f6-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c53f6-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c53f6-108">說明</span><span class="sxs-lookup"><span data-stu-id="c53f6-108">DESCRIPTION</span></span>
<span data-ttu-id="c53f6-109">**AzureRmRelayKey** Cmdlet 會傳回指定的中繼實體的主要及次要連線字串， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="c53f6-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="c53f6-110">示例</span><span class="sxs-lookup"><span data-stu-id="c53f6-110">EXAMPLES</span></span>

### <span data-ttu-id="c53f6-111">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="c53f6-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="c53f6-112">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c53f6-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="c53f6-113">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c53f6-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="c53f6-114">針對指定的中繼實體的主要及次要連線字串 (Namespace/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="c53f6-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="c53f6-115">參數</span><span class="sxs-lookup"><span data-stu-id="c53f6-115">PARAMETERS</span></span>

### <span data-ttu-id="c53f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c53f6-116">-DefaultProfile</span></span>
<span data-ttu-id="c53f6-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c53f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c53f6-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c53f6-118">-HybridConnection</span></span>
<span data-ttu-id="c53f6-119">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="c53f6-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="c53f6-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c53f6-120">-Name</span></span>
<span data-ttu-id="c53f6-121">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="c53f6-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="c53f6-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="c53f6-122">-Namespace</span></span>
<span data-ttu-id="c53f6-123">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="c53f6-123">Namespace Name.</span></span>

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

### <span data-ttu-id="c53f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c53f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="c53f6-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c53f6-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c53f6-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c53f6-126">-WcfRelay</span></span>
<span data-ttu-id="c53f6-127">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="c53f6-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="c53f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c53f6-128">CommonParameters</span></span>
<span data-ttu-id="c53f6-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c53f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c53f6-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c53f6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c53f6-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c53f6-131">INPUTS</span></span>

### <span data-ttu-id="c53f6-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c53f6-132">System.String</span></span>


## <span data-ttu-id="c53f6-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c53f6-133">OUTPUTS</span></span>

### <span data-ttu-id="c53f6-134">PSAuthorizationRuleKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c53f6-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>


## <span data-ttu-id="c53f6-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c53f6-135">NOTES</span></span>

## <span data-ttu-id="c53f6-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c53f6-136">RELATED LINKS</span></span>
