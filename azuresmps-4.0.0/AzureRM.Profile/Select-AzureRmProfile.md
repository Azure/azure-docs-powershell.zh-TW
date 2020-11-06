---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442976"
---
# <span data-ttu-id="fc881-101">Select-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="fc881-101">Select-AzureRmProfile</span></span>

## <span data-ttu-id="fc881-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc881-102">SYNOPSIS</span></span>
<span data-ttu-id="fc881-103">從檔案載入 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="fc881-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="fc881-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc881-104">SYNTAX</span></span>

### <span data-ttu-id="fc881-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="fc881-105">InMemoryProfile</span></span>
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### <span data-ttu-id="fc881-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="fc881-106">ProfileFromDisk</span></span>
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## <span data-ttu-id="fc881-107">說明</span><span class="sxs-lookup"><span data-stu-id="fc881-107">DESCRIPTION</span></span>
<span data-ttu-id="fc881-108">Select-AzureRmProfile Cmdlet 會從檔案載入驗證資訊，以設定 Azure 環境和內容。</span><span class="sxs-lookup"><span data-stu-id="fc881-108">The Select-AzureRmProfile cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="fc881-109">您在目前會話中執行的 Cmdlet 會使用這項資訊來驗證 Azure 資源管理員的要求。</span><span class="sxs-lookup"><span data-stu-id="fc881-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="fc881-110">示例</span><span class="sxs-lookup"><span data-stu-id="fc881-110">EXAMPLES</span></span>

### <span data-ttu-id="fc881-111">範例1：從 PSAzureProfile 選取設定檔</span><span class="sxs-lookup"><span data-stu-id="fc881-111">Example 1: Selecting a profile from a PSAzureProfile</span></span>
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="fc881-112">這個範例會從傳遞到 Cmdlet 的 PSAzureProfile 選取設定檔。</span><span class="sxs-lookup"><span data-stu-id="fc881-112">This example selects a profile from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="fc881-113">範例2：從 JSON 檔案選取設定檔</span><span class="sxs-lookup"><span data-stu-id="fc881-113">Example 2: Selecting a profile from a JSON file</span></span>
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="fc881-114">這個範例會從傳遞到 Cmdlet 的 JSON 檔案選取一個設定檔。</span><span class="sxs-lookup"><span data-stu-id="fc881-114">This example selects a profile from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="fc881-115">您可以從 [儲存-AzureRmProfile] 建立此 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="fc881-115">This JSON file can be created from Save-AzureRmProfile.</span></span>

## <span data-ttu-id="fc881-116">參數</span><span class="sxs-lookup"><span data-stu-id="fc881-116">PARAMETERS</span></span>

### <span data-ttu-id="fc881-117">-Path</span><span class="sxs-lookup"><span data-stu-id="fc881-117">-Path</span></span>
<span data-ttu-id="fc881-118">指定使用 Save AzureRMProfile 儲存的個人資料資訊的路徑。</span><span class="sxs-lookup"><span data-stu-id="fc881-118">Specifies the path to profile information saved by using Save-AzureRMProfile.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc881-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="fc881-119">-Profile</span></span>
<span data-ttu-id="fc881-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="fc881-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fc881-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="fc881-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc881-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc881-122">CommonParameters</span></span>
<span data-ttu-id="fc881-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc881-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc881-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc881-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc881-125">輸入</span><span class="sxs-lookup"><span data-stu-id="fc881-125">INPUTS</span></span>

## <span data-ttu-id="fc881-126">輸出</span><span class="sxs-lookup"><span data-stu-id="fc881-126">OUTPUTS</span></span>

### <span data-ttu-id="fc881-127">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="fc881-127">PSAzureProfile</span></span>

## <span data-ttu-id="fc881-128">筆記</span><span class="sxs-lookup"><span data-stu-id="fc881-128">NOTES</span></span>

## <span data-ttu-id="fc881-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc881-129">RELATED LINKS</span></span>

[<span data-ttu-id="fc881-130">AzureRMCoNtext</span><span class="sxs-lookup"><span data-stu-id="fc881-130">Get-AzureRMContext</span></span>]()

