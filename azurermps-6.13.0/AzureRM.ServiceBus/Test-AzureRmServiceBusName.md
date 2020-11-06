---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: e7fafeeee8a377cc9bb7eb9ce514c0a0d7b89c9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448209"
---
# <span data-ttu-id="401d1-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="401d1-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="401d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="401d1-102">SYNOPSIS</span></span>
<span data-ttu-id="401d1-103">檢查 (DR 設定名稱的指定命名空間名稱或別名的可用性) </span><span class="sxs-lookup"><span data-stu-id="401d1-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="401d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="401d1-104">SYNTAX</span></span>

### <span data-ttu-id="401d1-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="401d1-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="401d1-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="401d1-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="401d1-107">說明</span><span class="sxs-lookup"><span data-stu-id="401d1-107">DESCRIPTION</span></span>
<span data-ttu-id="401d1-108">**AzureRmServiceBusName** Cmdlet 會檢查命名空間名稱或別名 (DR 配置名稱是否可用) </span><span class="sxs-lookup"><span data-stu-id="401d1-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="401d1-109">示例</span><span class="sxs-lookup"><span data-stu-id="401d1-109">EXAMPLES</span></span>

### <span data-ttu-id="401d1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="401d1-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="401d1-111">將命名空間名稱 ' MyNameSapceName ' 的可用性傳回狀態傳回 True</span><span class="sxs-lookup"><span data-stu-id="401d1-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="401d1-112">範例2</span><span class="sxs-lookup"><span data-stu-id="401d1-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="401d1-113">傳回命名空間名稱 ' MyNameSapceName ' 的可用性狀態為 False，原因如下</span><span class="sxs-lookup"><span data-stu-id="401d1-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="401d1-114">範例3</span><span class="sxs-lookup"><span data-stu-id="401d1-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="401d1-115">參數</span><span class="sxs-lookup"><span data-stu-id="401d1-115">PARAMETERS</span></span>

### <span data-ttu-id="401d1-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="401d1-116">-AliasName</span></span>
<span data-ttu-id="401d1-117">DR 配置名稱-別名名稱</span><span class="sxs-lookup"><span data-stu-id="401d1-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="401d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="401d1-118">-DefaultProfile</span></span>
<span data-ttu-id="401d1-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="401d1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="401d1-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="401d1-120">-Namespace</span></span>
<span data-ttu-id="401d1-121">已將命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="401d1-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="401d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="401d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="401d1-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="401d1-123">Resource Group Name</span></span>

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

### <span data-ttu-id="401d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="401d1-124">CommonParameters</span></span>
<span data-ttu-id="401d1-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="401d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="401d1-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="401d1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="401d1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="401d1-127">INPUTS</span></span>

### <span data-ttu-id="401d1-128">System.object</span><span class="sxs-lookup"><span data-stu-id="401d1-128">System.String</span></span>

## <span data-ttu-id="401d1-129">輸出</span><span class="sxs-lookup"><span data-stu-id="401d1-129">OUTPUTS</span></span>

### <span data-ttu-id="401d1-130">PSCheckNameAvailabilityResultAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="401d1-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="401d1-131">筆記</span><span class="sxs-lookup"><span data-stu-id="401d1-131">NOTES</span></span>

## <span data-ttu-id="401d1-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="401d1-132">RELATED LINKS</span></span>
