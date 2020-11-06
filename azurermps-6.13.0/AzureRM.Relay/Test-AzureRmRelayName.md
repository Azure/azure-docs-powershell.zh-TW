---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 396243e366f6a21e2ac94d105473b348c6a8198d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452736"
---
# <span data-ttu-id="2a6da-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="2a6da-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="2a6da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a6da-102">SYNOPSIS</span></span>
<span data-ttu-id="2a6da-103">檢查指定命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="2a6da-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a6da-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a6da-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a6da-105">說明</span><span class="sxs-lookup"><span data-stu-id="2a6da-105">DESCRIPTION</span></span>
<span data-ttu-id="2a6da-106">**Test AzureRmRelayName** Cmdlet 會檢查命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="2a6da-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="2a6da-107">示例</span><span class="sxs-lookup"><span data-stu-id="2a6da-107">EXAMPLES</span></span>

### <span data-ttu-id="2a6da-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2a6da-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="2a6da-109">範例2</span><span class="sxs-lookup"><span data-stu-id="2a6da-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="2a6da-110">範例3</span><span class="sxs-lookup"><span data-stu-id="2a6da-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="2a6da-111">傳回命名空間名稱的可用性狀態</span><span class="sxs-lookup"><span data-stu-id="2a6da-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="2a6da-112">參數</span><span class="sxs-lookup"><span data-stu-id="2a6da-112">PARAMETERS</span></span>

### <span data-ttu-id="2a6da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a6da-113">-DefaultProfile</span></span>
<span data-ttu-id="2a6da-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a6da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a6da-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="2a6da-115">-Namespace</span></span>
<span data-ttu-id="2a6da-116">中繼命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="2a6da-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="2a6da-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a6da-117">CommonParameters</span></span>
<span data-ttu-id="2a6da-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a6da-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2a6da-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a6da-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a6da-120">輸入</span><span class="sxs-lookup"><span data-stu-id="2a6da-120">INPUTS</span></span>

### <span data-ttu-id="2a6da-121">System.object</span><span class="sxs-lookup"><span data-stu-id="2a6da-121">System.String</span></span>


## <span data-ttu-id="2a6da-122">輸出</span><span class="sxs-lookup"><span data-stu-id="2a6da-122">OUTPUTS</span></span>

### <span data-ttu-id="2a6da-123">PSCheckNameAvailabilityResultAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2a6da-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="2a6da-124">筆記</span><span class="sxs-lookup"><span data-stu-id="2a6da-124">NOTES</span></span>

## <span data-ttu-id="2a6da-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a6da-125">RELATED LINKS</span></span>
