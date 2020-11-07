---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 09ABE9E2-1080-4DEF-92DD-B8FF4C8B308C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9afdaafa57592239d0c24870e4459d650fac84c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967649"
---
# <span data-ttu-id="0ff35-101">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="0ff35-101">New-AzureStorageKey</span></span>

## <span data-ttu-id="0ff35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ff35-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff35-103">重新生成 Azure 儲存空間帳戶的儲存空間金鑰。</span><span class="sxs-lookup"><span data-stu-id="0ff35-103">Regenerates storage keys for an Azure storage account.</span></span>

## <span data-ttu-id="0ff35-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ff35-104">SYNTAX</span></span>

```
New-AzureStorageKey [-KeyType] <String> [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0ff35-105">說明</span><span class="sxs-lookup"><span data-stu-id="0ff35-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff35-106">**新的-AzureStorageKey** Cmdlet 會為 Azure 儲存空間帳戶重新產生主要或次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="0ff35-106">The **New-AzureStorageKey** cmdlet regenerates the primary or secondary key for an Azure Storage account.</span></span>
<span data-ttu-id="0ff35-107">它會傳回包含儲存空間帳戶名稱、主鍵和輔助金鑰做為屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="0ff35-107">It returns an object that contains the storage account name, primary key, and secondary key as properties.</span></span>

## <span data-ttu-id="0ff35-108">示例</span><span class="sxs-lookup"><span data-stu-id="0ff35-108">EXAMPLES</span></span>

### <span data-ttu-id="0ff35-109">範例1：重新產生主要儲存金鑰</span><span class="sxs-lookup"><span data-stu-id="0ff35-109">Example 1: Regenerate a primary storage key</span></span>
```
PS C:\> New-AzureStorageKey -KeyType "Primary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="0ff35-110">這個命令會重新生成 ContosoStore01 儲存空間帳戶的主要儲存空間金鑰。</span><span class="sxs-lookup"><span data-stu-id="0ff35-110">This command regenerates the primary storage key for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="0ff35-111">範例2：重新產生次要儲存金鑰並將它儲存在變數中</span><span class="sxs-lookup"><span data-stu-id="0ff35-111">Example 2: Regenerate a secondary storage key and save it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = New-AzureStorageKey -KeyType "Secondary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="0ff35-112">這個命令會重新產生 ContosoStore01 儲存空間帳戶的副儲存空間，並將更新的儲存空間帳戶金鑰資訊儲存在 $ContosoStoreKey 中。</span><span class="sxs-lookup"><span data-stu-id="0ff35-112">This command regenerate the secondary storage key for the ContosoStore01 storage account and stores the updated storage account key information in the $ContosoStoreKey.</span></span>

## <span data-ttu-id="0ff35-113">參數</span><span class="sxs-lookup"><span data-stu-id="0ff35-113">PARAMETERS</span></span>

### <span data-ttu-id="0ff35-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0ff35-114">-InformationAction</span></span>
<span data-ttu-id="0ff35-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="0ff35-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0ff35-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0ff35-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ff35-117">持續</span><span class="sxs-lookup"><span data-stu-id="0ff35-117">Continue</span></span>
- <span data-ttu-id="0ff35-118">理會</span><span class="sxs-lookup"><span data-stu-id="0ff35-118">Ignore</span></span>
- <span data-ttu-id="0ff35-119">看</span><span class="sxs-lookup"><span data-stu-id="0ff35-119">Inquire</span></span>
- <span data-ttu-id="0ff35-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0ff35-120">SilentlyContinue</span></span>
- <span data-ttu-id="0ff35-121">停止</span><span class="sxs-lookup"><span data-stu-id="0ff35-121">Stop</span></span>
- <span data-ttu-id="0ff35-122">封存</span><span class="sxs-lookup"><span data-stu-id="0ff35-122">Suspend</span></span>

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

### <span data-ttu-id="0ff35-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0ff35-123">-InformationVariable</span></span>
<span data-ttu-id="0ff35-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="0ff35-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0ff35-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="0ff35-125">-KeyType</span></span>
<span data-ttu-id="0ff35-126">指定要重新產生的金鑰。</span><span class="sxs-lookup"><span data-stu-id="0ff35-126">Specifies which key to regenerate.</span></span>
<span data-ttu-id="0ff35-127">有效值為：主要和次要。</span><span class="sxs-lookup"><span data-stu-id="0ff35-127">Valid values are: Primary and Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff35-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0ff35-128">-Profile</span></span>
<span data-ttu-id="0ff35-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0ff35-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ff35-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0ff35-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ff35-131">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0ff35-131">-StorageAccountName</span></span>
<span data-ttu-id="0ff35-132">指定要重新產生金鑰之 Azure 儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ff35-132">Specifies the name of the Azure Storage account for which to regenerate a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff35-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff35-133">CommonParameters</span></span>
<span data-ttu-id="0ff35-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ff35-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff35-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0ff35-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff35-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0ff35-136">INPUTS</span></span>

## <span data-ttu-id="0ff35-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0ff35-137">OUTPUTS</span></span>

### <span data-ttu-id="0ff35-138">StorageServiceKeys</span><span class="sxs-lookup"><span data-stu-id="0ff35-138">StorageServiceKeys</span></span>

## <span data-ttu-id="0ff35-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0ff35-139">NOTES</span></span>

## <span data-ttu-id="0ff35-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ff35-140">RELATED LINKS</span></span>

[<span data-ttu-id="0ff35-141">AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="0ff35-141">Get-AzureStorageKey</span></span>](./Get-AzureStorageKey.md)


