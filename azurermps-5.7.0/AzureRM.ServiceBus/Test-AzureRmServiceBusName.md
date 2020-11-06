---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: a35487b2eb1dae8d8af452fba9a47854ecab6efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447638"
---
# <span data-ttu-id="0bc56-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="0bc56-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="0bc56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0bc56-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc56-103">檢查 (DR 設定名稱的指定命名空間名稱或別名的可用性) </span><span class="sxs-lookup"><span data-stu-id="0bc56-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bc56-104">句法</span><span class="sxs-lookup"><span data-stu-id="0bc56-104">SYNTAX</span></span>

### <span data-ttu-id="0bc56-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0bc56-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bc56-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0bc56-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bc56-107">說明</span><span class="sxs-lookup"><span data-stu-id="0bc56-107">DESCRIPTION</span></span>
<span data-ttu-id="0bc56-108">**AzureRmServiceBusName** Cmdlet 會檢查命名空間名稱或別名 (DR 配置名稱是否可用) </span><span class="sxs-lookup"><span data-stu-id="0bc56-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="0bc56-109">示例</span><span class="sxs-lookup"><span data-stu-id="0bc56-109">EXAMPLES</span></span>

### <span data-ttu-id="0bc56-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0bc56-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="0bc56-111">將命名空間名稱 ' MyNameSapceName ' 的可用性傳回狀態傳回 True</span><span class="sxs-lookup"><span data-stu-id="0bc56-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="0bc56-112">範例2</span><span class="sxs-lookup"><span data-stu-id="0bc56-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="0bc56-113">傳回命名空間名稱 ' MyNameSapceName ' 的可用性狀態為 False，原因如下</span><span class="sxs-lookup"><span data-stu-id="0bc56-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="0bc56-114">範例3</span><span class="sxs-lookup"><span data-stu-id="0bc56-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```


## <span data-ttu-id="0bc56-115">參數</span><span class="sxs-lookup"><span data-stu-id="0bc56-115">PARAMETERS</span></span>

### <span data-ttu-id="0bc56-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="0bc56-116">-AliasName</span></span>
<span data-ttu-id="0bc56-117">DR 配置名稱-別名名稱</span><span class="sxs-lookup"><span data-stu-id="0bc56-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: Alias

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc56-118">-DefaultProfile</span></span>
<span data-ttu-id="0bc56-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0bc56-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bc56-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="0bc56-120">-Namespace</span></span>
<span data-ttu-id="0bc56-121">已將命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="0bc56-121">Servicebus Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc56-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc56-122">-ResourceGroupName</span></span>
<span data-ttu-id="0bc56-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="0bc56-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc56-124">CommonParameters</span></span>
<span data-ttu-id="0bc56-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0bc56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0bc56-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0bc56-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc56-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0bc56-127">INPUTS</span></span>

### <span data-ttu-id="0bc56-128">System.object</span><span class="sxs-lookup"><span data-stu-id="0bc56-128">System.String</span></span>


## <span data-ttu-id="0bc56-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0bc56-129">OUTPUTS</span></span>

### <span data-ttu-id="0bc56-130">[System.object]。清單 ' 1 [0.5.0.0，PSCheckNameAvailabilityResultAttributes，，版本 =，Culture = 中性，PublicKeyToken = null]」））。）</span><span class="sxs-lookup"><span data-stu-id="0bc56-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="0bc56-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0bc56-131">NOTES</span></span>

## <span data-ttu-id="0bc56-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bc56-132">RELATED LINKS</span></span>
