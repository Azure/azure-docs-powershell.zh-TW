---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 679452A6-A6CA-4DC8-8E00-09E369505319
online version: ''
schema: 2.0.0
ms.openlocfilehash: 933c6de8e7baa55b2093a7ffc4ac28fede13bb5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967904"
---
# <span data-ttu-id="0f278-101">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f278-101">Remove-AzureStorageAccount</span></span>

## <span data-ttu-id="0f278-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f278-102">SYNOPSIS</span></span>
<span data-ttu-id="0f278-103">從訂閱中刪除指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0f278-103">Deletes the specified storage account from a subscription.</span></span>

## <span data-ttu-id="0f278-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f278-104">SYNTAX</span></span>

```
Remove-AzureStorageAccount [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0f278-105">說明</span><span class="sxs-lookup"><span data-stu-id="0f278-105">DESCRIPTION</span></span>
<span data-ttu-id="0f278-106">**AzureStorageAccount** Cmdlet 會從 Azure 訂閱中移除帳戶。</span><span class="sxs-lookup"><span data-stu-id="0f278-106">The **Remove-AzureStorageAccount** cmdlet removes an account from an Azure subscription.</span></span>

## <span data-ttu-id="0f278-107">示例</span><span class="sxs-lookup"><span data-stu-id="0f278-107">EXAMPLES</span></span>

### <span data-ttu-id="0f278-108">範例1：移除儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="0f278-108">Example 1: Remove a storage account</span></span>
```
PS C:\> Remove-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="0f278-109">這個命令會從指定的訂閱中移除 ContosoStore01 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0f278-109">This command removes the ContosoStore01 storage account from the specified subscription.</span></span>

## <span data-ttu-id="0f278-110">參數</span><span class="sxs-lookup"><span data-stu-id="0f278-110">PARAMETERS</span></span>

### <span data-ttu-id="0f278-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0f278-111">-InformationAction</span></span>
<span data-ttu-id="0f278-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="0f278-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0f278-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0f278-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f278-114">持續</span><span class="sxs-lookup"><span data-stu-id="0f278-114">Continue</span></span>
- <span data-ttu-id="0f278-115">理會</span><span class="sxs-lookup"><span data-stu-id="0f278-115">Ignore</span></span>
- <span data-ttu-id="0f278-116">看</span><span class="sxs-lookup"><span data-stu-id="0f278-116">Inquire</span></span>
- <span data-ttu-id="0f278-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0f278-117">SilentlyContinue</span></span>
- <span data-ttu-id="0f278-118">停止</span><span class="sxs-lookup"><span data-stu-id="0f278-118">Stop</span></span>
- <span data-ttu-id="0f278-119">封存</span><span class="sxs-lookup"><span data-stu-id="0f278-119">Suspend</span></span>

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

### <span data-ttu-id="0f278-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0f278-120">-InformationVariable</span></span>
<span data-ttu-id="0f278-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="0f278-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0f278-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0f278-122">-Profile</span></span>
<span data-ttu-id="0f278-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0f278-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f278-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0f278-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f278-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0f278-125">-StorageAccountName</span></span>
<span data-ttu-id="0f278-126">指定要移除的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0f278-126">Specifies the name of the storage account to remove.</span></span>

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

### <span data-ttu-id="0f278-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f278-127">CommonParameters</span></span>
<span data-ttu-id="0f278-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f278-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f278-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0f278-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f278-130">輸入</span><span class="sxs-lookup"><span data-stu-id="0f278-130">INPUTS</span></span>

## <span data-ttu-id="0f278-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0f278-131">OUTPUTS</span></span>

## <span data-ttu-id="0f278-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0f278-132">NOTES</span></span>

## <span data-ttu-id="0f278-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f278-133">RELATED LINKS</span></span>

[<span data-ttu-id="0f278-134">AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f278-134">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="0f278-135">新-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f278-135">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="0f278-136">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f278-136">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


