---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625671"
---
# <span data-ttu-id="a5246-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="a5246-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="a5246-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5246-102">SYNOPSIS</span></span>
<span data-ttu-id="a5246-103">檢查指定命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="a5246-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5246-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5246-104">SYNTAX</span></span>

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## <span data-ttu-id="a5246-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5246-105">DESCRIPTION</span></span>
<span data-ttu-id="a5246-106">**Test AzureRmServiceBusName** Cmdlet 會檢查命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="a5246-106">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="a5246-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5246-107">EXAMPLES</span></span>

### <span data-ttu-id="a5246-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a5246-108">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### <span data-ttu-id="a5246-109">範例2</span><span class="sxs-lookup"><span data-stu-id="a5246-109">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### <span data-ttu-id="a5246-110">範例3</span><span class="sxs-lookup"><span data-stu-id="a5246-110">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

<span data-ttu-id="a5246-111">傳回命名空間名稱的可用性狀態</span><span class="sxs-lookup"><span data-stu-id="a5246-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="a5246-112">參數</span><span class="sxs-lookup"><span data-stu-id="a5246-112">PARAMETERS</span></span>

### <span data-ttu-id="a5246-113">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a5246-113">-Namespace</span></span>
<span data-ttu-id="a5246-114">已將命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="a5246-114">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="a5246-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5246-115">CommonParameters</span></span>
<span data-ttu-id="a5246-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5246-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5246-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a5246-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5246-118">輸入</span><span class="sxs-lookup"><span data-stu-id="a5246-118">INPUTS</span></span>

### <span data-ttu-id="a5246-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a5246-119">-Namespace</span></span>
 <span data-ttu-id="a5246-120">System.object</span><span class="sxs-lookup"><span data-stu-id="a5246-120">System.String</span></span>

## <span data-ttu-id="a5246-121">輸出</span><span class="sxs-lookup"><span data-stu-id="a5246-121">OUTPUTS</span></span>

### <span data-ttu-id="a5246-122">[CheckNameAvailabilityResultAttributes，0.1.0.0，Version =，Culture = 中性，PublicKeyToken = null）]。））。</span><span class="sxs-lookup"><span data-stu-id="a5246-122">[Microsoft.Azure.Commands.ServiceBus.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="a5246-123">範例1</span><span class="sxs-lookup"><span data-stu-id="a5246-123">Example 1</span></span>
<span data-ttu-id="a5246-124">NameAvailable 原因訊息</span><span class="sxs-lookup"><span data-stu-id="a5246-124">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="a5246-125">範例2</span><span class="sxs-lookup"><span data-stu-id="a5246-125">Example 2</span></span>
<span data-ttu-id="a5246-126">NameAvailable 原因訊息</span><span class="sxs-lookup"><span data-stu-id="a5246-126">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="a5246-127">範例3</span><span class="sxs-lookup"><span data-stu-id="a5246-127">Example 3</span></span>
<span data-ttu-id="a5246-128">NameAvailable 原因訊息</span><span class="sxs-lookup"><span data-stu-id="a5246-128">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="a5246-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a5246-129">NOTES</span></span>

## <span data-ttu-id="a5246-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5246-130">RELATED LINKS</span></span>
