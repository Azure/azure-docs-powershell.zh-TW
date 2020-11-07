---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 796f241ebd554647f22e3c5216807e1644c9d769
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791342"
---
# <span data-ttu-id="7ccf3-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="7ccf3-101">Test-AzRelayName</span></span>

## <span data-ttu-id="7ccf3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ccf3-102">SYNOPSIS</span></span>
<span data-ttu-id="7ccf3-103">檢查指定命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="7ccf3-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="7ccf3-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ccf3-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ccf3-105">說明</span><span class="sxs-lookup"><span data-stu-id="7ccf3-105">DESCRIPTION</span></span>
<span data-ttu-id="7ccf3-106">**Test AzRelayName** Cmdlet 會檢查命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="7ccf3-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="7ccf3-107">示例</span><span class="sxs-lookup"><span data-stu-id="7ccf3-107">EXAMPLES</span></span>

### <span data-ttu-id="7ccf3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7ccf3-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="7ccf3-109">範例2</span><span class="sxs-lookup"><span data-stu-id="7ccf3-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="7ccf3-110">範例3</span><span class="sxs-lookup"><span data-stu-id="7ccf3-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="7ccf3-111">傳回命名空間名稱的可用性狀態</span><span class="sxs-lookup"><span data-stu-id="7ccf3-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="7ccf3-112">參數</span><span class="sxs-lookup"><span data-stu-id="7ccf3-112">PARAMETERS</span></span>

### <span data-ttu-id="7ccf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ccf3-113">-DefaultProfile</span></span>
<span data-ttu-id="7ccf3-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ccf3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ccf3-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7ccf3-115">-Namespace</span></span>
<span data-ttu-id="7ccf3-116">中繼命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="7ccf3-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="7ccf3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ccf3-117">CommonParameters</span></span>
<span data-ttu-id="7ccf3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ccf3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ccf3-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7ccf3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ccf3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="7ccf3-120">INPUTS</span></span>

### <span data-ttu-id="7ccf3-121">System.object</span><span class="sxs-lookup"><span data-stu-id="7ccf3-121">System.String</span></span>

## <span data-ttu-id="7ccf3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="7ccf3-122">OUTPUTS</span></span>

### <span data-ttu-id="7ccf3-123">PSCheckNameAvailabilityResultAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7ccf3-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="7ccf3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="7ccf3-124">NOTES</span></span>

## <span data-ttu-id="7ccf3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ccf3-125">RELATED LINKS</span></span>
