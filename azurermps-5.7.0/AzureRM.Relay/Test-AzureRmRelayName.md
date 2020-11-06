---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450523"
---
# <span data-ttu-id="84954-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="84954-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="84954-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84954-102">SYNOPSIS</span></span>
<span data-ttu-id="84954-103">檢查指定命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="84954-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84954-104">句法</span><span class="sxs-lookup"><span data-stu-id="84954-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84954-105">說明</span><span class="sxs-lookup"><span data-stu-id="84954-105">DESCRIPTION</span></span>
<span data-ttu-id="84954-106">**Test AzureRmRelayName** Cmdlet 會檢查命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="84954-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="84954-107">示例</span><span class="sxs-lookup"><span data-stu-id="84954-107">EXAMPLES</span></span>

### <span data-ttu-id="84954-108">範例1</span><span class="sxs-lookup"><span data-stu-id="84954-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="84954-109">範例2</span><span class="sxs-lookup"><span data-stu-id="84954-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="84954-110">範例3</span><span class="sxs-lookup"><span data-stu-id="84954-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="84954-111">傳回命名空間名稱的可用性狀態</span><span class="sxs-lookup"><span data-stu-id="84954-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="84954-112">參數</span><span class="sxs-lookup"><span data-stu-id="84954-112">PARAMETERS</span></span>

### <span data-ttu-id="84954-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84954-113">-DefaultProfile</span></span>
<span data-ttu-id="84954-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84954-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84954-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="84954-115">-Namespace</span></span>
<span data-ttu-id="84954-116">中繼命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="84954-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="84954-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84954-117">CommonParameters</span></span>
<span data-ttu-id="84954-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84954-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84954-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="84954-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84954-120">輸入</span><span class="sxs-lookup"><span data-stu-id="84954-120">INPUTS</span></span>

### <span data-ttu-id="84954-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="84954-121">-Namespace</span></span>
 <span data-ttu-id="84954-122">System.object</span><span class="sxs-lookup"><span data-stu-id="84954-122">System.String</span></span>

## <span data-ttu-id="84954-123">輸出</span><span class="sxs-lookup"><span data-stu-id="84954-123">OUTPUTS</span></span>

### <span data-ttu-id="84954-124">[CheckNameAvailabilityResultAttributes、0.1.0.0、Culture = 中性、PublicKeyToken = null]，Culture = 非特定語言，PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="84954-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="84954-125">範例1</span><span class="sxs-lookup"><span data-stu-id="84954-125">Example 1</span></span>
<span data-ttu-id="84954-126">NameAvailable 原因訊息</span><span class="sxs-lookup"><span data-stu-id="84954-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="84954-127">範例2</span><span class="sxs-lookup"><span data-stu-id="84954-127">Example 2</span></span>
<span data-ttu-id="84954-128">NameAvailable 原因訊息</span><span class="sxs-lookup"><span data-stu-id="84954-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="84954-129">範例3</span><span class="sxs-lookup"><span data-stu-id="84954-129">Example 3</span></span>
<span data-ttu-id="84954-130">NameAvailable 原因訊息</span><span class="sxs-lookup"><span data-stu-id="84954-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="84954-131">筆記</span><span class="sxs-lookup"><span data-stu-id="84954-131">NOTES</span></span>

## <span data-ttu-id="84954-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="84954-132">RELATED LINKS</span></span>

