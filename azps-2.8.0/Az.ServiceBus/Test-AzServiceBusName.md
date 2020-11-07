---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: 0c094fbc294ac6ca5370f8d82c8ebfceac74af0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792090"
---
# <span data-ttu-id="8f827-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="8f827-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="8f827-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f827-102">SYNOPSIS</span></span>
<span data-ttu-id="8f827-103">檢查 (DR 設定名稱的指定命名空間名稱或別名的可用性) </span><span class="sxs-lookup"><span data-stu-id="8f827-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="8f827-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f827-104">SYNTAX</span></span>

### <span data-ttu-id="8f827-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8f827-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f827-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8f827-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f827-107">說明</span><span class="sxs-lookup"><span data-stu-id="8f827-107">DESCRIPTION</span></span>
<span data-ttu-id="8f827-108">**AzServiceBusName** Cmdlet 會檢查命名空間名稱或別名 (DR 配置名稱是否可用) </span><span class="sxs-lookup"><span data-stu-id="8f827-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="8f827-109">示例</span><span class="sxs-lookup"><span data-stu-id="8f827-109">EXAMPLES</span></span>

### <span data-ttu-id="8f827-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8f827-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="8f827-111">將命名空間名稱 ' MyNameSapceName ' 的可用性傳回狀態傳回 True</span><span class="sxs-lookup"><span data-stu-id="8f827-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="8f827-112">範例2</span><span class="sxs-lookup"><span data-stu-id="8f827-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="8f827-113">傳回命名空間名稱 ' MyNameSapceName ' 的可用性狀態為 False，原因如下</span><span class="sxs-lookup"><span data-stu-id="8f827-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="8f827-114">範例3</span><span class="sxs-lookup"><span data-stu-id="8f827-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="8f827-115">參數</span><span class="sxs-lookup"><span data-stu-id="8f827-115">PARAMETERS</span></span>

### <span data-ttu-id="8f827-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="8f827-116">-AliasName</span></span>
<span data-ttu-id="8f827-117">DR 配置名稱-別名名稱</span><span class="sxs-lookup"><span data-stu-id="8f827-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f827-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f827-118">-DefaultProfile</span></span>
<span data-ttu-id="8f827-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f827-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f827-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="8f827-120">-Namespace</span></span>
<span data-ttu-id="8f827-121">已將命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="8f827-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f827-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f827-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f827-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="8f827-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f827-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f827-124">CommonParameters</span></span>
<span data-ttu-id="8f827-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f827-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f827-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f827-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f827-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8f827-127">INPUTS</span></span>

### <span data-ttu-id="8f827-128">System.object</span><span class="sxs-lookup"><span data-stu-id="8f827-128">System.String</span></span>

## <span data-ttu-id="8f827-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8f827-129">OUTPUTS</span></span>

### <span data-ttu-id="8f827-130">PSCheckNameAvailabilityResultAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8f827-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="8f827-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8f827-131">NOTES</span></span>

## <span data-ttu-id="8f827-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f827-132">RELATED LINKS</span></span>