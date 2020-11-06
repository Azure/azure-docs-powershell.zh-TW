---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 4b3afc0b41f6eaf68e7ec0c4f8ed976b36267c97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446683"
---
# <span data-ttu-id="d67a5-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="d67a5-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="d67a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d67a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d67a5-103">檢查指定命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="d67a5-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d67a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d67a5-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d67a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="d67a5-105">DESCRIPTION</span></span>
<span data-ttu-id="d67a5-106">**Test AzureRmRelayName** Cmdlet 會檢查命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="d67a5-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="d67a5-107">示例</span><span class="sxs-lookup"><span data-stu-id="d67a5-107">EXAMPLES</span></span>

### <span data-ttu-id="d67a5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d67a5-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="d67a5-109">範例2</span><span class="sxs-lookup"><span data-stu-id="d67a5-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="d67a5-110">範例3</span><span class="sxs-lookup"><span data-stu-id="d67a5-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="d67a5-111">傳回命名空間名稱的可用性狀態</span><span class="sxs-lookup"><span data-stu-id="d67a5-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="d67a5-112">參數</span><span class="sxs-lookup"><span data-stu-id="d67a5-112">PARAMETERS</span></span>

### <span data-ttu-id="d67a5-113">-命名空間</span><span class="sxs-lookup"><span data-stu-id="d67a5-113">-Namespace</span></span>
<span data-ttu-id="d67a5-114">中繼命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="d67a5-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="d67a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67a5-115">-DefaultProfile</span></span>
<span data-ttu-id="d67a5-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d67a5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d67a5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67a5-117">CommonParameters</span></span>
<span data-ttu-id="d67a5-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d67a5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67a5-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d67a5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67a5-120">輸入</span><span class="sxs-lookup"><span data-stu-id="d67a5-120">INPUTS</span></span>

### <span data-ttu-id="d67a5-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="d67a5-121">-Namespace</span></span>
 <span data-ttu-id="d67a5-122">System.object</span><span class="sxs-lookup"><span data-stu-id="d67a5-122">System.String</span></span>

## <span data-ttu-id="d67a5-123">輸出</span><span class="sxs-lookup"><span data-stu-id="d67a5-123">OUTPUTS</span></span>

### <span data-ttu-id="d67a5-124">[CheckNameAvailabilityResultAttributes、0.1.0.0、Culture = 中性、PublicKeyToken = null]，Culture = 非特定語言，PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="d67a5-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="d67a5-125">範例1</span><span class="sxs-lookup"><span data-stu-id="d67a5-125">Example 1</span></span>
<span data-ttu-id="d67a5-126">NameAvailable 原因訊息</span><span class="sxs-lookup"><span data-stu-id="d67a5-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="d67a5-127">範例2</span><span class="sxs-lookup"><span data-stu-id="d67a5-127">Example 2</span></span>
<span data-ttu-id="d67a5-128">NameAvailable 原因訊息</span><span class="sxs-lookup"><span data-stu-id="d67a5-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="d67a5-129">範例3</span><span class="sxs-lookup"><span data-stu-id="d67a5-129">Example 3</span></span>
<span data-ttu-id="d67a5-130">NameAvailable 原因訊息</span><span class="sxs-lookup"><span data-stu-id="d67a5-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="d67a5-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d67a5-131">NOTES</span></span>

## <span data-ttu-id="d67a5-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d67a5-132">RELATED LINKS</span></span>

