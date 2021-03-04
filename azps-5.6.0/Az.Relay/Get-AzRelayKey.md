---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: ca477e278ef28cd2fce17578d55782f3ab610954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914610"
---
# <span data-ttu-id="3e592-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="3e592-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="3e592-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3e592-102">SYNOPSIS</span></span>
<span data-ttu-id="3e592-103">在命名空間/WcfRelay/HybridConnection (中，獲得所給轉會實體的主要和次要) 。</span><span class="sxs-lookup"><span data-stu-id="3e592-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3e592-104">語法</span><span class="sxs-lookup"><span data-stu-id="3e592-104">SYNTAX</span></span>

### <span data-ttu-id="3e592-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3e592-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e592-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e592-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e592-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e592-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e592-108">描述</span><span class="sxs-lookup"><span data-stu-id="3e592-108">DESCRIPTION</span></span>
<span data-ttu-id="3e592-109">**Get-AzRelayKey** Cmdlet 會傳回給定轉場實體 (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="3e592-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3e592-110">例子</span><span class="sxs-lookup"><span data-stu-id="3e592-110">EXAMPLES</span></span>

### <span data-ttu-id="3e592-111">範例 1：命名空間</span><span class="sxs-lookup"><span data-stu-id="3e592-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="3e592-112">範例 2：WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3e592-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="3e592-113">範例 3：HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3e592-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="3e592-114">到指定的 Relay 實體的主要和次要連接字串 (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="3e592-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3e592-115">參數</span><span class="sxs-lookup"><span data-stu-id="3e592-115">PARAMETERS</span></span>

### <span data-ttu-id="3e592-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e592-116">-DefaultProfile</span></span>
<span data-ttu-id="3e592-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e592-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e592-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3e592-118">-HybridConnection</span></span>
<span data-ttu-id="3e592-119">HybridConnection 名稱。</span><span class="sxs-lookup"><span data-stu-id="3e592-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="3e592-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e592-120">-Name</span></span>
<span data-ttu-id="3e592-121">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="3e592-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="3e592-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="3e592-122">-Namespace</span></span>
<span data-ttu-id="3e592-123">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="3e592-123">Namespace Name.</span></span>

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

### <span data-ttu-id="3e592-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e592-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e592-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3e592-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="3e592-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3e592-126">-WcfRelay</span></span>
<span data-ttu-id="3e592-127">WcfRelay 名稱。</span><span class="sxs-lookup"><span data-stu-id="3e592-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="3e592-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e592-128">CommonParameters</span></span>
<span data-ttu-id="3e592-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3e592-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e592-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3e592-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e592-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3e592-131">INPUTS</span></span>

### <span data-ttu-id="3e592-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3e592-132">System.String</span></span>

## <span data-ttu-id="3e592-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3e592-133">OUTPUTS</span></span>

### <span data-ttu-id="3e592-134">Microsoft.Azure.Commands.Relay.models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="3e592-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="3e592-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3e592-135">NOTES</span></span>

## <span data-ttu-id="3e592-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e592-136">RELATED LINKS</span></span>
