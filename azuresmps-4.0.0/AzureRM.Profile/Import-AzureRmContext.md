---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93442103"
---
# <span data-ttu-id="c4f50-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="c4f50-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="c4f50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4f50-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f50-103">從檔案載入 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="c4f50-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="c4f50-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4f50-104">SYNTAX</span></span>

### <span data-ttu-id="c4f50-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="c4f50-105">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c4f50-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="c4f50-106">ProfileFromDisk</span></span>
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c4f50-107">說明</span><span class="sxs-lookup"><span data-stu-id="c4f50-107">DESCRIPTION</span></span>
<span data-ttu-id="c4f50-108">Import-AzureRmContext Cmdlet 會從檔案載入驗證資訊，以設定 Azure 環境和內容。</span><span class="sxs-lookup"><span data-stu-id="c4f50-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="c4f50-109">您在目前會話中執行的 Cmdlet 會使用這項資訊來驗證 Azure 資源管理員的要求。</span><span class="sxs-lookup"><span data-stu-id="c4f50-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="c4f50-110">示例</span><span class="sxs-lookup"><span data-stu-id="c4f50-110">EXAMPLES</span></span>

### <span data-ttu-id="c4f50-111">範例1：從 AzureRmProfile 匯入內容</span><span class="sxs-lookup"><span data-stu-id="c4f50-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="c4f50-112">這個範例會從傳遞到 Cmdlet 的 PSAzureProfile 匯入內容。</span><span class="sxs-lookup"><span data-stu-id="c4f50-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="c4f50-113">範例2：從 JSON 檔案匯入內容</span><span class="sxs-lookup"><span data-stu-id="c4f50-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="c4f50-114">這個範例會從傳遞到 Cmdlet 的 JSON 檔案選取內容。</span><span class="sxs-lookup"><span data-stu-id="c4f50-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span>
<span data-ttu-id="c4f50-115">您可以從匯入-AzureRmCoNtext 建立此 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="c4f50-115">This JSON file can be created from Import-AzureRmContext.</span></span>

## <span data-ttu-id="c4f50-116">參數</span><span class="sxs-lookup"><span data-stu-id="c4f50-116">PARAMETERS</span></span>

### <span data-ttu-id="c4f50-117">-AzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="c4f50-117">-AzureContext</span></span>
<span data-ttu-id="c4f50-118">指定此 Cmdlet 讀取的 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="c4f50-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="c4f50-119">如果您沒有指定內容，這個 Cmdlet 會從本機預設的內容讀取。</span><span class="sxs-lookup"><span data-stu-id="c4f50-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4f50-120">-Path</span><span class="sxs-lookup"><span data-stu-id="c4f50-120">-Path</span></span>
<span data-ttu-id="c4f50-121">指定使用 Save AzureRMCoNtext 儲存之內容資訊的路徑。</span><span class="sxs-lookup"><span data-stu-id="c4f50-121">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4f50-122">-確認</span><span class="sxs-lookup"><span data-stu-id="c4f50-122">-Confirm</span></span>
<span data-ttu-id="c4f50-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c4f50-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f50-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4f50-124">-WhatIf</span></span>
<span data-ttu-id="c4f50-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4f50-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4f50-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4f50-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="c4f50-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c4f50-127">INPUTS</span></span>

### <span data-ttu-id="c4f50-128">AzureRMProfile 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="c4f50-128">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="c4f50-129">System.object</span><span class="sxs-lookup"><span data-stu-id="c4f50-129">System.String</span></span>

## <span data-ttu-id="c4f50-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c4f50-130">OUTPUTS</span></span>

### <span data-ttu-id="c4f50-131">PSAzureProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="c4f50-131">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="c4f50-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c4f50-132">NOTES</span></span>

## <span data-ttu-id="c4f50-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4f50-133">RELATED LINKS</span></span>

