---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: be0b0f2aa9aa45fa69b3d57051a5671a76186abc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914538"
---
# <span data-ttu-id="65992-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="65992-101">Test-AzRelayName</span></span>

## <span data-ttu-id="65992-102">簡介</span><span class="sxs-lookup"><span data-stu-id="65992-102">SYNOPSIS</span></span>
<span data-ttu-id="65992-103">檢查指定 NameSpace 名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="65992-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="65992-104">語法</span><span class="sxs-lookup"><span data-stu-id="65992-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65992-105">描述</span><span class="sxs-lookup"><span data-stu-id="65992-105">DESCRIPTION</span></span>
<span data-ttu-id="65992-106">**Test-AzRelayName** Cmdlet 檢查 NameSpace 名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="65992-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="65992-107">例子</span><span class="sxs-lookup"><span data-stu-id="65992-107">EXAMPLES</span></span>

### <span data-ttu-id="65992-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="65992-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="65992-109">範例 2</span><span class="sxs-lookup"><span data-stu-id="65992-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="65992-110">範例 3</span><span class="sxs-lookup"><span data-stu-id="65992-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="65992-111">在命名空間名稱可用性時，返回狀態</span><span class="sxs-lookup"><span data-stu-id="65992-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="65992-112">參數</span><span class="sxs-lookup"><span data-stu-id="65992-112">PARAMETERS</span></span>

### <span data-ttu-id="65992-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65992-113">-DefaultProfile</span></span>
<span data-ttu-id="65992-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="65992-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65992-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="65992-115">-Namespace</span></span>
<span data-ttu-id="65992-116">轉場命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="65992-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="65992-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65992-117">CommonParameters</span></span>
<span data-ttu-id="65992-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="65992-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65992-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="65992-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65992-120">輸入</span><span class="sxs-lookup"><span data-stu-id="65992-120">INPUTS</span></span>

### <span data-ttu-id="65992-121">System.String</span><span class="sxs-lookup"><span data-stu-id="65992-121">System.String</span></span>

## <span data-ttu-id="65992-122">輸出</span><span class="sxs-lookup"><span data-stu-id="65992-122">OUTPUTS</span></span>

### <span data-ttu-id="65992-123">Microsoft.Azure.Commands.Relay.models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="65992-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="65992-124">筆記</span><span class="sxs-lookup"><span data-stu-id="65992-124">NOTES</span></span>

## <span data-ttu-id="65992-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="65992-125">RELATED LINKS</span></span>
