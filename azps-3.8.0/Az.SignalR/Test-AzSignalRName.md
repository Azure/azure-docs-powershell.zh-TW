---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957225"
---
# <span data-ttu-id="fe312-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="fe312-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="fe312-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe312-102">SYNOPSIS</span></span>
<span data-ttu-id="fe312-103">檢查名稱是否有空。</span><span class="sxs-lookup"><span data-stu-id="fe312-103">Check the availability of a name.</span></span> <span data-ttu-id="fe312-104">別名： Test-AzSignal。</span><span class="sxs-lookup"><span data-stu-id="fe312-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="fe312-105">句法</span><span class="sxs-lookup"><span data-stu-id="fe312-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe312-106">說明</span><span class="sxs-lookup"><span data-stu-id="fe312-106">DESCRIPTION</span></span>
<span data-ttu-id="fe312-107">檢查名稱是否有空。</span><span class="sxs-lookup"><span data-stu-id="fe312-107">Check the availability of a name.</span></span> <span data-ttu-id="fe312-108">別名： Test-AzSignal。</span><span class="sxs-lookup"><span data-stu-id="fe312-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="fe312-109">示例</span><span class="sxs-lookup"><span data-stu-id="fe312-109">EXAMPLES</span></span>

### <span data-ttu-id="fe312-110">檢查已存在的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe312-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="fe312-111">檢查 unexisted 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe312-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="fe312-112">參數</span><span class="sxs-lookup"><span data-stu-id="fe312-112">PARAMETERS</span></span>

### <span data-ttu-id="fe312-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe312-113">-DefaultProfile</span></span>
<span data-ttu-id="fe312-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe312-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe312-115">-位置</span><span class="sxs-lookup"><span data-stu-id="fe312-115">-Location</span></span>
<span data-ttu-id="fe312-116">SignalR 服務位置。</span><span class="sxs-lookup"><span data-stu-id="fe312-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="fe312-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe312-117">-Name</span></span>
<span data-ttu-id="fe312-118">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="fe312-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="fe312-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe312-119">CommonParameters</span></span>
<span data-ttu-id="fe312-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe312-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe312-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe312-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe312-122">輸入</span><span class="sxs-lookup"><span data-stu-id="fe312-122">INPUTS</span></span>

### <span data-ttu-id="fe312-123">System.object</span><span class="sxs-lookup"><span data-stu-id="fe312-123">System.String</span></span>

## <span data-ttu-id="fe312-124">輸出</span><span class="sxs-lookup"><span data-stu-id="fe312-124">OUTPUTS</span></span>

### <span data-ttu-id="fe312-125">System.object</span><span class="sxs-lookup"><span data-stu-id="fe312-125">System.Boolean</span></span>

## <span data-ttu-id="fe312-126">筆記</span><span class="sxs-lookup"><span data-stu-id="fe312-126">NOTES</span></span>

## <span data-ttu-id="fe312-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe312-127">RELATED LINKS</span></span>
