---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966995"
---
# <span data-ttu-id="9b61f-101">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b61f-101">Get-AzureStorageAccount</span></span>

## <span data-ttu-id="9b61f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b61f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b61f-103">取得目前 Azure 訂閱的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="9b61f-103">Gets the storage accounts for the current Azure subscription.</span></span>

## <span data-ttu-id="9b61f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b61f-104">SYNTAX</span></span>

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9b61f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b61f-105">DESCRIPTION</span></span>
<span data-ttu-id="9b61f-106">**AzureStorageAccount** Cmdlet 會傳回一個物件，其中包含目前訂閱之儲存空間帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b61f-106">The **Get-AzureStorageAccount** cmdlet returns an object containing information about the storage accounts for the current subscription.</span></span>
<span data-ttu-id="9b61f-107">如果指定了 *StorageAccountName* 參數，則只會傳回指定儲存空間帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b61f-107">If the *StorageAccountName* parameter is specified, then only information about the specified storage account is returned.</span></span>

## <span data-ttu-id="9b61f-108">示例</span><span class="sxs-lookup"><span data-stu-id="9b61f-108">EXAMPLES</span></span>

### <span data-ttu-id="9b61f-109">範例1：返回所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="9b61f-109">Example 1: Return all storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount
```

<span data-ttu-id="9b61f-110">這個命令會傳回與目前訂閱相關聯之所有儲存空間帳戶的物件。</span><span class="sxs-lookup"><span data-stu-id="9b61f-110">This command returns an object with all the storage accounts associated with the current subscription.</span></span>

### <span data-ttu-id="9b61f-111">範例2：返回指定帳戶的帳戶資訊</span><span class="sxs-lookup"><span data-stu-id="9b61f-111">Example 2: Return account information for a specified account</span></span>
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="9b61f-112">這個命令會傳回只有 ContosoStore01 帳戶資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="9b61f-112">This command returns an object with only the ContosoStore01 account information.</span></span>

### <span data-ttu-id="9b61f-113">範例3：顯示儲存空間帳戶資料表</span><span class="sxs-lookup"><span data-stu-id="9b61f-113">Example 3: Display a table of storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

<span data-ttu-id="9b61f-114">這個命令會傳回與目前訂閱相關的所有儲存空間帳戶的物件，並將其輸出為顯示帳戶名稱、帳戶標籤和儲存位置的表格。</span><span class="sxs-lookup"><span data-stu-id="9b61f-114">This command returns an object with all the storage accounts associated with the current subscription, and outputs them as a table showing the account name, the account label, and the storage location.</span></span>

## <span data-ttu-id="9b61f-115">參數</span><span class="sxs-lookup"><span data-stu-id="9b61f-115">PARAMETERS</span></span>

### <span data-ttu-id="9b61f-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9b61f-116">-InformationAction</span></span>
<span data-ttu-id="9b61f-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="9b61f-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9b61f-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9b61f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b61f-119">持續</span><span class="sxs-lookup"><span data-stu-id="9b61f-119">Continue</span></span>
- <span data-ttu-id="9b61f-120">理會</span><span class="sxs-lookup"><span data-stu-id="9b61f-120">Ignore</span></span>
- <span data-ttu-id="9b61f-121">看</span><span class="sxs-lookup"><span data-stu-id="9b61f-121">Inquire</span></span>
- <span data-ttu-id="9b61f-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9b61f-122">SilentlyContinue</span></span>
- <span data-ttu-id="9b61f-123">停止</span><span class="sxs-lookup"><span data-stu-id="9b61f-123">Stop</span></span>
- <span data-ttu-id="9b61f-124">封存</span><span class="sxs-lookup"><span data-stu-id="9b61f-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b61f-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9b61f-125">-InformationVariable</span></span>
<span data-ttu-id="9b61f-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="9b61f-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b61f-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9b61f-127">-Profile</span></span>
<span data-ttu-id="9b61f-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9b61f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b61f-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9b61f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b61f-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9b61f-130">-StorageAccountName</span></span>
<span data-ttu-id="9b61f-131">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b61f-131">Specifies the name of a storage account.</span></span>
<span data-ttu-id="9b61f-132">如果已指定，這個 Cmdlet 只會傳回指定的儲存空間帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="9b61f-132">If specified, this cmdlet returns only the specified storage account object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b61f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b61f-133">CommonParameters</span></span>
<span data-ttu-id="9b61f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b61f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b61f-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b61f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b61f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="9b61f-136">INPUTS</span></span>

## <span data-ttu-id="9b61f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9b61f-137">OUTPUTS</span></span>

### <span data-ttu-id="9b61f-138">ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="9b61f-138">ManagementOperationContext</span></span>

## <span data-ttu-id="9b61f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9b61f-139">NOTES</span></span>
* <span data-ttu-id="9b61f-140">輸入 `help node-dev` 以取得 Node.js 與開發相關的 Cmdlet 的說明。</span><span class="sxs-lookup"><span data-stu-id="9b61f-140">Type `help node-dev` to get help on Node.js development-related cmdlets.</span></span> <span data-ttu-id="9b61f-141">輸入 `help php-dev` 以取得有關 PHP 開發相關 Cmdlet 的說明。</span><span class="sxs-lookup"><span data-stu-id="9b61f-141">Type `help php-dev` to get help on PHP development-related cmdlets.</span></span>

## <span data-ttu-id="9b61f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b61f-142">RELATED LINKS</span></span>

[<span data-ttu-id="9b61f-143">新-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b61f-143">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="9b61f-144">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b61f-144">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


