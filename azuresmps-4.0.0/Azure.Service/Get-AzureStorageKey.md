---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966994"
---
# <span data-ttu-id="62d4a-101">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="62d4a-101">Get-AzureStorageKey</span></span>

## <span data-ttu-id="62d4a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="62d4a-103">傳回 Azure 儲存空間帳戶的主要和次要儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="62d4a-103">Returns the primary and secondary storage account keys for an Azure storage account.</span></span>

## <span data-ttu-id="62d4a-104">句法</span><span class="sxs-lookup"><span data-stu-id="62d4a-104">SYNTAX</span></span>

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="62d4a-105">說明</span><span class="sxs-lookup"><span data-stu-id="62d4a-105">DESCRIPTION</span></span>
<span data-ttu-id="62d4a-106">**AzureStorageKey** Cmdlet 會傳回具有 Azure 儲存空間帳戶名稱的物件、主要帳戶金鑰，以及指定之 Azure 儲存空間帳戶的次要帳戶金鑰做為屬性。</span><span class="sxs-lookup"><span data-stu-id="62d4a-106">The **Get-AzureStorageKey** cmdlet returns an object with the Azure Storage account name, the primary account key, and the secondary account key of the specified Azure storage account as properties.</span></span>

## <span data-ttu-id="62d4a-107">示例</span><span class="sxs-lookup"><span data-stu-id="62d4a-107">EXAMPLES</span></span>

### <span data-ttu-id="62d4a-108">範例1：取得包含主要和次要儲存空間金鑰的物件</span><span class="sxs-lookup"><span data-stu-id="62d4a-108">Example 1: Get an object that contains primary and secondary storage keys</span></span>
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="62d4a-109">這個命令會透過 ContosoStore01 儲存空間帳戶的主要和次要儲存空間來取得物件。</span><span class="sxs-lookup"><span data-stu-id="62d4a-109">This command gets an object with the primary and secondary storage keys for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="62d4a-110">範例2：取得主要儲存空間帳戶金鑰並將它儲存在變數中</span><span class="sxs-lookup"><span data-stu-id="62d4a-110">Example 2: Get the primary storage account key and store it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

<span data-ttu-id="62d4a-111">這個命令會將 ContosoStore01 儲存空間帳戶的 [主要儲存空間] 帳戶金鑰放在 $ContosoStoreKey 變數中。</span><span class="sxs-lookup"><span data-stu-id="62d4a-111">This command puts the primary storage account key for the ContosoStore01 storage account in the $ContosoStoreKey variable.</span></span>

## <span data-ttu-id="62d4a-112">參數</span><span class="sxs-lookup"><span data-stu-id="62d4a-112">PARAMETERS</span></span>

### <span data-ttu-id="62d4a-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="62d4a-113">-InformationAction</span></span>
<span data-ttu-id="62d4a-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="62d4a-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="62d4a-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="62d4a-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="62d4a-116">持續</span><span class="sxs-lookup"><span data-stu-id="62d4a-116">Continue</span></span>
- <span data-ttu-id="62d4a-117">理會</span><span class="sxs-lookup"><span data-stu-id="62d4a-117">Ignore</span></span>
- <span data-ttu-id="62d4a-118">看</span><span class="sxs-lookup"><span data-stu-id="62d4a-118">Inquire</span></span>
- <span data-ttu-id="62d4a-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="62d4a-119">SilentlyContinue</span></span>
- <span data-ttu-id="62d4a-120">停止</span><span class="sxs-lookup"><span data-stu-id="62d4a-120">Stop</span></span>
- <span data-ttu-id="62d4a-121">封存</span><span class="sxs-lookup"><span data-stu-id="62d4a-121">Suspend</span></span>

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

### <span data-ttu-id="62d4a-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="62d4a-122">-InformationVariable</span></span>
<span data-ttu-id="62d4a-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="62d4a-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="62d4a-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="62d4a-124">-Profile</span></span>
<span data-ttu-id="62d4a-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="62d4a-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="62d4a-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="62d4a-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="62d4a-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="62d4a-127">-StorageAccountName</span></span>
<span data-ttu-id="62d4a-128">指定儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="62d4a-128">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62d4a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d4a-129">CommonParameters</span></span>
<span data-ttu-id="62d4a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62d4a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d4a-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62d4a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d4a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="62d4a-132">INPUTS</span></span>

## <span data-ttu-id="62d4a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="62d4a-133">OUTPUTS</span></span>

## <span data-ttu-id="62d4a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="62d4a-134">NOTES</span></span>
* <span data-ttu-id="62d4a-135">若要取得 Node.js 的協助，請使用 `help node-dev` 命令。</span><span class="sxs-lookup"><span data-stu-id="62d4a-135">To get help with Node.js, use the `help node-dev` command.</span></span> <span data-ttu-id="62d4a-136">如需 PHP 延伸的說明，請使用 `help php-dev` 命令。</span><span class="sxs-lookup"><span data-stu-id="62d4a-136">For help with PHP extensions, use the `help php-dev` command.</span></span>

## <span data-ttu-id="62d4a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="62d4a-137">RELATED LINKS</span></span>

[<span data-ttu-id="62d4a-138">AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="62d4a-138">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="62d4a-139">新-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="62d4a-139">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="62d4a-140">新-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="62d4a-140">New-AzureStorageKey</span></span>](./New-AzureStorageKey.md)

[<span data-ttu-id="62d4a-141">移除-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="62d4a-141">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)

[<span data-ttu-id="62d4a-142">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="62d4a-142">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


