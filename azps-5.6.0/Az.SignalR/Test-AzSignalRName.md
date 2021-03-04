---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: 01fc755564fdfd702773c31a52e13d8a95c40ede
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902762"
---
# <span data-ttu-id="773a1-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="773a1-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="773a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="773a1-102">SYNOPSIS</span></span>
<span data-ttu-id="773a1-103">檢查名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="773a1-103">Check the availability of a name.</span></span> <span data-ttu-id="773a1-104">別名：Test-AzSignal。</span><span class="sxs-lookup"><span data-stu-id="773a1-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="773a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="773a1-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="773a1-106">描述</span><span class="sxs-lookup"><span data-stu-id="773a1-106">DESCRIPTION</span></span>
<span data-ttu-id="773a1-107">檢查名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="773a1-107">Check the availability of a name.</span></span> <span data-ttu-id="773a1-108">別名：Test-AzSignal。</span><span class="sxs-lookup"><span data-stu-id="773a1-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="773a1-109">例子</span><span class="sxs-lookup"><span data-stu-id="773a1-109">EXAMPLES</span></span>

### <span data-ttu-id="773a1-110">檢查已存在的名稱。</span><span class="sxs-lookup"><span data-stu-id="773a1-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="773a1-111">檢查未顯示的名稱。</span><span class="sxs-lookup"><span data-stu-id="773a1-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="773a1-112">參數</span><span class="sxs-lookup"><span data-stu-id="773a1-112">PARAMETERS</span></span>

### <span data-ttu-id="773a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="773a1-113">-DefaultProfile</span></span>
<span data-ttu-id="773a1-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="773a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="773a1-115">-位置</span><span class="sxs-lookup"><span data-stu-id="773a1-115">-Location</span></span>
<span data-ttu-id="773a1-116">SignalR 服務位置。</span><span class="sxs-lookup"><span data-stu-id="773a1-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="773a1-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="773a1-117">-Name</span></span>
<span data-ttu-id="773a1-118">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="773a1-118">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="773a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="773a1-119">CommonParameters</span></span>
<span data-ttu-id="773a1-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="773a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="773a1-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="773a1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="773a1-122">輸入</span><span class="sxs-lookup"><span data-stu-id="773a1-122">INPUTS</span></span>

### <span data-ttu-id="773a1-123">System.String</span><span class="sxs-lookup"><span data-stu-id="773a1-123">System.String</span></span>

## <span data-ttu-id="773a1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="773a1-124">OUTPUTS</span></span>

### <span data-ttu-id="773a1-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="773a1-125">System.Boolean</span></span>

## <span data-ttu-id="773a1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="773a1-126">NOTES</span></span>

## <span data-ttu-id="773a1-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="773a1-127">RELATED LINKS</span></span>
